<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>INNOVATE CAPITAL | Trading Mentorship</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #050505;
            color: white;
            line-height: 1.6;
        }

        :root {
            --blue: #8ed8ff;
            --blue-dark: #55b9e8;
            --white: #ffffff;
            --black: #050505;
            --grey: #b8b8b8;
            --card: #0d0d0d;
        }

        /* NAVIGATION */

        nav {
            width: 100%;
            position: fixed;
            top: 0;
            left: 0;
            z-index: 1000;
            background: rgba(5, 5, 5, 0.92);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(142, 216, 255, 0.15);
        }

        .nav-container {
            max-width: 1200px;
            margin: auto;
            padding: 20px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 22px;
            font-weight: 800;
            letter-spacing: 2px;
            color: white;
        }

        .logo span {
            color: var(--blue);
        }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 14px;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--blue);
        }

        /* HERO */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 120px 20px 80px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            width: 600px;
            height: 600px;
            background: var(--blue);
            opacity: 0.07;
            filter: blur(130px);
            border-radius: 50%;
            top: 10%;
            left: 50%;
            transform: translateX(-50%);
        }

        .hero-content {
            max-width: 900px;
            position: relative;
            z-index: 1;
        }

        .small-heading {
            color: var(--blue);
            font-size: 14px;
            letter-spacing: 4px;
            text-transform: uppercase;
            margin-bottom: 20px;
            font-weight: bold;
        }

        .hero h1 {
            font-size: clamp(50px, 9vw, 105px);
            line-height: 0.95;
            letter-spacing: -3px;
            margin-bottom: 25px;
        }

        .hero h1 span {
            color: var(--blue);
        }

        .hero p {
            max-width: 680px;
            margin: auto;
            color: #cfcfcf;
            font-size: 18px;
        }

        .hero-buttons {
            margin-top: 40px;
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .button {
            display: inline-block;
            padding: 15px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        .primary-button {
            background: var(--blue);
            color: #050505;
        }

        .primary-button:hover {
            background: white;
            transform: translateY(-3px);
        }

        .secondary-button {
            border: 1px solid #444;
            color: white;
        }

        .secondary-button:hover {
            border-color: var(--blue);
            color: var(--blue);
        }

        /* GENERAL */

        section {
            padding: 100px 20px;
        }

        .container {
            max-width: 1100px;
            margin: auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title .label {
            color: var(--blue);
            text-transform: uppercase;
            letter-spacing: 3px;
            font-size: 13px;
            font-weight: bold;
        }

        .section-title h2 {
            font-size: 42px;
            margin-top: 10px;
        }

        .section-title p {
            color: #999;
            max-width: 650px;
            margin: 15px auto 0;
        }

        /* ABOUT */

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h3 {
            font-size: 32px;
            margin-bottom: 20px;
        }

        .about-text h3 span {
            color: var(--blue);
        }

        .about-text p {
            color: #bdbdbd;
            margin-bottom: 18px;
        }

        .founder-card {
            background: linear-gradient(145deg, #111111, #080808);
            border: 1px solid rgba(142, 216, 255, 0.2);
            padding: 45px;
            border-radius: 12px;
            position: relative;
            overflow: hidden;
        }

        .founder-card::after {
            content: "";
            position: absolute;
            width: 120px;
            height: 120px;
            background: var(--blue);
            opacity: 0.08;
            border-radius: 50%;
            right: -40px;
            bottom: -40px;
        }

        .founder-card .role {
            color: var(--blue);
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 12px;
            font-weight: bold;
        }

        .founder-card h3 {
            font-size: 35px;
            margin: 10px 0;
        }

        .founder-card p {
            color: #aaa;
        }

        /* MENTORSHIP */

        .mentorship {
            background: #080808;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .feature-card {
            background: var(--card);
            border: 1px solid #1c1c1c;
            padding: 35px 28px;
            border-radius: 10px;
            transition: 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-6px);
            border-color: var(--blue);
        }

        .feature-number {
            color: var(--blue);
            font-size: 14px;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .feature-card h3 {
            font-size: 21px;
            margin-bottom: 12px;
        }

        .feature-card p {
            color: #999;
            font-size: 15px;
        }

        /* APPROACH */

        .approach-box {
            border: 1px solid rgba(142, 216, 255, 0.2);
            border-radius: 12px;
            padding: 60px;
            text-align: center;
            background: linear-gradient(
                145deg,
                rgba(142,216,255,0.05),
                rgba(0,0,0,0)
            );
        }

        .approach-box h2 {
            font-size: 38px;
            margin-bottom: 20px;
        }

        .approach-box h2 span {
            color: var(--blue);
        }

        .approach-box p {
            color: #aaa;
            max-width: 750px;
            margin: auto;
            font-size: 17px;# Innovate.Capital
