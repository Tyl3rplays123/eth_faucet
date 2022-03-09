# ETH Faucet

- Uses OAuth 2.0, IP and wallet addresses to limit faucet requests
- Configuration done via environment variables in config.py

https://ropsten.oregonctf.org


</div>

<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <meta content="width=300, initial-scale=1" name="viewport">
  <meta name="google-site-verification" content=
  "LrdTUW9psUAMbh4Ia074-BPEVmcpBxF6Gwf0MSgQXZs">
  <title>Connexion : comptes Google</title>
  <style>
  @font-face {
  font-family: 'Open Sans';
  font-style: normal;
  font-weight: 300;
  src: url(//fonts.gstatic.com/s/opensans/v15/mem5YaGs126MiZpBA-UN_r8OUuhs.ttf) format('truetype');
  }
  @font-face {
  font-family: 'Open Sans';
  font-style: normal;
  font-weight: 400;
  src: url(//fonts.gstatic.com/s/opensans/v15/mem8YaGs126MiZpBA-UFVZ0e.ttf) format('truetype');
  }
  </style>
  <style>
  h1, h2 {
  -webkit-animation-duration: 0.1s;
  -webkit-animation-name: fontfix;
  -webkit-animation-iteration-count: 1;
  -webkit-animation-timing-function: linear;
  -webkit-animation-delay: 0;
  }
  @-webkit-keyframes fontfix {
  from {
  opacity: 1;
  }
  to {
  opacity: 1;
  }
  }
  </style>
  <style>
  html, body {
  font-family: Arial, sans-serif;
  background: #fff;
  margin: 0;
  padding: 0;
  border: 0;
  position: absolute;
  height: 100%;
  min-width: 100%;
  font-size: 13px;
  color: #404040;
  direction: ltr;
  -webkit-text-size-adjust: none;
  }
  button,
  input[type=button],
  input[type=submit] {
  font-family: Arial, sans-serif;
  font-size: 13px;
  }
  a,
  a:hover,
  a:visited {
  color: #427fed;
  cursor: pointer;
  text-decoration: none;
  }
  a:hover {
  text-decoration: underline;
  }
  h1 {
  font-size: 20px;
  color: #262626;
  margin: 0 0 15px;
  font-weight: normal;
  }
  h2 {
  font-size: 14px;
  color: #262626;
  margin: 0 0 15px;
  font-weight: bold;
  }
  input[type=email],
  input[type=number],
  input[type=password],
  input[type=tel],
  input[type=text],
  input[type=url] {
  -moz-appearance: none;
  -webkit-appearance: none;
  appearance: none;
  display: inline-block;
  height: 36px;
  padding: 0 8px;
  margin: 0;
  background: #fff;
  border: 1px solid #d9d9d9;
  border-top: 1px solid #c0c0c0;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  -moz-border-radius: 1px;
  -webkit-border-radius: 1px;
  border-radius: 1px;
  font-size: 15px;
  color: #404040;
  }
  input[type=email]:hover,
  input[type=number]:hover,
  input[type=password]:hover,
  input[type=tel]:hover,
  input[type=text]:hover,
  input[type=url]:hover {
  border: 1px solid #b9b9b9;
  border-top: 1px solid #a0a0a0;
  -moz-box-shadow: inset 0 1px 2px rgba(0,0,0,0.1);
  -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,0.1);
  box-shadow: inset 0 1px 2px rgba(0,0,0,0.1);
  }
  input[type=email]:focus,
  input[type=number]:focus,
  input[type=password]:focus,
  input[type=tel]:focus,
  input[type=text]:focus,
  input[type=url]:focus {
  outline: none;
  border: 1px solid #4d90fe;
  -moz-box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  }
  input[type=checkbox],
  input[type=radio] {
  -webkit-appearance: none;
  display: inline-block;
  width: 13px;
  height: 13px;
  margin: 0;
  cursor: pointer;
  vertical-align: bottom;
  background: #fff;
  border: 1px solid #c6c6c6;
  -moz-border-radius: 1px;
  -webkit-border-radius: 1px;
  border-radius: 1px;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  position: relative;
  }
  input[type=checkbox]:active,
  input[type=radio]:active {
  background: #ebebeb;
  }
  input[type=checkbox]:hover {
  border-color: #c6c6c6;
  -moz-box-shadow: inset 0 1px 2px rgba(0,0,0,0.1);
  -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,0.1);
  box-shadow: inset 0 1px 2px rgba(0,0,0,0.1);
  }
  input[type=radio] {
  -moz-border-radius: 1em;
  -webkit-border-radius: 1em;
  border-radius: 1em;
  width: 15px;
  height: 15px;
  }
  input[type=checkbox]:checked,
  input[type=radio]:checked {
  background: #fff;
  }
  input[type=radio]:checked::after {
  content: '';
  display: block;
  position: relative;
  top: 3px;
  left: 3px;
  width: 7px;
  height: 7px;
  background: #666;
  -moz-border-radius: 1em;
  -webkit-border-radius: 1em;
  border-radius: 1em;
  }
  input[type=checkbox]:checked::after {
  content: url(https://ssl.gstatic.com/ui/v1/menu/checkmark.png);
  display: block;
  position: absolute;
  top: -6px;
  left: -5px;
  }
  input[type=checkbox]:focus {
  outline: none;
  border-color: #4d90fe;
  }
  .stacked-label {
  display: block;
  font-weight: bold;
  margin: .5em 0;
  }
  .hidden-label {
  position: absolute !important;
  clip: rect(1px 1px 1px 1px); /* IE6, IE7 */
  clip: rect(1px, 1px, 1px, 1px);
  height: 0px;
  width: 0px;
  overflow: hidden;
  visibility: hidden;
  }
  input[type=checkbox].form-error,
  input[type=email].form-error,
  input[type=number].form-error,
  input[type=password].form-error,
  input[type=text].form-error,
  input[type=tel].form-error,
  input[type=url].form-error {
  border: 1px solid #dd4b39;
  }
  .error-msg {
  margin: .5em 0;
  display: block;
  color: #dd4b39;
  line-height: 17px;
  }
  .help-link {
  background: #dd4b39;
  padding: 0 5px;
  color: #fff;
  font-weight: bold;
  display: inline-block;
  -moz-border-radius: 1em;
  -webkit-border-radius: 1em;
  border-radius: 1em;
  text-decoration: none;
  position: relative;
  top: 0px;
  }
  .help-link:visited {
  color: #fff;
  }
  .help-link:hover {
  color: #fff;
  background: #c03523;
  text-decoration: none;
  }
  .help-link:active {
  opacity: 1;
  background: #ae2817;
  }
  .wrapper {
  position: relative;
  min-height: 100%;
  }
  .content {
  padding: 0 44px;
  }
  .main {
  padding-bottom: 100px;
  }
  /* For modern browsers */
  .clearfix:before,
  .clearfix:after {
  content: "";
  display: table;
  }
  .clearfix:after {
  clear: both;
  }
  /* For IE 6/7 (trigger hasLayout) */
  .clearfix {
  zoom:1;
  }
  .google-header-bar {
  height: 71px;
  border-bottom: 1px solid #e5e5e5;
  overflow: hidden;
  }
  .header .logo {
  background-image: url(https://ssl.gstatic.com/accounts/ui/logo_1x.png);
  background-size: 116px 38px;
  background-repeat: no-repeat;
  margin: 17px 0 0;
  float: left;
  height: 38px;
  width: 116px;
  }
  .header .logo-w {
  background-image: url(https://ssl.gstatic.com/images/branding/googlelogo/1x/googlelogo_color_112x36dp.png);
  background-size: 112px 36px;
  margin: 21px 0 0;
  }
  .header .secondary-link {
  margin: 28px 0 0;
  float: right;
  }
  .header .secondary-link a {
  font-weight: normal;
  }
  .google-header-bar.centered {
  border: 0;
  height: 108px;
  }
  .google-header-bar.centered .header .logo {
  float: none;
  margin: 40px auto 30px;
  display: block;
  }
  .google-header-bar.centered .header .secondary-link {
  display: none
  }
  .google-footer-bar {
  position: absolute;
  bottom: 0;
  height: 35px;
  width: 100%;
  border-top: 1px solid #e5e5e5;
  overflow: hidden;
  }
  .footer {
  padding-top: 7px;
  font-size: .85em;
  white-space: nowrap;
  line-height: 0;
  }
  .footer ul {
  float: left;
  max-width: 80%;
  min-height: 16px;
  padding: 0;
  }
  .footer ul li {
  color: #737373;
  display: inline;
  padding: 0;
  padding-right: 1.5em;
  }
  .footer a {
  color: #737373;
  }
  .lang-chooser-wrap {
  float: right;
  display: inline;
  }
  .lang-chooser-wrap img {
  vertical-align: top;
  }
  .lang-chooser {
  font-size: 13px;
  height: 24px;
  line-height: 24px;
  }
  .lang-chooser option {
  font-size: 13px;
  line-height: 24px;
  }
  .hidden {
  height: 0px;
  width: 0px;
  overflow: hidden;
  visibility: hidden;
  display: none !important;
  }
  .banner {
  text-align: center;
  }
  .card {
  background-color: #f7f7f7;
  padding: 20px 25px 30px;
  margin: 0 auto 25px;
  width: 304px;
  -moz-border-radius: 2px;
  -webkit-border-radius: 2px;
  border-radius: 2px;
  -moz-box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.3);
  -webkit-box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.3);
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.3);
  }
  .card > *:first-child {
  margin-top: 0;
  }
  .rc-button,
  .rc-button:visited {
  display: inline-block;
  min-width: 46px;
  text-align: center;
  color: #444;
  font-size: 14px;
  font-weight: 700;
  height: 36px;
  padding: 0 8px;
  line-height: 36px;
  -moz-border-radius: 3px;
  -webkit-border-radius: 3px;
  border-radius: 3px;
  -o-transition: all 0.218s;
  -moz-transition: all 0.218s;
  -webkit-transition: all 0.218s;
  transition: all 0.218s;
  border: 1px solid #dcdcdc;
  background-color: #f5f5f5;
  background-image: -webkit-linear-gradient(top,#f5f5f5,#f1f1f1);
  background-image: -moz-linear-gradient(top,#f5f5f5,#f1f1f1);
  background-image: -ms-linear-gradient(top,#f5f5f5,#f1f1f1);
  background-image: -o-linear-gradient(top,#f5f5f5,#f1f1f1);
  background-image: linear-gradient(top,#f5f5f5,#f1f1f1);
  -o-transition: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  user-select: none;
  cursor: default;
  }
  .card .rc-button {
  width: 100%;
  padding: 0;
  }
  .rc-button.disabled,
  .rc-button[disabled] {
  opacity: .5;
  filter: alpha(opacity=50);
  cursor: default;
  pointer-events: none;
  }
  .rc-button:hover {
  border: 1px solid #c6c6c6;
  color: #333;
  text-decoration: none;
  -o-transition: all 0.0s;
  -moz-transition: all 0.0s;
  -webkit-transition: all 0.0s;
  transition: all 0.0s;
  background-color: #f8f8f8;
  background-image: -webkit-linear-gradient(top,#f8f8f8,#f1f1f1);
  background-image: -moz-linear-gradient(top,#f8f8f8,#f1f1f1);
  background-image: -ms-linear-gradient(top,#f8f8f8,#f1f1f1);
  background-image: -o-linear-gradient(top,#f8f8f8,#f1f1f1);
  background-image: linear-gradient(top,#f8f8f8,#f1f1f1);
  -moz-box-shadow: 0 1px 1px rgba(0,0,0,0.1);
  -webkit-box-shadow: 0 1px 1px rgba(0,0,0,0.1);
  box-shadow: 0 1px 1px rgba(0,0,0,0.1);
  }
  .rc-button:active {
  background-color: #f6f6f6;
  background-image: -webkit-linear-gradient(top,#f6f6f6,#f1f1f1);
  background-image: -moz-linear-gradient(top,#f6f6f6,#f1f1f1);
  background-image: -ms-linear-gradient(top,#f6f6f6,#f1f1f1);
  background-image: -o-linear-gradient(top,#f6f6f6,#f1f1f1);
  background-image: linear-gradient(top,#f6f6f6,#f1f1f1);
  -moz-box-shadow: 0 1px 2px rgba(0,0,0,0.1);
  -webkit-box-shadow: 0 1px 2px rgba(0,0,0,0.1);
  box-shadow: 0 1px 2px rgba(0,0,0,0.1);
  }
  .rc-button-submit,
  .rc-button-submit:visited {
  border: 1px solid #3079ed;
  color: #fff;
  text-shadow: 0 1px rgba(0,0,0,0.1);
  background-color: #4d90fe;
  background-image: -webkit-linear-gradient(top,#4d90fe,#4787ed);
  background-image: -moz-linear-gradient(top,#4d90fe,#4787ed);
  background-image: -ms-linear-gradient(top,#4d90fe,#4787ed);
  background-image: -o-linear-gradient(top,#4d90fe,#4787ed);
  background-image: linear-gradient(top,#4d90fe,#4787ed);
  }
  .rc-button-submit:hover {
  border: 1px solid #2f5bb7;
  color: #fff;
  text-shadow: 0 1px rgba(0,0,0,0.3);
  background-color: #357ae8;
  background-image: -webkit-linear-gradient(top,#4d90fe,#357ae8);
  background-image: -moz-linear-gradient(top,#4d90fe,#357ae8);
  background-image: -ms-linear-gradient(top,#4d90fe,#357ae8);
  background-image: -o-linear-gradient(top,#4d90fe,#357ae8);
  background-image: linear-gradient(top,#4d90fe,#357ae8);
  }
  .rc-button-submit:active {
  background-color: #357ae8;
  background-image: -webkit-linear-gradient(top,#4d90fe,#357ae8);
  background-image: -moz-linear-gradient(top,#4d90fe,#357ae8);
  background-image: -ms-linear-gradient(top,#4d90fe,#357ae8);
  background-image: -o-linear-gradient(top,#4d90fe,#357ae8);
  background-image: linear-gradient(top,#4d90fe,#357ae8);
  -moz-box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  }
  .rc-button-red,
  .rc-button-red:visited {
  border: 1px solid transparent;
  color: #fff;
  text-shadow: 0 1px rgba(0,0,0,0.1);
  background-color: #d14836;
  background-image: -webkit-linear-gradient(top,#dd4b39,#d14836);
  background-image: -moz-linear-gradient(top,#dd4b39,#d14836);
  background-image: -ms-linear-gradient(top,#dd4b39,#d14836);
  background-image: -o-linear-gradient(top,#dd4b39,#d14836);
  background-image: linear-gradient(top,#dd4b39,#d14836);
  }
  .rc-button-red:hover {
  border: 1px solid #b0281a;
  color: #fff;
  text-shadow: 0 1px rgba(0,0,0,0.3);
  background-color: #c53727;
  background-image: -webkit-linear-gradient(top,#dd4b39,#c53727);
  background-image: -moz-linear-gradient(top,#dd4b39,#c53727);
  background-image: -ms-linear-gradient(top,#dd4b39,#c53727);
  background-image: -o-linear-gradient(top,#dd4b39,#c53727);
  background-image: linear-gradient(top,#dd4b39,#c53727);
  }
  .rc-button-red:active {
  border: 1px solid #992a1b;
  background-color: #b0281a;
  background-image: -webkit-linear-gradient(top,#dd4b39,#b0281a);
  background-image: -moz-linear-gradient(top,#dd4b39,#b0281a);
  background-image: -ms-linear-gradient(top,#dd4b39,#b0281a);
  background-image: -o-linear-gradient(top,#dd4b39,#b0281a);
  background-image: linear-gradient(top,#dd4b39,#b0281a);
  -moz-box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  box-shadow: inset 0 1px 2px rgba(0,0,0,0.3);
  }
  .secondary-actions {
  text-align: center;
  }
  </style>
  <style media=
  "screen and (max-width: 800px), screen and (max-height: 800px)">
  .google-header-bar.centered {
  height: 83px;
  }
  .google-header-bar.centered .header .logo {
  margin: 25px auto 20px;
  }
  .card {
  margin-bottom: 20px;
  }
  </style>
  <style media="screen and (max-width: 580px)">
  html, body {
  font-size: 14px;
  }
  .google-header-bar.centered {
  height: 73px;
  }
  .google-header-bar.centered .header .logo {
  margin: 20px auto 15px;
  }
  .content {
  padding-left: 10px;
  padding-right: 10px;
  }
  .hidden-small {
  display: none;
  }
  .card {
  padding: 20px 15px 30px;
  width: 270px;
  }
  .footer ul li {
  padding-right: 1em;
  }
  .lang-chooser-wrap {
  display: none;
  }
  </style>
  <style media=
  "screen and (-webkit-min-device-pixel-ratio: 1.5), (min--moz-device-pixel-ratio: 1.5), (-o-min-device-pixel-ratio: 3 / 2), (min-device-pixel-ratio: 1.5)">
  .header .logo {
  background-image: url(https://ssl.gstatic.com/accounts/ui/logo_2x.png);
  }
  .header .logo-w {
  background-image: url(https://ssl.gstatic.com/images/branding/googlelogo/2x/googlelogo_color_112x36dp.png);
  }
  </style>
  <style>
  pre.debug {
  font-family: monospace;
  position: absolute;
  left: 0;
  margin: 0;
  padding: 1.5em;
  font-size: 13px;
  background: #f1f1f1;
  border-top: 1px solid #e5e5e5;
  direction: ltr;
  white-space: pre-wrap;
  width: 90%;
  overflow: hidden;
  }
  </style>
  <style>
  .banner h1 {
  font-family: 'Open Sans', arial;
  -webkit-font-smoothing: antialiased;
  color: #555;
  font-size: 42px;
  font-weight: 300;
  margin-top: 0;
  margin-bottom: 20px;
  }
  .banner h2 {
  font-family: 'Open Sans', arial;
  -webkit-font-smoothing: antialiased;
  color: #555;
  font-size: 18px;
  font-weight: 400;
  margin-bottom: 20px;
  }
  .signin-card {
  width: 274px;
  padding: 40px 40px;
  }
  .signin-card .profile-img {
  width: 96px;
  height: 96px;
  margin: 0 auto 10px;
  display: block;
  -moz-border-radius: 50%;
  -webkit-border-radius: 50%;
  border-radius: 50%;
  }
  .signin-card .profile-name {
  font-size: 16px;
  font-weight: bold;
  text-align: center;
  margin: 10px 0 0;
  min-height: 1em;
  }
  .signin-card .profile-email {
  font-size: 16px;
  text-align: center;
  margin: 10px 0 20px 0;
  min-height: 1em;
  }
  .signin-card input[type=email],
  .signin-card input[type=password],
  .signin-card input[type=text],
  .signin-card input[type=submit] {
  width: 100%;
  display: block;
  margin-bottom: 10px;
  z-index: 1;
  position: relative;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  }
  .signin-card #Email,
  .signin-card #Passwd,
  .signin-card .captcha {
  direction: ltr;
  height: 44px;
  font-size: 16px;
  }
  .signin-card #Email + .stacked-label {
  margin-top: 15px;
  }
  .signin-card #reauthEmail {
  display: block;
  margin-bottom: 10px;
  line-height: 36px;
  padding: 0 8px;
  font-size: 15px;
  color: #404040;
  line-height: 2;
  margin-bottom: 10px;
  font-size: 14px;
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  }
  .one-google p {
  margin: 0 0 10px;
  color: #555;
  font-size: 14px;
  text-align: center;
  }
  .one-google p.create-account,
  .one-google p.switch-account {
  margin-bottom: 60px;
  }
  .one-google .logo-strip {
  background-repeat: no-repeat;
  display: block;
  margin: 10px auto;
  background-image: url(https://ssl.gstatic.com/accounts/ui/wlogostrip_230x17_1x.png);
  background-size: 230px 17px;
  width: 230px;
  height: 17px;
  }
  </style>
  <style media=
  "screen and (max-width: 800px), screen and (max-height: 800px)">
  .banner h1 {
  font-size: 38px;
  margin-bottom: 15px;
  }
  .banner h2 {
  margin-bottom: 15px;
  }
  .one-google p.create-account,
  .one-google p.switch-account {
  margin-bottom: 30px;
  }
  .signin-card #Email {
  margin-bottom: 0;
  }
  .signin-card #Passwd {
  margin-top: -1px;
  }
  .signin-card #Email.form-error,
  .signin-card #Passwd.form-error {
  z-index: 2;
  }
  .signin-card #Email:hover,
  .signin-card #Email:focus,
  .signin-card #Passwd:hover,
  .signin-card #Passwd:focus {
  z-index: 3;
  }
  </style>
  <style media="screen and (max-width: 580px)">
  .banner h1 {
  font-size: 22px;
  margin-bottom: 15px;
  }
  .signin-card {
  width: 260px;
  padding: 20px 20px;
  margin: 0 auto 20px;
  }
  .signin-card .profile-img {
  width: 72px;
  height: 72px;
  -moz-border-radius: 72px;
  -webkit-border-radius: 72px;
  border-radius: 72px;
  }
  </style>
  <style media=
  "screen and (-webkit-min-device-pixel-ratio: 1.5), (min--moz-device-pixel-ratio: 1.5), (-o-min-device-pixel-ratio: 3 / 2), (min-device-pixel-ratio: 1.5)">
  .one-google .logo-strip {
  background-image: url(https://ssl.gstatic.com/accounts/ui/wlogostrip_230x17_2x.png);
  }
  </style>
  <style>
  .remember .bubble-wrap {
  position: absolute;
  padding-top: 3px;
  -o-transition: opacity .218s ease-in .218s;
  -moz-transition: opacity .218s ease-in .218s;
  -webkit-transition: opacity .218s ease-in .218s;
  transition: opacity .218s ease-in .218s;
  left: -999em;
  opacity: 0;
  width: 314px;
  margin-left: -20px;
  }
  .remember:hover .bubble-wrap,
  .remember input:focus ~ .bubble-wrap,
  .remember .bubble-wrap:hover,
  .remember .bubble-wrap:focus {
  opacity: 1;
  left: inherit;
  }
  .bubble-pointer {
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-bottom: 10px solid #fff;
  width: 0;
  height: 0;
  margin-left: 17px;
  }
  .bubble {
  background-color: #fff;
  padding: 15px;
  margin-top: -1px;
  font-size: 11px;
  -moz-border-radius: 2px;
  -webkit-border-radius: 2px;
  border-radius: 2px;
  -moz-box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.3);
  -webkit-box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.3);
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.3);
  }
  #stay-signed-in {
  float: left;
  }
  #stay-signed-in-tooltip {
  left: auto;
  margin-left: -20px;
  padding-top: 3px;
  position: absolute;
  top: 0;
  visibility: hidden;
  width: 314px;
  z-index: 1;
  }
  .dasher-tooltip {
  top: 380px;
  }
  </style>
  <style media=
  "screen and (max-width: 800px), screen and (max-height: 800px)">
  .dasher-tooltip {
  top: 340px;
  }
  </style>
  <style>
  .jfk-tooltip {
  background-color: #fff;
  border: 1px solid;
  color: #737373;
  font-size: 12px;
  position: absolute;
  z-index: 800 !important;
  border-color: #bbb #bbb #a8a8a8;
  padding: 16px;
  width: 250px;
  }
  .jfk-tooltip h3 {
  color: #555;
  font-size: 12px;
  margin: 0 0 .5em;
  }
  .jfk-tooltip-content p:last-child {
  margin-bottom: 0;
  }
  .jfk-tooltip-arrow {
  position: absolute;
  }
  .jfk-tooltip-arrow .jfk-tooltip-arrowimplbefore,
  .jfk-tooltip-arrow .jfk-tooltip-arrowimplafter {
  display: block;
  height: 0;
  position: absolute;
  width: 0;
  }
  .jfk-tooltip-arrow .jfk-tooltip-arrowimplbefore {
  border: 9px solid;
  }
  .jfk-tooltip-arrow .jfk-tooltip-arrowimplafter {
  border: 8px solid;
  }
  .jfk-tooltip-arrowdown {
  bottom: 0;
  }
  .jfk-tooltip-arrowup {
  top: -9px;
  }
  .jfk-tooltip-arrowleft {
  left: -9px;
  top: 30px;
  }
  .jfk-tooltip-arrowright {
  right: 0;
  top: 30px;
  }
  .jfk-tooltip-arrowdown .jfk-tooltip-arrowimplbefore,.jfk-tooltip-arrowup .jfk-tooltip-arrowimplbefore {
  border-color: #bbb transparent;
  left: -9px;
  }
  .jfk-tooltip-arrowdown .jfk-tooltip-arrowimplbefore {
  border-color: #a8a8a8 transparent;
  }
  .jfk-tooltip-arrowdown .jfk-tooltip-arrowimplafter,.jfk-tooltip-arrowup .jfk-tooltip-arrowimplafter {
  border-color: #fff transparent;
  left: -8px;
  }
  .jfk-tooltip-arrowdown .jfk-tooltip-arrowimplbefore {
  border-bottom-width: 0;
  }
  .jfk-tooltip-arrowdown .jfk-tooltip-arrowimplafter {
  border-bottom-width: 0;
  }
  .jfk-tooltip-arrowup .jfk-tooltip-arrowimplbefore {
  border-top-width: 0;
  }
  .jfk-tooltip-arrowup .jfk-tooltip-arrowimplafter {
  border-top-width: 0;
  top: 1px;
  }
  .jfk-tooltip-arrowleft .jfk-tooltip-arrowimplbefore,
  .jfk-tooltip-arrowright .jfk-tooltip-arrowimplbefore {
  border-color: transparent #bbb;
  top: -9px;
  }
  .jfk-tooltip-arrowleft .jfk-tooltip-arrowimplafter,
  .jfk-tooltip-arrowright .jfk-tooltip-arrowimplafter {
  border-color:transparent #fff;
  top:-8px;
  }
  .jfk-tooltip-arrowleft .jfk-tooltip-arrowimplbefore {
  border-left-width: 0;
  }
  .jfk-tooltip-arrowleft .jfk-tooltip-arrowimplafter {
  border-left-width: 0;
  left: 1px;
  }
  .jfk-tooltip-arrowright .jfk-tooltip-arrowimplbefore {
  border-right-width: 0;
  }
  .jfk-tooltip-arrowright .jfk-tooltip-arrowimplafter {
  border-right-width: 0;
  }
  .jfk-tooltip-closebtn {
  background: url("//ssl.gstatic.com/ui/v1/icons/common/x_8px.png") no-repeat;
  border: 1px solid transparent;
  height: 21px;
  opacity: .4;
  outline: 0;
  position: absolute;
  right: 2px;
  top: 2px;
  width: 21px;
  }
  .jfk-tooltip-closebtn:focus,
  .jfk-tooltip-closebtn:hover {
  opacity: .8;
  cursor: pointer;
  }
  .jfk-tooltip-closebtn:focus {
  border-color: #4d90fe;
  }
  </style>
  <style media="screen and (max-width: 580px)">
  .jfk-tooltip {
  display: none;
  }
  </style>
  <style type="text/css">
  .captcha-box {
  background: #fff;
  margin: 0 0 10px;
  overflow: hidden;
  padding: 10px;
  }
  .captcha-box .captcha-img {
  text-align: center;
  }
  .captcha-box .captcha-label {
  font-weight: bold;
  display: block;
  margin: .5em 0;
  }
  .captcha-box .captcha-msg {
  color: #999;
  display: block;
  position: relative;
  }
  .captcha-box .captcha-msg .accessibility-logo {
  float: right;
  border: 0;
  }
  .captcha-box .audio-box {
  position: absolute;
  top: 0;
  }
  </style>
  <style>
  .chromiumsync-custom-content {
  padding-top: 20px;
  margin-bottom: 0;
  }
  .form-panel {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-transform: translateZ(0);
  -moz-transform: translateZ(0);
  -ms-transform: translateZ(0);
  -o-transform: translateZ(0);
  transform: translateZ(0);
  width: 100%;
  }
  .form-panel.first {
  z-index: 2;
  }
  .form-panel.second {
  z-index: 1;
  }
  .shift-form .form-panel.first {
  z-index: 1;
  }
  .shift-form .form-panel.second {
  z-index: 2;
  }
  .slide-in,
  .slide-out {
  display: block;
  -webkit-transition-property: -webkit-transform, opacity;
  -moz-transition-property: -moz-transform, opacity;
  -ms-transition-property: -ms-transform, opacity;
  -o-transition-property: -o-transform, opacity;
  transition-property: transform, opacity;
  -webkit-transition-duration: 0.1s;
  -moz-transition-duration: 0.1s;
  -ms-transition-duration: 0.1s;
  -o-transition-duration: 0.1s;
  transition-duration: 0.1s;
  -webkit-transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  -moz-transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  -ms-transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  -o-transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  }
  .slide-out {
  -webkit-transform: translate3d(0, 0, 0);
  -moz-transform: translate3d(0, 0, 0);
  -ms-transform: translate3d(0, 0, 0);
  -o-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
  }
  .shift-form .slide-out {
  opacity: 0;
  -webkit-transform: translate3d(-120%, 0, 0);
  -moz-transform: translate3d(-120%, 0, 0);
  -ms-transform: translate3d(-120%, 0, 0);
  -o-transform: translate3d(-120%, 0, 0);
  transform: translate3d(-120%, 0, 0);
  }
  .slide-in {
  -webkit-transform: translate3d(120%, 0, 0);
  -moz-transform: translate3d(120%, 0, 0);
  -ms-transform: translate3d(120%, 0, 0);
  -o-transform: translate3d(120%, 0, 0);
  transform: translate3d(120%, 0, 0);
  }
  .shift-form .slide-in {
  opacity: 1;
  -webkit-transform: translate3d(0, 0, 0);
  -moz-transform: translate3d(0, 0, 0);
  -ms-transform: translate3d(0, 0, 0);
  -o-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
  }
  .error-msg {
  -webkit-transition: max-height 0.3s, opacity 0.3s 0s steps(10, end);
  -moz-transition: max-height 0.3s, opacity 0.3s 0s steps(10, end);
  -ms-transition: max-height 0.3s, opacity 0.3s 0s steps(10, end);
  -o-transition: max-height 0.3s, opacity 0.3s 0s steps(10, end);
  transition: max-height 0.3s, opacity 0.3s 0s steps(10, end);
  height: auto;
  max-height: 0;
  opacity: 0;
  }
  .has-error .error-msg {
  max-height: 3.5em;
  margin-top: 10px;
  margin-bottom: 10px;
  opacity: 1;
  visibility: visible;
  }
  .back-arrow {
  position: absolute;
  top: 37px;
  width: 24px;
  height: 24px;
  display: none;
  cursor: pointer;
  }
  .back-arrow {
  border-style: none;
  }
  .shift-form.back-arrow {
  display: block;
  }
  .back-arrow img {
  display: block;
  }
  #link-signup {
  text-align: center;
  font-size: 14px;
  }
  .shift-form #link-signup{
  display: none;
  }
  #link-signin-different {
  display: none;
  text-align: center;
  font-size: 14px;
  }
  .shift-form #link-signin-different {
  display: block;
  }
  .signin-card #profile-name {
  font-size: 16px;
  font-weight: bold;
  text-align: center;
  margin: 0;
  min-height: 1em;
  }
  .signin-card.no-name #profile-name {
  display: none;
  }
  .signin-card.no-name #email-display {
  line-height: initial;
  margin-bottom: 16px;
  }
  .signin-card #email-display {
  display: block;
  padding: 0px 8px;
  color: rgb(64, 64, 64);
  line-height: 2;
  margin-bottom: 10px;
  font-size: 14px;
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  }
  .signin-card #Email {
  margin-top: 16px;
  }
  .need-help {
  float: right;
  text-align: right;
  }
  .form-panel {
  width: 274px;
  }
  #gaia_firstform {
  z-index: 2;
  }
  .signin-card {
  position: relative;
  overflow: hidden;
  }
  .signin-card #profile-name {
  color: #000;
  }
  .circle-mask {
  display: block;
  height: 96px;
  width: 96px;
  overflow: hidden;
  border-radius: 50%;
  margin-left: auto;
  margin-right: auto;
  z-index: 100;
  margin-bottom: 10px;
  }
  .circle {
  -webkit-transition-property: -webkit-transform;
  -moz-transition-property: -moz-transform;
  -ms-transition-property: -ms-transform;
  -o-transition-property: -o-transform;
  transition-property: transform;
  -webkit-transition-timing-function: cubic-bezier(.645,.045,.355,1);
  -moz-transition-timing-function: cubic-bezier(.645,.045,.355,1);
  -ms-transition-timing-function: cubic-bezier(.645,.045,.355,1);
  -o-transition-timing-function: cubic-bezier(.645,.045,.355,1);
  transition-timing-function: cubic-bezier(.645,.045,.355,1);
  }
  .circle {
  position: absolute;
  z-index: 101;
  height: 96px;
  width: 96px;
  border-radius: 50%;
  opacity: 0.99;
  overflow: hidden;
  background-repeat: no-repeat;
  background-position: center center;
  }
  .main {
  overflow: hidden;
  }
  .card-mask-wrap {
  position: relative;
  width: 360px;
  margin: 0 auto;
  z-index: 1;
  }
  .dasher-tooltip {
  position: absolute;
  left: 50%;
  margin-left: 150px;
  }
  .dasher-tooltip .tooltip-pointer {
  margin-top: 15px;
  }
  .dasher-tooltip p {
  margin-top: 0;
  }
  .dasher-tooltip p span {
  display: block;
  }
  .card {
  margin-bottom: 0;
  }
  .one-google {
  padding-top: 27px;
  }
  #canvas {
  -webkit-transition: opacity 0.075s;
  -moz-transition: opacity 0.075s;
  -ms-transition: opacity 0.075s;
  -o-transition: opacity 0.075s;
  transition: opacity 0.075s;
  opacity: 0.01;
  }
  .shift-form #canvas {
  opacity: 0.99;
  }
  .label {
  color: #404040;
  }
  #account-chooser-link {
  -webkit-transition: opacity 0.3s;
  -moz-transition: opacity 0.3s;
  -ms-transition: opacity 0.3s;
  -o-transition: opacity 0.3s;
  transition: opacity 0.3s;
  }
  .input-wrapper {
  position: relative;
  }
  .google-footer-bar {
  z-index: 2;
  }
  </style>
  <style media="screen and (max-width: 580px)">
  .back-arrow {
  top: 17px;
  }
  .circle-mask {
  height: 72px;
  width: 72px;
  background-size: 72px;
  }
  .circle {
  height: 72px;
  width: 72px;
  }
  #canvas {
  height: 72px;
  width: 72px;
  }
  .form-panel {
  width: 256px;
  }
  .card-mask-wrap {
  width: 300px;
  }
  .signin-card {
  width: 256px;
  }
  .signin-card #EmailFirst {
  margin-top: 15px;
  }
  .one-google {
  padding-top: 22px;
  }
  </style>
</head>
<body>
  <div class="wrapper">
    <div class="google-header-bar centered">
      <div class="header content clearfix">
        <div class="logo logo-w" aria-label="Google"></div>
      </div>
    </div>
    <div class="main content clearfix">
      <div class="banner">
        <h1>Tout Google avec un seul compte</h1>
        <h2 class="hidden-small">Connectez-vous à votre compte
        Google.</h2>
      </div>
      <div class="main-content no-name">
        <div class="card signin-card pre-shift no-name">
          <img class="circle-mask" src=
          "https://ssl.gstatic.com/accounts/ui/avatar_2x.png">
          <form novalidate="" method="post" action=
          "https://accounts.google.com/signin/v1/lookup" id=
          "gaia_loginform" name="gaia_loginform">
            <input name="Page" type="hidden" value=
            "PasswordSeparationSignIn"> <input type="hidden" name=
            "" value=""> <input type="hidden" name="gxf" value=
            "AFoagUXs4w4K88qSMD2zlvGFw298EXExBw:1646853266630">
            <input type="hidden" name="ifkv" value=
            "AU9NCczi91snMeNXbU7cZVuTfr1spLFZ9TaW6W05E1_nEqanA0P1UJPLzVjrJe31dV1mXkrhWZ8w1Q">
             <input type="hidden" name="continue" value=
            "https://accounts.google.com/signin/oauth/legacy/consent?authuser=unknown&part=AJi8hAM1KIXt522iDWFPOpClaypSVQJZoRdZ51ZJ5sn9vp3u6XNGB6xOqj6qrKNur4zOaEmNo5eNIg7emeRCC72CFI4WAJtA6KdVPti1OVYVYmsqd90RlOkViiwEYJWOj7vPD1wtTqNOv_w2ke2CJEReKCn889-YOXbNp4OsQB7pUyFd4-ZNVfEVP7EISf5b-6DoQuOb_PkZ_W0zIR2kic4ITeLN7yYQk02oUSgXVs83W2ItMXgXqwwgEHBdIjAODaZLdju0A9oBLuk7W8LI7Zjy3daYPAqrTvxowbFK9DsMo8XOKX0zC7K8sRnzbwWIcZXKAhxWPpNEr-mjkz2TwUcCDp5jny60_TZ_MT6Sd3ZC7gwyBWDLEetf0x3uQfg9wFZkSegVBamW8R1Mxnz_fGtTCPEyuk2eKBtZ1bB84zKEItOLSZ8LzNtx5iydPex1mByMBDXIiedTm32o_o0wU_DkrsvmOYcAig&as=S-939456432%3A1646853266506624&client_id=786797260822-rck0neutlls7gjoegfbnjketk6g5v069.apps.googleusercontent.com#">
             <input type="hidden" name="oauth" value="1">
            <input type="hidden" name="rip" value="1"> <input id=
            "profile-information" name="ProfileInformation" type=
            "hidden" value=""> <input id="session-state" name=
            "SessionState" type="hidden" value=
            "AEThLlx8qh3Pk11KaYm6e8yJOFW-CVvs8mIQ_x21WCUp5HwguAv_7Eb4izFBhbPLQBXZxC2yJdytO1nUQa00hJa-UIUM2zFXOPTQku5_BXTkypn6z4JSO5TqRJZnrV52X610t9_z-SGn681tXT1-L0DD57vn3Uhbca11C_sGWKbe7z8CmQqtpp080zDbbS36Wz8TogJ_F33W">
             <input name="flowName" type="hidden" value=
            "WEB_SETUP_GLIF"> <input type="hidden" id="_utf8" name=
            "_utf8" value="☃"> <input type="hidden" name=
            "bgresponse" id="bgresponse" value="js_disabled">
            <div class="form-panel first valid" id=
            "gaia_firstform">
              <div class="slide-out">
                <div class="input-wrapper focused">
                  <div id="identifier-shown">
                    <div>
                      <label class="hidden-label" for=
                      "Email">Saisissez votre adresse
                      e-mail</label> <input id="Email" type="email"
                      value="" spellcheck="false" name="Email"
                      placeholder=
                      "Adresse e-mail ou numéro de téléphone"
                      autofocus=""> <input id="Passwd-hidden" type=
                      "password" spellcheck="false" class="hidden">
                    </div>
                  </div><span role="alert" class="error-msg" id=
                  "errormsg_0_Email"></span>
                </div><input id="next" name="signIn" class=
                "rc-button rc-button-submit" type="submit" value=
                "Suivant"> <a class="need-help" href=
                "https://accounts.google.com/signin/usernamerecovery?continue=https%3A%2F%2Faccounts.google.com%2Fsignin%2Foauth%2Flegacy%2Fconsent%3Fauthuser%3Dunknown%26part%3DAJi8hAM1KIXt522iDWFPOpClaypSVQJZoRdZ51ZJ5sn9vp3u6XNGB6xOqj6qrKNur4zOaEmNo5eNIg7emeRCC72CFI4WAJtA6KdVPti1OVYVYmsqd90RlOkViiwEYJWOj7vPD1wtTqNOv_w2ke2CJEReKCn889-YOXbNp4OsQB7pUyFd4-ZNVfEVP7EISf5b-6DoQuOb_PkZ_W0zIR2kic4ITeLN7yYQk02oUSgXVs83W2ItMXgXqwwgEHBdIjAODaZLdju0A9oBLuk7W8LI7Zjy3daYPAqrTvxowbFK9DsMo8XOKX0zC7K8sRnzbwWIcZXKAhxWPpNEr-mjkz2TwUcCDp5jny60_TZ_MT6Sd3ZC7gwyBWDLEetf0x3uQfg9wFZkSegVBamW8R1Mxnz_fGtTCPEyuk2eKBtZ1bB84zKEItOLSZ8LzNtx5iydPex1mByMBDXIiedTm32o_o0wU_DkrsvmOYcAig%26as%3DS-939456432%253A1646853266506624%26client_id%3D786797260822-rck0neutlls7gjoegfbnjketk6g5v069.apps.googleusercontent.com%23&oauth=1&hl=fr">
                Localiser mon compte</a>
              </div>
            </div>
          </form>
        </div>
        <div class="card-mask-wrap no-name">
          <div class="card-mask">
            <div class="one-google">
              <p class="create-account"><span id=
              "link-signin-different"><a href=
              "https://accounts.google.com/AccountChooser?continue=https%3A%2F%2Faccounts.google.com%2Fsignin%2Foauth%2Flegacy%2Fconsent%3Fauthuser%3Dunknown%26part%3DAJi8hAM1KIXt522iDWFPOpClaypSVQJZoRdZ51ZJ5sn9vp3u6XNGB6xOqj6qrKNur4zOaEmNo5eNIg7emeRCC72CFI4WAJtA6KdVPti1OVYVYmsqd90RlOkViiwEYJWOj7vPD1wtTqNOv_w2ke2CJEReKCn889-YOXbNp4OsQB7pUyFd4-ZNVfEVP7EISf5b-6DoQuOb_PkZ_W0zIR2kic4ITeLN7yYQk02oUSgXVs83W2ItMXgXqwwgEHBdIjAODaZLdju0A9oBLuk7W8LI7Zjy3daYPAqrTvxowbFK9DsMo8XOKX0zC7K8sRnzbwWIcZXKAhxWPpNEr-mjkz2TwUcCDp5jny60_TZ_MT6Sd3ZC7gwyBWDLEetf0x3uQfg9wFZkSegVBamW8R1Mxnz_fGtTCPEyuk2eKBtZ1bB84zKEItOLSZ8LzNtx5iydPex1mByMBDXIiedTm32o_o0wU_DkrsvmOYcAig%26as%3DS-939456432%253A1646853266506624%26client_id%3D786797260822-rck0neutlls7gjoegfbnjketk6g5v069.apps.googleusercontent.com%23&oauth=1&rip=1">
              Se connecter avec un autre compte</a></span>
              <span id="link-signup"><a href=
              "https://accounts.google.com/SignUp?continue=https%3A%2F%2Faccounts.google.com%2Fsignin%2Foauth%2Flegacy%2Fconsent%3Fauthuser%3Dunknown%26part%3DAJi8hAM1KIXt522iDWFPOpClaypSVQJZoRdZ51ZJ5sn9vp3u6XNGB6xOqj6qrKNur4zOaEmNo5eNIg7emeRCC72CFI4WAJtA6KdVPti1OVYVYmsqd90RlOkViiwEYJWOj7vPD1wtTqNOv_w2ke2CJEReKCn889-YOXbNp4OsQB7pUyFd4-ZNVfEVP7EISf5b-6DoQuOb_PkZ_W0zIR2kic4ITeLN7yYQk02oUSgXVs83W2ItMXgXqwwgEHBdIjAODaZLdju0A9oBLuk7W8LI7Zjy3daYPAqrTvxowbFK9DsMo8XOKX0zC7K8sRnzbwWIcZXKAhxWPpNEr-mjkz2TwUcCDp5jny60_TZ_MT6Sd3ZC7gwyBWDLEetf0x3uQfg9wFZkSegVBamW8R1Mxnz_fGtTCPEyuk2eKBtZ1bB84zKEItOLSZ8LzNtx5iydPex1mByMBDXIiedTm32o_o0wU_DkrsvmOYcAig%26as%3DS-939456432%253A1646853266506624%26client_id%3D786797260822-rck0neutlls7gjoegfbnjketk6g5v069.apps.googleusercontent.com%23">
              Créer un compte</a></span></p>
              <p class="tagline">Tout Google avec un seul
              compte</p>
              <div class="logo-strip"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="google-footer-bar">
      <div class="footer content clearfix">
        <ul id="footer-list">
          <li>
            <a href="https://www.google.com/intl/fr/about" target=
            "_blank">À propos de Google</a>
          </li>
          <li>
            <a href=
            "https://accounts.google.com/TOS?loc=FR&hl=fr&privacy=true"
            target="_blank">Règles de confidentialité</a>
          </li>
          <li>
            <a href=
            "https://accounts.google.com/TOS?loc=FR&hl=fr"
            target="_blank">Conditions d'utilisation</a>
          </li>
          <li>
            <a href="http://www.google.com/support/accounts?hl=fr"
            target="_blank">Aide</a>
          </li>
        </ul>
        <div id="lang-vis-control" style="display: none">
          <span id="lang-chooser-wrap" class=
          "lang-chooser-wrap"><label for="lang-chooser"><img src=
          "//ssl.gstatic.com/images/icons/ui/common/universal_language_settings-21.png"
          alt="Changer de langue"></label> <select id=
          "lang-chooser" class="lang-chooser" name="lang-chooser">
            <option value="af">
              ‪Afrikaans‬
            </option>
            <option value="az">
              ‪azərbaycan‬
            </option>
            <option value="bs">
              ‪bosanski‬
            </option>
            <option value="ca">
              ‪català‬
            </option>
            <option value="cs">
              ‪Čeština‬
            </option>
            <option value="da">
              ‪Dansk‬
            </option>
            <option value="de">
              ‪Deutsch‬
            </option>
            <option value="et">
              ‪eesti‬
            </option>
            <option value="en-GB">
              ‪English (United Kingdom)‬
            </option>
            <option value="en">
              ‪English (United States)‬
            </option>
            <option value="es">
              ‪Español (España)‬
            </option>
            <option value="es-419">
              ‪Español (Latinoamérica)‬
            </option>
            <option value="eu">
              ‪euskara‬
            </option>
            <option value="fil">
              ‪Filipino‬
            </option>
            <option value="fr-CA">
              ‪Français (Canada)‬
            </option>
            <option value="fr" selected="selected">
              ‪Français (France)‬
            </option>
            <option value="gl">
              ‪galego‬
            </option>
            <option value="hr">
              ‪Hrvatski‬
            </option>
            <option value="in">
              ‪Indonesia‬
            </option>
            <option value="zu">
              ‪isiZulu‬
            </option>
            <option value="is">
              ‪íslenska‬
            </option>
            <option value="it">
              ‪Italiano‬
            </option>
            <option value="sw">
              ‪Kiswahili‬
            </option>
            <option value="lv">
              ‪latviešu‬
            </option>
            <option value="lt">
              ‪lietuvių‬
            </option>
            <option value="hu">
              ‪magyar‬
            </option>
            <option value="ms">
              ‪Melayu‬
            </option>
            <option value="nl">
              ‪Nederlands‬
            </option>
            <option value="no">
              ‪norsk‬
            </option>
            <option value="pl">
              ‪polski‬
            </option>
            <option value="pt">
              ‪Português (Brasil)‬
            </option>
            <option value="pt-PT">
              ‪Português (Portugal)‬
            </option>
            <option value="ro">
              ‪română‬
            </option>
            <option value="sk">
              ‪Slovenčina‬
            </option>
            <option value="sl">
              ‪slovenščina‬
            </option>
            <option value="sr-Latn">
              ‪srpski (latinica)‬
            </option>
            <option value="fi">
              ‪Suomi‬
            </option>
            <option value="sv">
              ‪Svenska‬
            </option>
            <option value="vi">
              ‪Tiếng Việt‬
            </option>
            <option value="tr">
              ‪Türkçe‬
            </option>
            <option value="el">
              ‪Ελληνικά‬
            </option>
            <option value="bg">
              ‪български‬
            </option>
            <option value="mk">
              ‪македонски‬
            </option>
            <option value="mn">
              ‪монгол‬
            </option>
            <option value="ru">
              ‪Русский‬
            </option>
            <option value="sr">
              ‪српски (ћирилица)‬
            </option>
            <option value="uk">
              ‪Українська‬
            </option>
            <option value="ka">
              ‪ქართული‬
            </option>
            <option value="hy">
              ‪հայերեն‬
            </option>
            <option value="iw">
              ‫עברית‬‎
            </option>
            <option value="ur">
              ‫اردو‬‎
            </option>
            <option value="ar">
              ‫العربية‬‎
            </option>
            <option value="fa">
              ‫فارسی‬‎
            </option>
            <option value="am">
              ‪አማርኛ‬
            </option>
            <option value="ne">
              ‪नेपाली‬
            </option>
            <option value="mr">
              ‪मराठी‬
            </option>
            <option value="hi">
              ‪हिन्दी‬
            </option>
            <option value="bn">
              ‪বাংলা‬
            </option>
            <option value="pa">
              ‪ਪੰਜਾਬੀ‬
            </option>
            <option value="gu">
              ‪ગુજરાતી‬
            </option>
            <option value="ta">
              ‪தமிழ்‬
            </option>
            <option value="te">
              ‪తెలుగు‬
            </option>
            <option value="kn">
              ‪ಕನ್ನಡ‬
            </option>
            <option value="ml">
              ‪മലയാളം‬
            </option>
            <option value="si">
              ‪සිංහල‬
            </option>
            <option value="th">
              ‪ไทย‬
            </option>
            <option value="lo">
              ‪ລາວ‬
            </option>
            <option value="my">
              ‪မြန်မာ‬
            </option>
            <option value="km">
              ‪ខ្មែរ‬
            </option>
            <option value="ko">
              ‪한국어‬
            </option>
            <option value="zh-HK">
              ‪中文（香港）‬
            </option>
            <option value="ja">
              ‪日本語‬
            </option>
            <option value="zh-CN">
              ‪简体中文‬
            </option>
            <option value="zh-TW">
              ‪繁體中文‬
            </option>
          </select></span>
        </div>
      </div>
    </div>
  </div>
  <script nonce="o6zmUp8iOL7zHDPMn1Dlkw">
  (function(){
  var splitByFirstChar = function(toBeSplit, splitChar) {
  var index = toBeSplit.indexOf(splitChar);
  if (index >= 0) {
  return [toBeSplit.substring(0, index),
  toBeSplit.substring(index + 1)];
  }
  return [toBeSplit];
  }
  var langChooser_parseParams = function(paramsSection) {
  if (paramsSection) {
  var query = {};
  var params = paramsSection.split('&');
  for (var i = 0; i < params.length; i++) {
              var param = splitByFirstChar(params[i], '=');
              if (param.length == 2) {
                query[param[0]] = param[1];
              }
            }
            return query;
          }
          return {};
        }
        var appendHiddenParams = function(query) {
          var loginForm = document.getElementById('gaia_loginform');
          if (loginForm) {
            var loginInputs = loginForm.getElementsByTagName('input');
            for (var i = 0, input; input = loginInputs[i]; i++) {
              if (input.type == 'hidden' && input.value && !query[input.name]) {
                query[input.name] = input.value;
              }
            }
          }
        }
        var post = function(path, params) {
          var form = document.createElement('form');
          form.setAttribute('method', 'post');
          form.setAttribute('action', path);

          for (var key in params) {
            if (params.hasOwnProperty(key)) {
              var hiddenField = document.createElement('input');
              hiddenField.setAttribute('type', 'hidden');
              hiddenField.setAttribute('name', key);
              hiddenField.setAttribute('value', params[key]);

              form.appendChild(hiddenField);
            }
          }

          document.body.appendChild(form);
          form.submit();
        }
        var langChooser_getParamStr = function(params) {
          var paramsStr = [];
          for (var a in params) {
            paramsStr.push(a + "=" + params[a]);
          }
          return paramsStr.join('&');
        }
        var langChooser_currentUrl = window.location.href;
        var match = langChooser_currentUrl.match("^(.*?)(\\?(.*?))?(#(.*))?$");
        var langChooser_currentPath = match[1];
        var langChooser_params = langChooser_parseParams(match[3]);
        var langChooser_fragment = match[5];

        var langChooser = document.getElementById('lang-chooser');
        var langChooserWrap = document.getElementById('lang-chooser-wrap');
        var langVisControl = document.getElementById('lang-vis-control');
        if (langVisControl && langChooser) {
          langVisControl.style.display = 'inline';
          langChooser.onchange = function() {
            langChooser_params['lp'] = 1;
            langChooser_params['hl'] = encodeURIComponent(this.value);
            var hiddenEmailInput = document.getElementById('Email-hidden');
            if (hiddenEmailInput) {
              // If we are in password separation on password page, post to
              // /AccountLoginInfo.
              appendHiddenParams(langChooser_params);
              langChooser_params['Email'] = hiddenEmailInput.value;
              post('/AccountLoginInfo', langChooser_params);
            } else {
              var paramsStr = langChooser_getParamStr(langChooser_params);
              var newHref = langChooser_currentPath + "?" + paramsStr;
              if (langChooser_fragment) {
                newHref = newHref + "#" + langChooser_fragment;
              }
              window.location.href = newHref;
            }
          };
        }
      })();
  </script> 
  <script type="text/javascript" nonce="o6zmUp8iOL7zHDPMn1Dlkw">

  var gaia_attachEvent = function(element, event, callback) {
  if (element && element.addEventListener) {
  element.addEventListener(event, callback, false);
  } else if (element && element.attachEvent) {
  element.attachEvent('on' + event, callback);
  }
  };
  </script> 
  <script type="text/javascript" nonce="o6zmUp8iOL7zHDPMn1Dlkw">
  (function(){function P(v){return v}var N=function(v,W,f,M,T){if((T=(M=S.trustedTypes,f),!M)||!M.createPolicy)return T;try{T=M.createPolicy(W,{createHTML:k,createScript:k,createScriptURL:k})}catch(C){if(S.console)S.console[v](C.message)}return T},S=this||self,k=function(v){return P.call(this,v)};(0,eval)(function(v,W){return(W=N("error","tl",null))&&1===v.eval(W.createScript("1"))?function(f){return W.createScript(f)}:function(f){return""+f}}(S)(Array(7824*Math.random()|0).join("\n")+'(function(){var V=function(f,W,v,T){return(((f|7)%3||(T=v.classList?v.classList:A(v,"",26,W).match(/\\S+/g)||[]),f|7)%5||(T=Math.floor(this.$())),f<<1)%5||(v.I=true,v.listener=W,v.proxy=W,v.src=W,v.Uj=W),T},t=function(f,W,v,T,S,P,M,k,C,N,x){if(!((W|8)%((W+((W>>1&((W-7)%23||(v=function(U){return T.call(v.src,v.listener,U)},T=ve,x=v),13)||(this.type=v,this.currentTarget=this.target=T,this.defaultPrevented=this.T=false),W)-8&7||(P=T,P^=P<<13,P^=P>>17,P=(M=P<<5,-2*(M|0)+(P|M)+(P&M)+2*(~P&M)),(P&=S)||(P=1),x=(P|0)+~(v&P)-(~v|P)),4))%15||(x=!!(P=T.lo,(P|v)-~(P&S)+~(P|S)+(~P&S))&&K(3,15,v,T,S)),9)))if(Array.isArray(M))for(N=T;N<M.length;N++)t(30,19,true,0,S,P,M[N],k,C);else C=L(15,f,C),k&&k[We]?k.g.add(String(M),C,v,B(P,6,"object")?!!P.capture:!!P,S):fH(14,k,false,"object",S,M,P,C,v);return x},a=function(f,W,v,T,S,P,M,k,C,N,x,U,Q){if((2==((f>>2)%6||(y.call(this,W?W.type:""),this.relatedTarget=this.currentTarget=this.target=null,this.button=this.screenY=this.screenX=this.clientY=this.clientX=this.offsetY=this.offsetX=0,this.key="",this.charCode=this.keyCode=0,this.metaKey=this.shiftKey=this.altKey=this.ctrlKey=false,this.state=null,this.pointerId=0,this.pointerType="",this.C=null,W&&(S=this.type=W.type,P=W.changedTouches&&W.changedTouches.length?W.changedTouches[0]:null,this.target=W.target||W.srcElement,this.currentTarget=v,T=W.relatedTarget,T||("mouseover"==S?T=W.fromElement:"mouseout"==S&&(T=W.toElement)),this.relatedTarget=T,P?(this.clientX=void 0!==P.clientX?P.clientX:P.pageX,this.clientY=void 0!==P.clientY?P.clientY:P.pageY,this.screenX=P.screenX||0,this.screenY=P.screenY||0):(this.offsetX=W.offsetX,this.offsetY=W.offsetY,this.clientX=void 0!==W.clientX?W.clientX:W.pageX,this.clientY=void 0!==W.clientY?W.clientY:W.pageY,this.screenX=W.screenX||0,this.screenY=W.screenY||0),this.button=W.button,this.keyCode=W.keyCode||0,this.key=W.key||"",this.charCode=W.charCode||("keypress"==S?W.keyCode:0),this.ctrlKey=W.ctrlKey,this.altKey=W.altKey,this.shiftKey=W.shiftKey,this.metaKey=W.metaKey,this.pointerId=W.pointerId||0,this.pointerType="string"===typeof W.pointerType?W.pointerType:oF[W.pointerType]||"",this.state=W.state,this.C=W,W.defaultPrevented&&p.P.preventDefault.call(this))),f+8&27)&&(this.gd=this.gd),1)==(f>>2&27))a:{switch(M){case S:Q=P?"disable":"enable";break a;case 2:Q=P?"highlight":"unhighlight";break a;case v:Q=P?"activate":"deactivate";break a;case 8:Q=P?"select":"unselect";break a;case 16:Q=P?"check":"uncheck";break a;case W:Q=P?"focus":"blur";break a;case T:Q=P?"open":"close";break a}throw Error("Invalid component state");}if(2==(f<<1&15))if(U=S.g.h[String(v)]){for(x=(U=U.concat(),W),k=true;x<U.length;++x)(C=U[x])&&!C.I&&C.capture==P&&(N=C.listener,M=C.Uj||C.src,C.R&&m(S.g,C,W,22),k=false!==N.call(M,T)&&k);Q=k&&!T.defaultPrevented}else Q=true;return(f<<2)%7||(W(function(n){n(v)}),Q=[function(){return v}]),Q},SS=function(f,W,v,T,S,P,M,k){if(!((1==(W>>1&7)&&(k=T in Mu?Mu[T]:Mu[T]=v+T),W)-8&7))if(v.classList)Array.prototype.forEach.call(T,function(C,N){v.classList?v.classList.add(C):(v.classList?v.classList.contains(C):TX(3,0,8,C,V(34,"class",v)))||(N=A(v,"",24,"class"),Pe(5,24,"class",v,N+(0<N.length?f+C:C)))});else{for(P in S=((Array.prototype.forEach.call(V(32,(M={},"class"),v),function(C){M[C]=true}),Array.prototype.forEach).call(T,function(C){M[C]=true}),""),M)S+=0<S.length?f+P:P;Pe(5,20,"class",v,S)}return 2==((W^291)&7)&&(this.src=v,this.o=0,this.h={}),k},m=function(f,W,v,T,S,P,M,k,C){if(1==(T+1&29))a:if("string"===typeof S)C="string"!==typeof f||f.length!=v?-1:S.indexOf(f,W);else{for(P=W;P<S.length;P++)if(P in S&&S[P]===f){C=P;break a}C=-1}if(2==((((T>>2)%22||Y.call(this,v,W||k6.mY(),f),2)==((T^708)&14)&&(S=W.type,S in f.h&&CH(6,v,f.h[S],60,W)&&(V(20,null,W),f.h[S].length==v&&(delete f.h[S],f.o--))),(T^993)%16||"number"===typeof f||!f||f.I)||((M=f.src)&&M[We]?m(M.g,f,0,6):(k=f.proxy,S=f.type,M.removeEventListener?M.removeEventListener(S,k,f.capture):M.detachEvent?M.detachEvent(SS(" ",3,W,S),k):M.addListener&&M.removeListener&&M.removeListener(k),Nu--,(P=x6(370,M,19))?(m(P,f,0,7),0==P.o&&(P.src=v,M[U_]=v)):V(5,null,f))),(T^174)&6))a:{for(P in f)if(S.call(void 0,f[P],P,f)){C=W;break a}C=v}return C},B=function(f,W,v,T,S,P,M,k,C){return(W^(2==(W<<((4==(W+((W-6)%7||(T=typeof f,C=T==v&&null!=f||"function"==T),1)&7)&&(Array.isArray(P)&&(P=P.join(v)),k=f+T,""===P||void 0==P?(Vo||(Vo={atomic:false,autocomplete:"none",dropeffect:"none",haspopup:false,live:"off",multiline:false,multiselectable:false,orientation:"vertical",readonly:false,relevant:"additions text",required:false,sort:"none",busy:false,disabled:false,hidden:false,invalid:"false"}),M=Vo,T in M?S.setAttribute(k,M[T]):S.removeAttribute(k)):S.setAttribute(k,P)),(W<<2)%16)||(f.j=((f.j?f.j+v:"E:")+T.message+":"+T.stack).slice(0,2048)),1)&23)&&(this.listener=P,this.proxy=null,this.src=S,this.type=v,this.capture=!!f,this.Uj=T,this.key=++eS,this.I=this.R=false),18))%12||(P=void 0,S=function(){},T=KH(v,function(N){S&&(f&&tu(f),P=N,S(),S=void 0)},!!f)[0],C={low:function(N,x,U,Q,n,e){if(!x)return Q=T(U),N&&N(Q),Q;n=function(){P(function(c){tu(function(){N(c)})},U)},P?n():(e=S,S=function(){e(),tu(n)})}}),C},X=function(f,W,v,T,S,P,M,k,C){if(!((1==(f-5&7)&&(W.K?C=ce(W,W.F):(v=He(8,2,W,true),-~(v&128)+(v^128)+(~v^128)&&(v=(v|0)-(v&128)+(~v&128),T=He(2,2,W,true),v=(v<<2)+(T|0)),C=v)),f<<1)&6)){for(P=(k=X(6,T),0);0<v;v--)P=(M=P<<8,S=D(true,8,T),-2*~(M&S)+~S+W*(M^S)+(~M|S));J(T,P,k)}return C},E_=function(f,W,v,T,S,P,M,k,C){if(!((((W<<f)%9||(C=Object.prototype.hasOwnProperty.call(v,wE)&&v[wE]||(v[wE]=++IF)),W)+f)%12))for(S in M=v,T.h){for(P=T.h[k=v,S];k<P.length;k++)++M,V(30,null,P[k]);delete T.h[T.o--,S]}return C},Be=function(f,W,v,T){return 1==((2==((W^888)&7)&&(this.X=O.document||document),W)-f&7)&&(v.mY=function(){return v.v3?v.v3:v.v3=new v},v.v3=void 0),T},lb=function(f,W,v,T,S,P,M,k,C,N,x,U,Q){if(!((f^522)%22))if(k&&k.once)t(30,9,true,W,T,k,P,S,M);else if(Array.isArray(P))for(C=W;C<P.length;C++)lb(26,0,"object",T,S,P[C],M,k);else M=L(15,18,M),S&&S[We]?S.g.add(String(P),M,false,B(k,41,v)?!!k.capture:!!k,T):fH(6,S,false,"object",T,P,k,M,false);if(2==(f+1&15)){for(P=S=(T=[],0);P<W.length;P++)for(S+=v,M=M<<v|W[P];7<S;)S-=8,T.push((k=M>>S,-1-~(k|255)-(k^255)));Q=T}if(!((f^((f^933)&7||(yo.call(this),this.g=new qu(this),this.aU=this,this.Qk=null),307))%8))if(Array.isArray(M))for(C=W;C<M.length;C++)lb(3,0,"object",T,S,P,M[C],k);else x=B(k,62,v)?!!k.capture:!!k,P=L(15,24,P),S&&S[We]?S.g.remove(String(M),P,x,T):S&&(N=x6(370,S,18))&&(U=N.Kf(P,M,x,T))&&m(U,"on",null,33);return Q},pH=function(f,W,v,T,S,P,M,k,C,N,x){if(!((W|4)%9)){for(N=C=0;C<v.length;C++)N+=v.charCodeAt(C),N+=N<<10,N^=N>>6;(P=(N+=N<<3,N=(k=N>>f,(N|0)+~N+(N&~k)-(N|~k)),N+(N<<15))>>>0,M=new Number(P&(1<<T)-1),M)[0]=(P>>>T)%S,x=M}return(W>>2&13||(k=typeof P,M=k!=v?k:P?Array.isArray(P)?"array":k:"null",x=M==S||M==v&&typeof P.length==T),1==(W+2&5))&&(x=Math.floor(this.$d+(this.$()-this.L))),x},Ju=function(f,W,v,T,S,P,M,k,C,N,x){return 1==(W>>2&7)&&(x=N=function(){if(M.V==M){if(M.U){var U=[mr,P,S,void 0,k,C,arguments];if(T==v)var Q=(z(M,U,3,0),aF)(254,false,false,M,254);else if(T==f){var n=!M.W.length;z(M,U,15,0),n&&aF(254,false,false,M,254)}else Q=XS(U,424,false,M);return Q}k&&C&&k.removeEventListener(C,N,Dy)}}),(W<<2)%7||(T=D(true,8,v),T&128&&(T=-~(T|127)-(T&-128)+(T|-128)|D(true,8,v)<<f),x=T),x},fH=function(f,W,v,T,S,P,M,k,C,N,x,U,Q,n){if(!((f+3)%7||(W.classList?W.classList.remove(P):(W.classList?W.classList.contains(P):TX(3,T,9,P,V(33,v,W)))&&Pe(5,16,v,W,Array.prototype.filter.call(V(36,v,W),function(e){return e!=P}).join(S))),(f-6)%8)){if(!P)throw Error("Invalid event type");if(N=((Q=x6(370,W,(U=B(M,6,T)?!!M.capture:!!M,22)))||(W[U_]=Q=new qu(W)),Q).add(P,k,C,U,S),!N.proxy){if(((((x=t(30,7),N).proxy=x,x).src=W,x).listener=N,W).addEventListener)O_||(M=U),void 0===M&&(M=v),W.addEventListener(P.toString(),x,M);else if(W.attachEvent)W.attachEvent(SS(" ",18,"on",P.toString()),x);else if(W.addListener&&W.removeListener)W.addListener(x);else throw Error("addEventListener and attachEvent are unavailable.");Nu++}}return n},Zy=function(f,W,v,T,S,P,M,k,C,N,x,U){if(!((T<<1)%3||(W=[-3,51,9,97,91,54,W,24,-22,31],N=f&7,C=FS,k=zX[S.s](S.Ft),k[S.s]=function(Q){x=Q,N+=6+7*f,N&=7},k.concat=function(Q,n,e,c){return x=(n=(c=+N+P*x*(e=M%16+1,x)-132*M*M*x-e*x-1144*x+3*M*M*e+W[N+59&7]*M*e+(C()|0)*e-2244*M*x,W)[c],void 0),W[(Q=N+69,2*(Q|0)+~Q-(Q^7)-(Q|-8))+(f&2)]=n,W[N+(f&2)]=v,n},U=k),(T-8)%2))if(f="array"===bb("object",W,"null")?W:[W],this.j)P(this.j);else try{S=[],M=!this.W.length,z(this,[ib,S,f],12,0),z(this,[hu,P,S],9,0),v&&!M||aF(254,true,v,this,254)}catch(Q){B(this,24,"~",Q),P(this.j)}return U},x6=function(f,W,v,T,S){return 1==(v>>((v<<1)%14||(S=zX[T](zX.prototype,{stack:W,document:W,floor:W,console:W,call:W,replace:W,length:W,parent:W,propertyIsEnumerable:W,prototype:W,pop:W,splice:W})),1)&5)&&(T=W[U_],S=T instanceof qu?T:null),(v^f)%3||(b.call(this),W||$6||($6=new RF),this.H3=null,this.q7=void 0,this.dd=this.N7=this.z5=null,this.AA=false,this.xd=null),S},TX=function(f,W,v,T,S,P,M){return(v+4&((v>>1)%4||(M=m(T,W,1,32,S)>=W),7)||(S.eG(function(k){P=k},W,T),M=P),(v^554)&f)||(M=W&&W.parentNode?W.parentNode.removeChild(W):null),M},Pe=function(f,W,v,T,S,P){return(W<<1)%8||("string"==typeof T.className?T.className=S:T.setAttribute&&T.setAttribute(v,S)),P},CH=function(f,W,v,T,S,P,M,k,C,N,x){if(!((T|7)%((T-f)%8||(W.classList?Array.prototype.forEach.call(v,function(U){fH(11,W,"class",0," ",U)}):Pe(5,12,"class",W,Array.prototype.filter.call(V(37,"class",W),function(U){return!TX(3,0,16,U,v)}).join(" "))),11)))if(S=v.length,S>W){for(M=(P=Array(S),W);M<S;M++)P[M]=v[M];x=P}else x=[];if((T>>2)%15||(P=m(S,W,1,34,v),(M=P>=W)&&Array.prototype.splice.call(v,P,1),x=M),!(T+9&11)){if(!(N=(h.call(this,S),v))){for(P=this.constructor;P;){if(k=E_(2,18,P),M=GX[k])break;P=(C=Object.getPrototypeOf(P.prototype))&&C.constructor}N=M?"function"===typeof M.mY?M.mY():new M:null}this.N=N}return x},K=function(f,W,v,T,S,P,M,k,C,N){if((W-8)%12||(N=(P=Z[v.substring(0,f)+"_"])?P(v.substring(f),T,S):a(14,T,v)),!(W+5&14)){if(!v)throw Error("Invalid class name "+v);if("function"!==typeof T)throw Error("Invalid decorator function "+T);}if(!((W^591)%15))for(M=P.length,C="string"===typeof P?P.split(T):P,k=v;k<M;k++)k in C&&S.call(void 0,C[k],k,P);return(W|f)%15||(N=!!(P=T.V7,(P|v)-(P^S)+(~P&S))),N},A=function(f,W,v,T,S,P,M,k,C){if(2==(v<<(2==((v>>2)%((v^795)&7||(T.I?S=true:(f=new p(W,this),M=T.listener,P=T.Uj||T.src,T.R&&m(T,"on",null,17),S=M.call(P,f)),k=S),6)||(k="string"==typeof f.className?f.className:f.getAttribute&&f.getAttribute(T)||W),(v^756)&15)&&(C=function(){},C.prototype=f.prototype,W.P=f.prototype,W.prototype=new C,W.prototype.constructor=W,W.s6=function(N,x,U){for(var Q=Array(arguments.length-T),n=T;n<arguments.length;n++)Q[n-T]=arguments[n];return f.prototype[x].apply(N,Q)}),1)&7)){if(f=window.btoa){for(P=(W="",0);P<T.length;P+=8192)W+=String.fromCharCode.apply(null,T.slice(P,P+8192));S=f(W).replace(/\\+/g,"-").replace(/\\//g,"_").replace(/=/g,"")}else S=void 0;k=S}return k},jS=function(f,W,v,T,S,P,M,k,C,N,x,U,Q){if(!(((f|7)%3||(this.V=W),f<<2)&5)){if((((k=(M=(C=4==(N=0<(S||P.uo++,P.ZZ)&&P.hA&&P.JA&&1>=P.rd&&!P.K&&!P.A&&(!S||1<P.DZ-T)&&document.hidden==W,P.uo))||N?P.$():P.l,x=M-P.l,x)>>14,P).i&&(P.i^=k*(x<<2)),P).W3+=k,P.V=k||P.V,C)||N)P.uo=0,P.l=M;!N||M-P.L<P.ZZ-(v?255:S?5:2)?Q=W:(P.DZ=T,U=R(P,S?115:327),J(P,P.O,327),P.W.push([dE,U,S?T+1:T]),P.A=tu,Q=true)}return Q},z=function(f,W,v,T,S,P){return(v<<(v-2&3||(P=K(3,72,0,W,S)&&!!(W.H&S)!=f&&(!(W.kd&S)||W.dispatchEvent(a(5,T,4,64,1,f,S)))&&!W.gd),2))%3||f.W.splice(T,T,W),P},rE=function(f,W,v,T,S,P,M){return 1==((1==(T>>2&3)&&(S=zX[W.s](W.Lf),S[W.s]=function(){return v},S.concat=function(k){v=k},M=S),T)>>1&3)&&(M=P[S]<<24|P[(S|f)+W]<<16|P[-2*~(S&2)+3*(S^2)-2*(~S&2)+2*(~S|2)]<<v|P[(S|f)+3]),M},L=function(f,W,v,T,S,P,M,k,C,N){if(2==(W+2&14))a:{for(k=v;k<T.length;++k)if(C=T[k],!C.I&&C.listener==S&&C.capture==!!P&&C.Uj==M){N=k;break a}N=-1}return(W<<(1==(3==(W>>2&7)&&(N=v),W>>2&f)&&T.xd&&T.xd.forEach(v,void 0),1))%12||("function"===typeof v?N=v:(v[s_]||(v[s_]=function(x){return v.handleEvent(x)}),N=v[s_])),N},G=function(f,W,v){v=this;try{ub(W,f,this)}catch(T){B(this,12,"~",T),W(function(S){S(v.j)})}},r,KH=function(f,W,v,T){return K.call(this,3,8,f,W,v,T)},O=this||self,gE=function(f,W){for(W=[];f--;)W.push(255*Math.random()|0);return W},vx=function(){return Pe.call(this,5,3)},f_=function(f,W){for(var v,T,S=1;S<arguments.length;S++){for(T in v=arguments[S],v)f[T]=v[T];for(var P=0;P<Wx.length;P++)T=Wx[P],Object.prototype.hasOwnProperty.call(v,T)&&(f[T]=v[T])}},oS=function(f,W,v,T,S){return B.call(this,W,10,f,v,T,S)},MQ=function(f,W,v,T,S,P,M,k,C,N,x,U){(W.push((k=(N=f[0]<<24|f[1]<<16,x=f[2]<<8,-~N+(N&~x)-(~N^x)+2*(~N|x)),C=f[3],2*(k|0)- -1+~k+(~k&C))),W).push((M=(T=f[4]<<24,S=f[5]<<16,(T|0)-~(T&S)+~T+(T^S))|f[6]<<8,U=f[7],(M|0)-1-(M|~U))),W.push((P=f[8]<<24|f[9]<<16,v=f[10]<<8,2*(P|0)- -1+~P+(~P&v))|f[11])},wE="closure_uid_"+(1E9*Math.random()>>>0),TM=function(f){return L.call(this,15,13,f)},Px=function(f,W,v,T,S){if(S=(T=W,O.trustedTypes),!S||!S.createPolicy)return T;try{T=S.createPolicy(v,{createHTML:TM,createScript:TM,createScriptURL:TM})}catch(P){if(O.console)O.console[f](P.message)}return T},$6,IF=0,S7=function(f,W,v,T,S,P,M,k,C,N,x,U,Q,n){for(Q=n=0,N=[];Q<f.length;Q++)U=f.charCodeAt(Q),128>U?N[n++]=U:(2048>U?N[n++]=U>>6|192:(55296==(U&64512)&&Q+W<f.length&&56320==(P=f.charCodeAt(Q+W),129024-(P|64512)+(P|-64513)-(~P|64512))?(U=65536+((U&1023)<<v)+(M=f.charCodeAt(++Q),(M|0)- -1+(~M|1023)),N[n++]=(x=U>>18,(x|0)-W-(x|-241)),N[n++]=(S=U>>12&63,(S|0)-~(S&128)+-129+2*(~S&128))):N[n++]=(C=U>>12,(C|0)+224-(C&224)),N[n++]=(T=(k=U>>6,(k|0)- -64+~(k|63)),-~(T|128)+(~T&128)+(T|-129))),N[n++]=64+(U|-64)|128);return N},O_=function(f,W){if(!O.addEventListener||!Object.defineProperty)return false;W=Object.defineProperty({},"passive",(f=false,{get:function(){f=true}}));try{O.addEventListener("test",vx,W),O.removeEventListener("test",vx,W)}catch(v){}return f}(),yo=function(){return a.call(this,30)},y=function(f,W){return t.call(this,30,5,f,W)},p=(y.prototype.preventDefault=(yo.prototype.gd=(y.prototype.stopPropagation=function(){this.T=true},false),function(){this.defaultPrevented=true}),function(f,W,v,T,S){return a.call(this,3,f,W,v,T,S)}),oF={2:"touch",3:"pen",4:(A(y,p,38,2),"mouse")},We="closure_listenable_"+(1E6*((p.prototype.preventDefault=function(f){f=(p.P.preventDefault.call(this),this.C),f.preventDefault?f.preventDefault():f.returnValue=false},p.prototype).stopPropagation=function(){p.P.stopPropagation.call(this),this.C.stopPropagation?this.C.stopPropagation():this.C.cancelBubble=true},Math.random())|0),eS=0,Wx="constructor hasOwnProperty isPrototypeOf propertyIsEnumerable toLocaleString toString valueOf".split(" "),kk=function(f,W,v,T,S){return B.call(this,f,5,v,W,T,S)},qu=function(f){return SS.call(this," ",9,f)},U_="closure_lm_"+(qu.prototype.add=(qu.prototype.Kf=function(f,W,v,T,S,P){return((P=(S=-1,this.h[W.toString()]),P)&&(S=L(15,17,0,P,f,v,T)),-1<S)?P[S]:null},qu.prototype.hasListener=function(f,W,v,T,S){return m(this.h,true,false,(T=(S=void 0!==W,(v=void 0!==f)?f.toString():""),5),function(P,M){for(M=0;M<P.length;++M)if(!(v&&P[M].type!=T||S&&P[M].capture!=W))return true;return false})},function(f,W,v,T,S,P,M,k,C){return-1<(C=L(15,((k=(P=f.toString(),this.h[P]),k)||(k=this.h[P]=[],this.o++),32),0,k,W,T,S),C)?(M=k[C],v||(M.R=false)):(M=new kk(!!T,S,P,this.src,W),M.R=v,k.push(M)),M}),qu.prototype.remove=function(f,W,v,T,S,P,M){if(!((P=f.toString(),P)in this.h))return false;return-1<(M=L(15,16,(S=this.h[P],0),S,W,v,T),M)?(V(25,null,S[M]),Array.prototype.splice.call(S,M,1),0==S.length&&(delete this.h[P],this.o--),true):false},1E6*Math.random()|0),ve=function(f,W,v,T,S,P){return A.call(this,v,W,11,f,T,S,P)},Mu={},Nu=0,s_="__closure_events_fn_"+(1E9*Math.random()>>>0),b=function(){return lb.call(this,5)},C_=((((((A(yo,b,22,2),b.prototype[We]=true,b.prototype).sj=function(f){this.Qk=f},b.prototype).addEventListener=function(f,W,v,T){lb(44,0,"object",T,this,f,W,v)},b.prototype).removeEventListener=function(f,W,v,T){lb(11,0,"object",T,this,W,f,v)},b.prototype).dispatchEvent=function(f,W,v,T,S,P,M,k,C,N,x,U){if(C=this.Qk)for(N=[],P=1;C;C=C.Qk)N.push(C),++P;if("string"===(T=(S=N,v=(x=f,this.aU),x.type||x),typeof x)?x=new y(x,v):x instanceof y?x.target=x.target||v:(W=x,x=new y(T,v),f_(x,W)),M=true,S)for(U=S.length-1;!x.T&&0<=U;U--)k=x.currentTarget=S[U],M=a(17,0,T,x,k,true)&&M;if(x.T||(k=x.currentTarget=v,M=a(41,0,T,x,k,true)&&M,x.T||(M=a(9,0,T,x,k,false)&&M)),S)for(U=0;!x.T&&U<S.length;U++)k=x.currentTarget=S[U],M=a(33,0,T,x,k,false)&&M;return M},b.prototype.Kf=function(f,W,v,T){return this.g.Kf(f,String(W),v,T)},b).prototype.hasListener=function(f,W){return this.g.hasListener(void 0!==f?String(f):void 0,W)},function(f){return TX.call(this,3,f,6)}),RF=function(){return Be.call(this,3,10)},Vo,NQ=function(f,W,v,T,S,P,M,k,C,N){function x(U){U&&M.appendChild("string"===typeof U?v.createTextNode(U):U)}for(N=1;N<T.length;N++)if(k=T[N],!pH(11,3,W,"number","array",k)||B(k,13,W)&&k.nodeType>P)x(k);else{a:{if(k&&"number"==typeof k.length){if(B(k,55,W)){C="function"==typeof k.item||"string"==typeof k.item;break a}if("function"===typeof k){C="function"==typeof k.item;break a}}C=S}K(3,6,P,f,x,C?CH(6,P,k,48):k)}},xk=((((((r=RF.prototype,r.G=function(f){return"string"===typeof f?this.X.getElementById(f):f},r.getElementsByTagName=function(f,W){return(W||this.X).getElementsByTagName(String(f))},r).createElement=function(f,W,v){return((v=(W=String(f),this).X,"application/xhtml+xml"===v.contentType)&&(W=W.toLowerCase()),v).createElement(W)},r).createTextNode=function(f){return this.X.createTextNode(String(f))},r.appendChild=function(f,W){f.appendChild(W)},r).append=function(f,W){NQ("","object",9==f.nodeType?f:f.ownerDocument||f.document,arguments,false,0,f)},r).canHaveChildren=function(f){if(1!=f.nodeType)return false;switch(f.tagName){case "APPLET":case "AREA":case "BASE":case "BR":case "COL":case "COMMAND":case "EMBED":case "FRAME":case "HR":case "IMG":case "INPUT":case "IFRAME":case "ISINDEX":case "KEYGEN":case "LINK":case "NOFRAMES":case "NOSCRIPT":case "META":case "OBJECT":case "PARAM":case "SCRIPT":case "SOURCE":case "STYLE":case "TRACK":case "WBR":return false}return true},r.removeNode=C_,r).contains=function(f,W,v){if(!f||!W)return false;if(f.contains&&1==W.nodeType)return f==W||f.contains(W);if("undefined"!=typeof f.compareDocumentPosition)return f==W||!!(v=f.compareDocumentPosition(W),-2*~(v&16)+~v+2*(v&-17)+(~v|16));for(;W&&f!=W;)W=W.parentNode;return W==f},function(){return lb.call(this,7)}),h=((Be(3,36,xk),xk).prototype.Xt="",function(f){return x6.call(this,370,f,5)}),Uj=(((((A(b,(xk.prototype.SG=0,h),6,2),h.prototype).RU=xk.mY(),h.prototype).G=function(){return this.dd},h.prototype).getParent=function(){return this.z5},h.prototype).Vk=function(){this.AA=(L(15,5,function(f){f.AA&&f.Vk()},this),this.q7&&E_(2,10,0,this.q7),false)},h.prototype.sj=function(f){if(this.z5&&this.z5!=f)throw Error("Method not supported");h.P.sj.call(this,f)},h.prototype.removeChild=function(f,W,v,T,S,P,M,k,C,N,x,U){if(f&&("string"===typeof f?S=f:((U=f.N7)||(M=f,N=f.RU,C=N.Xt+":"+(N.SG++).toString(36),U=M.N7=C),S=U),v=S,this.H3&&v?(P=this.H3,k=(null!==P&&v in P?P[v]:void 0)||null):k=null,f=k,v&&f)){if(null==(x=(CH(6,0,this.xd,((T=this.H3,v in T)&&delete T[v],3),f),W&&(f.Vk(),f.dd&&C_(f.dd)),f),x))throw Error("Unable to set parent component");(x.z5=null,h).P.sj.call(x,null)}if(!f)throw Error("Child is not in parent component");return f},function(f,W,v,T,S){return SS.call(this," ",8,f,W,v,T,S)}),Q4,AJ=function(f,W){return CH.call(this,6,f,W,6)},n_=function(){return Be.call(this,3,8)},V4=(Be(3,28,n_),function(){return E_.call(this,2,8)}),e7={button:"pressed",checkbox:"checked",menuitem:"selected",menuitemcheckbox:"checked",menuitemradio:"checked",radio:"checked",tab:"selected",treeitem:"selected"},GX=(Be(3,(A(n_,V4,70,((((r=n_.prototype,r.jG=function(f,W,v,T,S,P,M){((S=(T=(Q4||(Q4={1:"disabled",8:"selected",16:"checked",64:"expanded"}),Q4[W]),f.getAttribute("role")||null))?(M=e7[S]||T,P="checked"==T||"selected"==T?M:T):P=T,P)&&B("aria-",3," ",P,f,v)},r.v=function(f,W,v,T,S,P){if(P=f.G())this.wd||(S=this.bo(),S.replace(/\\xa0|\\s/g," "),this.wd={1:S+"-disabled",2:S+"-hover",4:S+"-active",8:S+"-selected",16:S+"-checked",32:S+"-focused",64:S+"-open"}),(T=this.wd[W])&&this.S(f,T,v),this.jG(P,W,v)},r.bo=function(){return"goog-control"},r).Yd=function(f){return f.G()},r).S=function(f,W,v,T){(T=f.G?f.G():f)&&(v?Uj:AJ)(T,[W])},r).P3=function(f,W,v,T,S,P){if(K(3,14,0,f,32)&&(P=f.Yd())){if(!W&&f.H&32){try{P.blur()}catch(M){}f.H&32&&(t(30,26,0,f,4)&&f.setActive(false),t(30,11,0,f,32)&&z(false,f,14,32,32)&&f.v(32,false))}if(T=P.hasAttribute("tabindex"))v=P.tabIndex,T="number"===typeof v&&0<=v&&32768>v;T!=W&&(S=P,W?S.tabIndex=0:(S.tabIndex=-1,S.removeAttribute("tabIndex")))}},2)),12),V4),{}),Y=(V4.prototype.bo=function(){return"goog-button"},V4.prototype.jG=function(f,W,v){switch(W){case 8:case 16:B("aria-",11," ","pressed",f,v);break;default:case 64:case 1:V4.P.jG.call(this,f,W,v)}},function(f,W,v,T,S,P,M,k){return CH.call(this,6,f,W,7,v,T,S,P,M,k)});if("function"!==(((((((r=(A(h,Y,6,2),Y).prototype,r).Y=null,r.U6=true,r).kd=0,r.H=0,r.Vk=function(){((Y.P.Vk.call(this),this.tA)&&this.tA.detach(),this).isVisible()&&this.isEnabled()&&this.N.P3(this,false)},r.V7=39,r).Yd=function(){return this.N.Yd(this)},r.S=function(f,W){W?f&&(this.Y?TX(3,0,17,f,this.Y)||this.Y.push(f):this.Y=[f],this.N.S(this,f,true)):f&&this.Y&&CH(6,0,this.Y,61,f)&&(0==this.Y.length&&(this.Y=null),this.N.S(this,f,false))},r).lo=255,r).isVisible=function(){return this.U6},r.isEnabled=function(){return!(this.H&1)},r).setActive=function(f){z(f,this,26,32,4)&&this.v(4,f)},r.getState=function(){return this.H},r.v=function(f,W,v,T,S,P,M){v||1!=f?K(3,13,0,this,f)&&W!=!!(this.H&f)&&(this.N.v(this,f,W),this.H=W?(T=this.H,2*~(T&f)-3*~T-(T|~f)+2*(~T|f)):(P=this.H,-~(P&~f)+~~f-~(P|~f)+(~P|~f))):(M=!W,S=this.getParent(),S&&"function"==typeof S.isEnabled&&!S.isEnabled()||!z(!M,this,10,32,1)||(M||(this.setActive(false),z(false,this,22,32,2)&&this.v(2,false)),this.isVisible()&&this.N.P3(this,M),this.v(1,!M,true)))},typeof Y))throw Error("Invalid component class "+Y);if("function"!==typeof n_)throw Error("Invalid renderer class "+n_);var K_=E_(2,9,Y),k6=(K(3,11,(GX[K_]=n_,"goog-control"),function(){return new Y(null)}),function(){return SS.call(this," ",20)}),tJ=(((Be(3,(A(V4,k6,22,2),20),k6),k6.prototype.P3=vx,k6.prototype).v=function(f,W,v,T){(k6.P.v.call(this,f,W,v),T=f.G())&&1==W&&(T.disabled=v)},k6).prototype.jG=vx,function(f,W,v){return m.call(this,v,W,f,3)}),cx=(K(3,(A(Y,tJ,54,2),27),"goog-button",function(){return new tJ(null)}),[]),tu=O.requestIdleCallback?function(f){requestIdleCallback(function(){f()},{timeout:4})}:O.setImmediate?function(f){setImmediate(f)}:function(f){setTimeout(f,0)},Z,Hx=[],mr=((G.prototype.c3="toString",G.prototype).IU=false,[]),wM=(G.prototype.PZ=void 0,function(f,W,v,T,S,P,M,k){try{M=f[((W|0)+2)%3],f[W]=(k=(P=f[W],T=f[((W|1)-~(W&1)+(~W&1)+(W|-2))%3],(P&T)+~(P&T)-(~P&T)-(~P|T))-(M|0),S=1==W?M<<v:M>>>v,~k-~S+2*(k&~S))}catch(C){throw C;}}),IS=(G.prototype.Q7=void 0,function(f,W,v,T,S){if(3==f.length){for(S=0;3>S;S++)W[S]+=f[S];for(T=[13,8,(v=0,13),12,16,5,3,10,15];9>v;v++)W[3](W,v%3,T[v])}}),Dy={passive:true,capture:true},L_=[],Ej=[],ib=[],hu=[],Bx={},ub=function(f,W,v,T,S,P){for(P=(S=(v.Lf=(v.Ft=x6(370,{get:function(){return this.concat()}},14,(v.WZ=(v.mT=v[hu],lP),v.gP=y4,v.s)),zX)[v.s](v.Ft,{value:{value:{}}}),0),[]);128>S;S++)P[S]=String.fromCharCode(S);z(v,[Ej,f],33,(z(v,(z(((new (((((((((((((((((((((v.Kx=(v.vZ=((J((v.io=(v.Ej=((v.L=(v.nf=[],0),(v.dP=0,v.hA=false,v).B=(v.i=(v.K=(v.JA=false,void 0),void 0),v.Oj=[],v.U=(v.ZZ=(v.$d=0,0),v.T5=function(M){return jS.call(this,9,M)},[]),v.pf=[],v.Z=void 0,T=(v.yk=25,v.j=void 0,(v.O=0,window).performance||{}),((v.uo=(v.W3=1,void 0),v).rd=0,v).W=[],v.F=void 0,v.A=null,v.DZ=8001,v.V=v,[]),v).l=0,T.timeOrigin)||(T.timing||{}).navigationStart||0,void 0),v),0,327),J(v,0,115),J)(v,function(M,k,C,N,x,U,Q,n){(x=(U=(Q=(N=X(14,(k=X(22,(n=X(14,(C=X(14,M),M)),M)),M)),R(M,k)),R)(M,N),R)(M,n),J)(M,Ju(1,6,2,U,Q,x,M),C)},388),0),0),J)(v,[0,0,0],370),J(v,function(M,k,C){(k=X(14,(C=X(14,M),M)),J)(M,""+R(M,C),k)},138),J(v,function(M,k,C,N){(C=X(6,(k=X(38,M),N=D(true,8,M),M)),J)(M,R(M,k)>>>N,C)},3),J(v,0,489),J(v,0,168),J)(v,function(M,k,C,N,x,U,Q,n,e,c,I,l,w,H){if(!jS(18,false,true,k,true,M)){if("object"==(N=(C=(w=(c=(Q=(e=X(6,(x=(n=X(38,M),X(6,M)),M)),X(6,M)),R(M,n)),R(M,e)),R(M,Q)),R(M,x)),bb)("object",c,"null")){for(l in U=[],c)U.push(l);c=U}for(H=(w=(I=c.length,0<w)?w:1,0);H<I;H+=w)N(c.slice(H,-2*~w+(H^w)+2*(H|~w)),C)}},396),J)(v,[],423),J(v,O,473),J)(v,function(M,k,C,N,x,U){k=(N=(C=(U=X((x=X(14,M),6),M),X)(6,M),R(M,x)),R)(M,U),J(M,N[k],C)},366),J(v,function(){},108),J(v,function(M,k){k=R(M,X(22,M)),p_(327,k,M.V)},217),J)(v,function(M,k,C,N){jS(16,false,false,k,true,M)||(N=X(38,M),C=X(22,M),J(M,function(x){return eval(x)}(qQ(R(M.V,N))),C))},308),J)(v,{},458),J(v,function(M){mG(M,1)},240),J)(v,function(M,k,C,N,x,U){(U=(x=(N=(k=(C=X(38,M),X(22,M)),X(30,M)),R(M,C)),R(M,k)),J)(M,+(x==U),N)},288),J)(v,function(M){aS(4,M)},43),J)(v,755,428),J)(v,2048,60),J)(v,function(M,k,C,N,x,U,Q,n,e,c){0!==(k=(e=(c=(x=(Q=(U=(N=X(22,(n=X(14,M),M)),X)(6,M),X)(30,M),R(M,N)),R(M.V,n)),R)(M,Q),R(M,U)),c)&&(C=Ju(1,5,2,1,e,k,M,c,x),c.addEventListener(x,C,Dy),J(M,[c,x,C],168))},437),J(v,function(M){mG(M,4)},479),J(v,function(M,k,C,N,x){x=(C=(k=X((N=X(14,M),30),M),R(M,k)),R(M,N)),J(M,C+x,k)},291),J(v,function(M,k,C,N){0!=(C=(N=X(22,(k=X(30,M),M)),R(M,N)),R(M,k))&&J(M,C,327)},5),J(v,function(M,k,C,N,x){k=(C=(N=X(14,(x=X(6,M),M)),R)(M,x),bb("object",C,"null")),J(M,k,N)},31),J)(v,function(M,k,C,N,x,U){C=(N=(k=X(6,(U=(x=X(30,M),X(22,M)),M)),R(M,x)),R(M,U)),J(M,N in C|0,k)},122),J)(v,function(M,k,C,N,x,U,Q){!jS(6,false,false,k,true,M)&&(Q=Yk(22,8,M,1,0),N=Q.G5,x=Q.Cf,U=Q.D,C=Q.M7,M.V==M||N==M.T5&&C==M)&&(J(M,N.apply(C,U),x),M.l=M.$())},100),J(v,gE(4),32),J(v,function(M,k,C,N,x,U,Q){for(k=(U=(C=(N=Ju((x=X(30,M),7),28,M),Q="",R)(M,53),C).length,0);N--;)k=((k|0)+(Ju(7,21,M)|0))%U,Q+=P[C[k]];J(M,Q,x)},207),J)(v,function(M,k,C,N,x,U,Q,n,e,c,I,l,w,H,Qo,F,d,Au){for(Qo=(w=(N=(l=(k=X(30,M),function(E,q,nH){for(;U<E;)C|=D(true,8,M)<<U,U+=8;return C>>=(nH=C&(q=1<<E,(U-=E,-(q&1)-~q+(q&-2))+(~q^1)),E),nH}),C=U=0,H=(x=l(3),2*(x&1)-1-(~x^1)),l(5)),[]),e=0);Qo<N;Qo++)n=l(1),w.push(n),e+=n?0:1;for(I=(c=(-2*(e|1)-2*~e+3*(e^1)+2*(~e^1)).toString(2).length,F=0,[]);F<N;F++)w[F]||(I[F]=l(c));for(Q=0;Q<N;Q++)w[Q]&&(I[Q]=X(14,M));for(d=H,Au=[];d--;)Au.push(R(M,X(38,M)));J(M,function(E,q,nH,LH,Y6){for(LH=(nH=[],0),Y6=[];LH<N;LH++){if(q=I[LH],!w[LH]){for(;q>=Y6.length;)Y6.push(X(30,E));q=Y6[q]}nH.push(q)}E.F=rE(0,(E.K=rE(0,E,Au.slice(),6),E),nH,7)},k)},341),J(v,function(M,k,C){(C=X(38,M),k=R(M,C),k[0]).removeEventListener(k[1],k[2],Dy)},483),J)(v,[],301),J)(v,function(M,k,C,N,x,U){C=X(22,(U=X(22,(x=X(38,M),M)),M)),M.V==M&&(k=R(M,C),N=R(M,U),R(M,x)[N]=k,475==x&&(M.Z=void 0,2==N&&(M.i=He(32,2,M,false),M.Z=void 0)))},173),J)(v,function(M,k,C,N){C=(k=X(6,(N=X(22,M),M)),X(38,M)),J(M,R(M,N)||R(M,k),C)},189),J)(v,function(M){aS(3,M)},218),J)(v,function(M){X(12,2,4,M)},372),J(v,v,465),v.xH=0,J)(v,[106,0,0],160),tJ)("Submit"),J(v,function(M,k,C,N){if(C=M.pf.pop()){for(k=D(true,8,M);0<k;k--)N=X(6,M),C[N]=M.U[N];M.U=(C[60]=(C[423]=M.U[423],M.U)[60],C)}else J(M,M.O,327)},95),J(v,function(M,k,C,N,x){for(C=(x=(N=Ju(7,14,(k=X(38,M),M)),[]),0);C<N;C++)x.push(D(true,8,M));J(M,x,k)},159),J)(v,function(M,k,C,N,x,U,Q,n,e){jS(22,false,false,k,true,M)||(C=Yk(22,8,M.V,1,0),e=C.D,N=C.M7,Q=C.Cf,n=C.G5,U=e.length,x=0==U?new N[n]:1==U?new N[n](e[0]):2==U?new N[n](e[0],e[1]):3==U?new N[n](e[0],e[1],e[2]):4==U?new N[n](e[0],e[1],e[2],e[3]):2(),J(M,x,Q))},250),v),[L_],27,0),[cx,W]),21,0),0)),aF(254,true,true,v,254)},dE=[],bb=function(f,W,v,T,S){if((S=typeof W,S)==f)if(W){if(W instanceof Array)return"array";if(W instanceof Object)return S;if(T=Object.prototype.toString.call(W),"[object Window]"==T)return f;if("[object Array]"==T||"number"==typeof W.length&&"undefined"!=typeof W.splice&&"undefined"!=typeof W.propertyIsEnumerable&&!W.propertyIsEnumerable("splice"))return"array";if("[object Function]"==T||"undefined"!=typeof W.call&&"undefined"!=typeof W.propertyIsEnumerable&&!W.propertyIsEnumerable("call"))return"function"}else return v;else if("function"==S&&"undefined"==typeof W.call)return f;return S},XB=function(f,W,v,T,S,P,M,k,C,N,x,U){try{for(U=0;1414361568!==U;)S=(S|0)+(((f<<4|0)^f>>>5)+(f|0)^(x=v[3-(~U&3)],-2*~(U|x)+(U^x)+T*(~U^x)))|0,U=U+2325900175|0,f=(f|0)+((N=(S<<4|0)^S>>>5,(N&S)-1-~S+(N&~S))^(k=v[P=U>>>11,(P|3)-~(P&3)+~(P|3)],-~(U&k)+-2-~(U|k)))|0;return[S>>>24,S>>16&255,(M=S>>W,(M|255)-~(M&255)+~(M|255)),(S|255)- -1+(~S^255),f>>>24,f>>16&255,(C=f>>W,255-~C+~(C|255)),f&255]}catch(Q){throw Q;}},u=((MQ,gE,wM,function(){})(IS),function(f,W,v,T){for(v=-(W&-2)-(~W^1)+2*(W|-(T=[],2))-(~W|1);0<=v;v--)T[-(~W^1)-(~W&1)+(W|-2)-(v|0)]=f>>8*v&255;return T}),D=(r=G.prototype,function(f,W,v){return v.K?ce(v,v.F):He(W,2,v,f)}),He=function(f,W,v,T,S,P,M,k,C,N,x,U,Q,n,e,c,I,l,w,H){if(S=R(v,327),S>=v.O)throw[Bx,31];for(U=(k=v.mT.length,e=(Q=0,S),f);0<U;)x=e%8,I=8-(x|0),n=e>>3,c=v.B[n],M=I<U?I:U,T&&(C=v,C.Z!=e>>6&&(C.Z=e>>6,l=R(C,475),C.io=XB(C.Z,8,[0,0,l[1],l[W]],W,C.i)),c=(P=v.io[(k|0)- -2+(~n&k)+W*(n|~k)],-(c|0)+-3-~P-W*(~c|P))),Q=(w=(c>>1+W*(8^x)-3*(-9&x)+(-9|x)-(M|0)&(H=1<<M,-2*(H|1)-W*~H+3*(H^1)+W*(~H^1)))<<W*~M-W*~(U|M)-(U^M),(Q|0)+(w|0)+~(Q|w)-(~Q^w)),e+=M,U-=M;return J(v,-2*~(S|f)-W*(S&~f)+(S^f)+(N=Q,W*(S|~f)),327),N},p_=(r.uP=function(){return pH.call(this,11,7)},r.HZ=function(f,W,v,T,S,P,M,k){return pH.call(this,11,32,f,W,v,T,S,P,M,k)},function(f,W,v){(v.pf.push(v.U.slice()),v.U[f]=void 0,J)(v,W,f)}),R=(G.prototype.s="create",function(f,W,v){if(void 0===(v=f.U[W],v))throw[Bx,30,W];if(v.value)return v.create();return(v.create(3*W*W+51*W+26),v).prototype}),g=function(f,W,v,T,S,P,M,k,C){if(f.V==f)for(S=R(f,v),32==v?(k=function(N,x,U,Q,n,e,c){if((n=(e=S.length,-(e|4)+-5-2*~(e|4)+(e|-5))>>3,S.ff)!=n){x=[0,0,(Q=(U=n<<3,2+(U^4)+(S.ff=n,2*(U|-5))),C[1]),C[2]];try{S.oU=XB(rE(0,1,8,10,(Q|0)+4,S),8,x,2,rE(0,1,8,3,Q,S))}catch(I){throw I;}}S.push((c=S.oU[(e|0)+(e&-8)-2*(e^7)+2*(~e&7)],(c|N)+~(c|N)+(~c&N)-(~c|N)))},C=R(f,370)):k=function(N){S.push(N)},T&&k(T&255),M=W.length,P=0;P<M;P++)k(W[P])},FS=(r.rP=function(f,W,v,T,S){return t.call(this,30,8,f,W,v,T,S)},void 0),zX=Bx.constructor,DS=(r.jd=function(){return V.call(this,48)},function(f,W,v,T,S,P,M,k,C,N){if((0==(M=R(v,((k=void 0,f)&&f[0]===Bx&&(W=f[1],k=f[2],f=void 0),423)),M).length&&(N=R(v,115)>>3,M.push(W,N>>8&255,N&255),void 0!=k&&M.push(k&255)),S="",f)&&(f.message&&(S+=f.message),f.stack&&(S+=":"+f.stack)),C=R(v,60),3<C){(P=(S=S7((C-=(S=S.slice(0,~(C&3)- -1-~C+(C|-4)),(S.length|0)+3),S.replace(/\\r\\n/g,"\\n")),1,10),v.V),v).V=v;try{g(v,u(S.length,2).concat(S),32,T)}finally{v.V=P}}J(v,C,60)}),J=function(f,W,v){475==(327==v||115==v?f.U[v]?f.U[v].concat(W):f.U[v]=rE(0,f,W,5):160==v||32==v||301==v||423==v||370==v?f.U[v]||(f.U[v]=Zy(54,W,51,3,f,44,v)):f.U[v]=Zy(73,W,51,9,f,44,v),v)&&(f.i=He(32,2,f,false),f.Z=void 0)},Oj=(r.YH=function(f,W,v,T,S,P,M){return lb.call(this,17,f,W,v,T,S,P,M)},r.$=(window.performance||{}).now?function(){return this.Ej+window.performance.now()}:function(){return+new Date},function(f,W,v,T,S,P){return(JJ(20,T,S,((P=R(W,327),W.B)&&P<W.O?(J(W,W.O,327),p_(327,v,W)):J(W,v,327),W)),J)(W,P,327),R(W,f)}),JJ=(G.prototype.eG=function(f,W,v,T,S,P){return Zy.call(this,T,v,W,8,P,f,S)},function(f,W,v,T,S,P,M,k){if(!T.j){T.rd++;try{for(S=(P=void 0,M=T.O,v);--W;)try{if((k=void 0,T).K)P=ce(T,T.K);else{if((S=R(T,327),S)>=M)break;P=(k=X(22,(J(T,S,115),T)),R)(T,k)}jS(f,false,false,(P&&P.call?P(T,W):DS([Bx,21,k],v,T,195),W),false,T)}catch(C){R(T,428)?DS(C,22,T,195):J(T,C,428)}if(!W){if(T.IU){JJ(20,(T.rd--,526034690118),0,T);return}DS([Bx,33],v,T,195)}}catch(C){try{DS(C,22,T,195)}catch(N){B(T,8,"~",N)}}T.rd--}}),Yk=function(f,W,v,T,S,P,M,k,C,N){for(M=(C=X(30,(P=((N=X((k={},30),v),k.Cf=X(38,v),k).D=[],v.V==v?(D(true,W,v)|S)-T:1),v)),S);M<P;M++)k.D.push(X(f,v));for(;P--;)k.D[P]=R(v,k.D[P]);return k.M7=R(v,C),k.G5=R(v,N),k},ce=function(f,W,v){return(v=W.create().shift(),f.K.create()).length||f.F.create().length||(f.K=void 0,f.F=void 0),v},XS=function(f,W,v,T,S,P,M,k,C,N){if(S=f[0],S==ib)T.yk=25,T.J(f);else if(S==hu){N=f[1];try{P=T.j||T.J(f)}catch(x){B(T,16,"~",x),P=T.j}N(P)}else if(S==dE)T.J(f);else if(S==cx)T.J(f);else if(S==Ej){try{for(C=0;C<T.Oj.length;C++)try{M=T.Oj[C],M[0][M[1]](M[2])}catch(x){}}catch(x){}(0,f[1])(function(x,U){T.eG(x,true,U)},(T.Oj=[],function(x){(z(T,[Hx],(x=!T.W.length,24),0),x)&&aF(254,v,true,T,254)}))}else{if(S==mr)return k=f[2],J(T,f[6],W),J(T,k,458),T.J(f);S==Hx?(T.U=null,T.nf=[],T.B=[]):S==L_&&"loading"===O.document.readyState&&(T.A=function(x,U,Q){(U=v,Q=function(){U||(U=true,x())},O.document.addEventListener("DOMContentLoaded",Q,Dy),O).addEventListener("load",Q,Dy)})}};G.prototype.J=function(f,W){return f=(FS=function(){return f==W?26:15},{}),W={},function(v,T,S,P,M,k,C,N,x,U,Q,n,e,c,I,l,w,H,Qo,F,d,Au,E){f=(w=f,W);try{if(U=v[0],U==cx){S=v[1];try{for(l=atob((c=0,I=[],S)),F=0;c<l.length;c++)P=l.charCodeAt(c),255<P&&(I[F++]=255+(P&-256)-(P^255),P>>=8),I[F++]=P;J(this,(this.O=(this.B=I,this.B.length<<3),[0,0,0]),475)}catch(q){DS(q,17,this,195);return}JJ(20,8001,0,this)}else if(U==ib)v[1].push(R(this,32).length,R(this,160).length,R(this,301).length,R(this,60)),J(this,v[2],458),this.U[52]&&Oj(458,this,R(this,52),8001,0);else{if(U==hu){Qo=(Q=v[2],M=u((R(this,160).length|0)+2,2),this).V,this.V=this;try{C=R(this,423),0<C.length&&g(this,u(C.length,2).concat(C),160,192),g(this,u(this.W3,1),160,167),g(this,u(this[hu].length,1),160),H=0,e=R(this,32),H+=R(this,489)&2047,H-=(d=R(this,160).length,-2*~(d|5)+2*(d&-6)-(d^5)+2*(~d|5)),4<e.length&&(H-=(e.length|0)+3),0<H&&g(this,u(H,2).concat(gE(H)),160,197),4<e.length&&g(this,u(e.length,2).concat(e),160,86)}finally{this.V=Qo}if(E=((n=gE(2).concat(R(this,160)),n)[1]=n[0]^204,n[3]=(N=n[1],T=M[0],2*(~N&T)+(N|~T)-(~N|T)),n[4]=n[1]^M[1],this).B3(n))E="<"+E;else for(x=0,E="";x<n.length;x++)k=n[x][this.c3](16),1==k.length&&(k="0"+k),E+=k;return((R((Au=E,this),32).length=Q.shift(),R(this,160).length=Q.shift(),R)(this,301).length=Q.shift(),J)(this,Q.shift(),60),Au}if(U==dE)Oj(458,this,v[1],v[2],0);else if(U==mr)return Oj(458,this,v[1],8001,0)}}finally{f=w}}}();var lP,aS=function(f,W,v,T,S,P,M){g(W,((P=X(30,(S=X(14,(v=3+(f&-4)-(f^(M=f&4,3)),W)),W)),T=R(W,S),M)&&(T=S7((""+T).replace(/\\r\\n/g,"\\n"),1,10)),v&&g(W,u(T.length,2),P),T),P)},FB=function(f,W,v,T,S,P,M,k,C,N){for(;v.W.length;){C=(v.A=M,v.W).pop();try{N=XS(C,f,false,v)}catch(x){B(v,28,P,x)}if(S&&v.A){k=v.A,k(function(){aF(254,W,W,v,T)});break}}return N},y4=(G.prototype[Ej]=[0,0,1,1,0,1,1],G.prototype.B3=function(f,W,v,T,S){return A.call(this,v,W,5,f,T,S)},G.prototype.zh=0,/./),mG=function(f,W,v,T){g(f,u((T=X(38,(v=X(38,f),f)),R(f,v)),W),T)},aF=function(f,W,v,T,S,P,M,k){if(T.W.length){T.hA&&0(),T.hA=true,T.JA=v;try{k=T.$(),T.uo=0,T.L=k,T.l=k,P=FB(424,true,T,f,v,"~",null),M=T.$()-T.L,T.$d+=M,M<(W?0:10)||0>=T.yk--||(M=Math.floor(M),T.nf.push(M<=S?M:254))}finally{T.hA=false}return P}},zM=cx.pop.bind(G.prototype[ib]),qQ=((lP=x6(370,{get:zM},21,(y4[G.prototype.c3]=zM,G.prototype.s)),G.prototype).ho=void 0,function(f,W){return(W=Px("error",null,"tl"))&&1===f.eval(W.createScript("1"))?function(v){return W.createScript(v)}:function(v){return""+v}})(O);(Z=O.watchbell||(O.watchbell={}),40<Z.m)||(Z.m=41,Z.tl=oS,Z.a=KH),Z.MQe_=function(f,W,v){return v=new G(f,W),[function(T){return TX(3,false,12,T,v)}]};try{Z.u||(O.addEventListener("unload",function(){},Dy),Z.u=1)}catch(f){};}).call(this);'));}).call(this);
  </script> 
  <script type="text/javascript" nonce="o6zmUp8iOL7zHDPMn1Dlkw">

  document.bg = new watchbell.tl('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');
  </script> 
  <script nonce="o6zmUp8iOL7zHDPMn1Dlkw">

  gaia = window.gaia || {};
  gaia.ps = gaia.ps || {};
  gaia.ps.hasPrefilledIdentifier = false;
  function gaia_parseFragment() {
  var hash = location.hash;
  var params = {};
  if (!hash) {
  return params;
  }
  var paramStrs = decodeURIComponent(hash.substring(1)).split('&');
  for (var i = 0; i < paramStrs.length; i++) {
      var param = paramStrs[i].split('=');
      params[param[0]] = param[1];
    }
    return params;
  }

  function gaia_prefillEmail() {
    var email = null;
    var form = null;
    if (document.getElementById) {
      email = document.getElementById('Email');
      form = document.getElementById('gaia_loginform');
    }
    if (form && email && (email.value == null || email.value == '')
        && (email.type != 'hidden')) {
      hashParams = gaia_parseFragment();
      if (hashParams['Email'] && hashParams['Email'] != '') {
        email.value = hashParams['Email'];
      }
    }
  }


  try {
    gaia_prefillEmail();
  } catch (e) {
  }

  </script> 
  <script nonce="o6zmUp8iOL7zHDPMn1Dlkw">

  var gaia_scrollToElement = function(element) {
  var calculateOffsetHeight = function(element) {
  var curtop = 0;
  if (element.offsetParent) {
  while (element) {
  curtop += element.offsetTop;
  element = element.offsetParent;
  }
  }
  return curtop;
  }
  var siginOffsetHeight = calculateOffsetHeight(element);
  var scrollHeight = siginOffsetHeight - window.innerHeight +
  element.clientHeight + 0.02 * window.innerHeight;
  window.scroll(0, scrollHeight);
  }
  </script> 
  <script nonce="o6zmUp8iOL7zHDPMn1Dlkw">

  if (gaia.ps.hasPrefilledIdentifier) {
  var form = document.getElementById('gaia_loginform');
  if (form) {
  form.submit();
  }
  }
  </script> 
  <script nonce="o6zmUp8iOL7zHDPMn1Dlkw">

  (function(){
  gaia_onLoginSubmit = function() {
  try {
  document.bg.low(function(response) {
  document.getElementById('bgresponse').value = response;
  });
  } catch (err) {
  document.getElementById('bgresponse').value = '';
  }
  return true;
  }
  document.getElementById('gaia_loginform').onsubmit = gaia_onLoginSubmit;
  var signinButton = document.getElementById('next');
  gaia_attachEvent(window, 'load', function(){
  gaia_scrollToElement(signinButton);
  });
  })();
  </script>
</body>
</html>
