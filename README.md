# MINHYUK
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CareGuide - 맞춤형 질환 케어 가이드</title>
    <title>비뇨의학과 전립선비대증 약물 가이드 (ProstaMed Guide)</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&family=Outfit:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700;900&family=Outfit:wght@300;400;600;800&display=swap" rel="stylesheet">
    <!-- Lucide Icons (CDN) -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        :root {
            --primary: #0f766e;
            --primary-light: #14b8a6;
            --primary-hover: #0f766e;
            --primary-bg: #f0fdfa;
            --secondary: #4f46e5;
            --primary: #0284c7; /* Sky blue */
            --primary-hover: #0369a1;
            --primary-light: #e0f2fe;
            --secondary: #4f46e5; /* Indigo */
            --secondary-light: #e0e7ff;
            --accent: #0d9488; /* Teal */
            --accent-light: #ccfbf1;
            --bg-slate: #f8fafc;
            --text-main: #0f172a;
            --text-muted: #475569;
            --text-muted: #64748b;
            --border: #e2e8f0;
            --shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.05), 0 8px 10px -6px rgba(0, 0, 0, 0.05);
            --shadow-lg: 0 20px 25px -5px rgba(13, 148, 136, 0.1), 0 8px 10px -6px rgba(13, 148, 136, 0.05);
            --radius: 16px;
            --card-bg: rgba(255, 255, 255, 0.9);
            --shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.03), 0 8px 10px -6px rgba(0, 0, 0, 0.03);
            --shadow-lg: 0 20px 25px -5px rgba(2, 132, 199, 0.08), 0 10px 10px -6px rgba(2, 132, 199, 0.04);
            --radius: 20px;
        }
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            background-color: var(--bg-slate);
            background-color: #f1f5f9;
            background-image: 
                radial-gradient(at 0% 0%, rgba(224, 242, 254, 0.5) 0px, transparent 50%),
                radial-gradient(at 100% 0%, rgba(224, 231, 255, 0.5) 0px, transparent 50%);
            color: var(--text-main);
            font-family: 'Noto Sans KR', 'Outfit', sans-serif;
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
        /* Header Styles */
        header {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border);
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid rgba(226, 232, 240, 0.8);
            position: sticky;
            top: 0;
            z-index: 100;
            transition: all 0.3s ease;
        }
        .header-container {
            max-width: 1100px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 16px 24px;
            display: flex;
            color: var(--primary);
            font-family: 'Outfit', sans-serif;
            font-weight: 800;
            font-size: 1.5rem;
            font-size: 1.6rem;
            letter-spacing: -0.5px;
        }
        .logo i {
            color: var(--primary-light);
            color: var(--primary);
        }
        .logo span {
            color: var(--text-main);
            font-weight: 400;
            color: var(--secondary);
        }
        .header-actions {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .btn-settings {
            background: transparent;
            background: white;
            border: 1px solid var(--border);
            padding: 8px 16px;
            border-radius: 30px;
            color: var(--text-muted);
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 6px;
            font-size: 0.875rem;
            font-weight: 500;
            transition: all 0.2s ease;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }
        .btn-settings:hover {
            background: #f1f5f9;
            color: var(--text-main);
            border-color: #cbd5e1;
            background: var(--primary-light);
            color: var(--primary-hover);
            border-color: var(--primary);
        }
        /* Main Layout */
        .main-container {
            max-width: 1000px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 24px 60px;
            padding: 32px 24px 60px;
            flex-grow: 1;
            width: 100%;
            display: grid;
            grid-template-columns: 1fr;
            gap: 30px;
        }
        .hero-section {
            text-align: center;
            margin-bottom: 40px;
        @media (min-width: 992px) {
            .main-container {
                grid-template-columns: 7fr 5fr;
            }
        }
        .hero-section h1 {
            font-size: 2.25rem;
            font-weight: 700;
            color: #0f172a;
            margin-bottom: 12px;
            letter-spacing: -0.5px;
        /* Left side: Drug Guide Center */
        .guide-center {
            display: flex;
            flex-direction: column;
            gap: 24px;
        }
        .hero-section h1 span {
            color: var(--primary);
        /* Right side: Interactive Tools (AI Chat & Tips) */
        .tool-center {
            display: flex;
            flex-direction: column;
            gap: 24px;
        }
        .hero-section p {
            color: var(--text-muted);
            font-size: 1.1rem;
        /* Hero / Introduction Box */
        .hero-card {
            background: linear-gradient(135deg, #0284c7 0%, #4f46e5 100%);
            color: white;
            border-radius: var(--radius);
            padding: 32px;
            box-shadow: var(--shadow-lg);
            position: relative;
            overflow: hidden;
        }
        .hero-card::before {
            content: '';
            position: absolute;
            top: -50px;
            right: -50px;
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.08);
            pointer-events: none;
        }
        .hero-card h1 {
            font-size: 2rem;
            font-weight: 800;
            margin-bottom: 12px;
            line-height: 1.3;
        }
        .hero-card p {
            font-size: 1.05rem;
            opacity: 0.9;
            font-weight: 300;
            max-width: 600px;
            margin: 0 auto;
        }
        /* Search Section */
        .search-card {
            background: white;
            background: var(--card-bg);
            backdrop-filter: blur(10px);
            border-radius: var(--radius);
            padding: 24px;
            border: 1px solid rgba(255, 255, 255, 0.6);
            box-shadow: var(--shadow);
            border: 1px solid var(--border);
            margin-bottom: 30px;
            transition: all 0.3s ease;
        }
        .search-card:focus-within {
            box-shadow: var(--shadow-lg);
            border-color: var(--primary-light);
            border-color: var(--primary);
        }
        .search-label {
            font-size: 0.95rem;
            font-weight: 700;
            color: var(--text-main);
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .search-form {
            display: flex;
            gap: 12px;
            width: 100%;
            padding: 16px 16px 16px 52px;
            border: 1px solid var(--border);
            border-radius: 12px;
            border-radius: 14px;
            font-size: 1.05rem;
            font-family: inherit;
            outline: none;
            transition: all 0.2s ease;
            background: #f8fafc;
        }
        .search-input:focus {
            background: white;
            border-color: var(--primary-light);
            border-color: var(--primary);
        }
        .btn-submit {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0 28px;
            border-radius: 12px;
            padding: 0 24px;
            border-radius: 14px;
            font-size: 1rem;
            font-weight: 500;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.2s ease;
        }
        .btn-submit:hover {
            background: #115e59;
            background: var(--primary-hover);
            transform: translateY(-1px);
        }
        .btn-submit:active {
            transform: translateY(0);
        }
        /* Quick Chips */
        .quick-chips {
            margin-top: 16px;
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            align-items: center;
        }
        .chips-label {
            font-size: 0.85rem;
            color: var(--text-muted);
            font-weight: 500;
            margin-right: 4px;
            font-weight: 600;
        }
        .chip {
            background: #f1f5f9;
            border: 1px solid #e2e8f0;
            background: white;
            border: 1px solid var(--border);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85rem;
            color: var(--text-muted);
            font-weight: 500;
            cursor: pointer;
            transition: all 0.2s ease;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }
        .chip:hover {
            background: var(--primary-bg);
            border-color: var(--primary-light);
            color: var(--primary);
        .chip:hover, .chip.active {
            background: var(--primary-light);
            border-color: var(--primary);
            color: var(--primary-hover);
            font-weight: 600;
        }
        /* Loader */
        .loader-container {
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 60px 0;
            text-align: center;
        /* Filter Section tabs */
        .filter-section {
            display: flex;
            gap: 8px;
            overflow-x: auto;
            padding-bottom: 8px;
            margin-bottom: 8px;
        }
        .pulse-loader {
            width: 48px;
            height: 48px;
            border-radius: 50%;
            background: var(--primary-light);
            animation: pulse-animation 1.5s infinite ease-in-out;
            margin-bottom: 20px;
        .filter-tab {
            background: white;
            border: 1px solid var(--border);
            padding: 8px 18px;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--text-muted);
            cursor: pointer;
            white-space: nowrap;
            transition: all 0.2s ease;
        }
        @keyframes pulse-animation {
            0% { transform: scale(0.8); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 1; }
            100% { transform: scale(0.8); opacity: 0.5; }
        .filter-tab:hover {
            background: #f8fafc;
            color: var(--text-main);
        }
        .loader-container p {
            color: var(--text-muted);
            font-weight: 500;
        .filter-tab.active {
            background: var(--secondary);
            color: white;
            border-color: var(--secondary);
        }
        /* Results Section */
        /* Drug List / Detail Results */
        .results-section {
            display: none;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        .drug-card {
            background: white;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            padding: 24px;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
            animation: fadeIn 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        .drug-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 30px -5px rgba(0, 0, 0, 0.05);
        }
        .results-header {
        .drug-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 24px;
            padding-bottom: 12px;
            border-bottom: 2px solid var(--border);
            align-items: flex-start;
            border-bottom: 1px dashed var(--border);
            padding-bottom: 16px;
            margin-bottom: 18px;
        }
        .results-title {
        .drug-title-area {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.5rem;
            font-weight: 700;
            flex-direction: column;
            gap: 4px;
        }
        .drug-name {
            font-size: 1.4rem;
            font-weight: 800;
            color: var(--text-main);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .results-title span {
            color: var(--primary);
        .drug-badge {
            background: var(--primary-light);
            color: var(--primary-hover);
            padding: 4px 10px;
            border-radius: 6px;
            font-size: 0.75rem;
            font-weight: 700;
            letter-spacing: -0.3px;
        }
        .btn-print {
            background: white;
            border: 1px solid var(--border);
            padding: 8px 18px;
            border-radius: 30px;
        .drug-generic {
            font-size: 0.95rem;
            color: var(--text-muted);
            cursor: pointer;
            font-weight: 500;
        }
        .drug-class-tag {
            background: var(--secondary-light);
            color: var(--secondary);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 700;
        }
        /* Detail Blocks */
        .detail-block {
            margin-bottom: 18px;
        }
        .detail-block:last-child {
            margin-bottom: 0;
        }
        .block-title {
            font-size: 0.95rem;
            font-weight: 800;
            color: var(--text-main);
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            font-weight: 500;
            box-shadow: 0 2px 5px rgba(0,0,0,0.02);
            transition: all 0.2s ease;
            gap: 6px;
        }
        .btn-print:hover {
        .block-title i {
            color: var(--primary);
        }
        .block-content {
            font-size: 0.95rem;
            color: #334155;
            background: #f8fafc;
            padding: 12px 16px;
            border-radius: 12px;
            border-left: 4px solid var(--primary);
        }
        .block-content ul {
            list-style-type: none;
            padding-left: 0;
        }
        .block-content li {
            margin-bottom: 8px;
            position: relative;
            padding-left: 18px;
        }
        .block-content li::before {
            content: '•';
            color: var(--primary);
            border-color: var(--primary-light);
            font-weight: bold;
            font-size: 1.2rem;
            position: absolute;
            left: 4px;
            top: -2px;
        }
        .results-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 20px;
        .block-content li:last-child {
            margin-bottom: 0;
        }
        @media (min-width: 768px) {
            .results-grid {
                grid-template-columns: 1fr 1fr;
            }
            .grid-full-width {
                grid-column: span 2;
            }
        /* Different border colors for warnings */
        .border-warning {
            border-left-color: #ef4444 !important;
            background: #fff5f5;
        }
        .block-title-warning i {
            color: #ef4444 !important;
        }
        .block-content-warning li::before {
            content: '⚠️' !important;
            font-size: 0.8rem !important;
            top: 2px !important;
            left: 0px !important;
        }
        .block-content-warning li {
            padding-left: 18px;
        }
        .card {
        /* AI Chat Room Card */
        .ai-chat-card {
            background: white;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            padding: 24px;
            box-shadow: var(--shadow);
            display: flex;
            flex-direction: column;
            height: 480px;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        .card:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 30px -5px rgba(0, 0, 0, 0.08);
        .ai-chat-header {
            background: linear-gradient(135deg, #4f46e5 0%, #3b82f6 100%);
            color: white;
            padding: 16px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .card-header {
        .ai-chat-title {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 16px;
            padding-bottom: 12px;
            border-bottom: 1px dashed var(--border);
            gap: 10px;
            font-weight: 700;
            font-size: 1.05rem;
        }
        .card-icon-wrapper {
            width: 40px;
            height: 40px;
        .ai-chat-title span {
            background: rgba(255,255,255,0.2);
            padding: 2px 8px;
            border-radius: 10px;
            font-size: 0.7rem;
            font-weight: 600;
        }
        .chat-body {
            flex-grow: 1;
            padding: 20px;
            overflow-y: auto;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            gap: 12px;
            background: #f8fafc;
        }
        .card-title {
            font-size: 1.15rem;
            font-weight: 700;
        .chat-msg {
            max-width: 85%;
            padding: 12px 16px;
            border-radius: 16px;
            font-size: 0.925rem;
            line-height: 1.5;
            animation: slideUp 0.2s ease;
        }
        .msg-bot {
            background: white;
            color: var(--text-main);
            align-self: flex-start;
            border-bottom-left-radius: 4px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.03);
            border: 1px solid var(--border);
        }
        /* Card Colors */
        .card-info {
            border-left: 5px solid var(--primary-light);
        .msg-user {
            background: var(--secondary);
            color: white;
            align-self: flex-end;
            border-bottom-right-radius: 4px;
        }
        .card-info .card-icon-wrapper {
            background: #ccfbf1;
            color: var(--primary);
        .chat-input-area {
            padding: 12px 16px;
            background: white;
            border-top: 1px solid var(--border);
            display: flex;
            gap: 10px;
        }
        .card-rules {
            border-left: 5px solid var(--secondary);
        .chat-input {
            flex-grow: 1;
            border: 1px solid var(--border);
            border-radius: 20px;
            padding: 10px 16px;
            font-family: inherit;
            font-size: 0.9rem;
            outline: none;
            transition: all 0.2s ease;
        }
        .card-rules .card-icon-wrapper {
            background: #e0e7ff;
            color: var(--secondary);
        .chat-input:focus {
            border-color: var(--secondary);
        }
        .card-avoid {
            border-left: 5px solid #ef4444;
        .btn-chat-send {
            background: var(--secondary);
            color: white;
            border: none;
            width: 38px;
            height: 38px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s ease;
        }
        .card-avoid .card-icon-wrapper {
            background: #fee2e2;
            color: #ef4444;
        .btn-chat-send:hover {
            background: #4338ca;
            transform: scale(1.05);
        }
        .card-recommend {
            border-left: 5px solid #10b981;
        /* Tips & Caution Accordion */
        .info-card {
            background: white;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            padding: 24px;
            box-shadow: var(--shadow);
        }
        .card-recommend .card-icon-wrapper {
            background: #d1fae5;
            color: #10b981;
        .info-card-title {
            font-size: 1.15rem;
            font-weight: 800;
            color: var(--text-main);
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
            border-bottom: 1px solid var(--border);
            padding-bottom: 10px;
        }
        .card-body ul {
            list-style-position: inside;
            padding-left: 4px;
        .info-card-title i {
            color: #ef4444; /* red icon for caution */
        }
        .card-body li {
        .accordion-item {
            border: 1px solid var(--border);
            border-radius: 12px;
            margin-bottom: 10px;
            font-size: 0.975rem;
            color: #334155;
            overflow: hidden;
        }
        .card-body li strong {
        .accordion-item:last-child {
            margin-bottom: 0;
        }
        .accordion-header {
            background: #f8fafc;
            padding: 14px 18px;
            font-size: 0.9rem;
            font-weight: 700;
            color: var(--text-main);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: background-color 0.2s ease;
        }
        .card-body p {
            color: #334155;
            font-size: 0.975rem;
            margin-bottom: 10px;
        .accordion-header:hover {
            background: #f1f5f9;
        }
        /* API Settings Modal */
        .accordion-body {
            padding: 14px 18px;
            font-size: 0.875rem;
            color: #475569;
            background: white;
            border-top: 1px solid var(--border);
            display: none;
            line-height: 1.5;
        }
        .accordion-body p {
            margin-bottom: 8px;
        }
        .accordion-body p:last-child {
            margin-bottom: 0;
        }
        /* Settings Modal */
        .modal {
            display: none;
            position: fixed;
        .modal-content {
            background: white;
            border-radius: var(--radius);
            width: 100%;
            width: 90%;
            max-width: 480px;
            padding: 30px;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.15);
            border: 1px solid var(--border);
            position: relative;
            animation: slideUp 0.3s cubic-bezier(0.16, 1, 0.3, 1);
        }
        @keyframes slideUp {
            from { transform: translateY(20px); }
            to { transform: translateY(0); }
        }
        .modal-header {
            display: flex;
            justify-content: space-between;
        }
        .modal-body input:focus {
            border-color: var(--primary-light);
            border-color: var(--primary);
        }
        .modal-body .info-text {
        }
        .btn-save:hover {
            background: #115e59;
            background: var(--primary-hover);
        }
        /* Notification Toast */
        /* Toast Notification */
        .toast {
            position: fixed;
            bottom: 24px;
            right: 24px;
            background: #1e293b;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            border-radius: 10px;
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.3);
            display: flex;
            align-items: center;
            opacity: 1;
        }
        /* Loader inside search */
        .loader {
            display: none;
            align-items: center;
            justify-content: center;
            padding: 40px;
            text-align: center;
            flex-direction: column;
            gap: 16px;
        }
        .spinner {
            width: 40px;
            height: 40px;
            border: 4px solid var(--primary-light);
            border-top: 4px solid var(--primary);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes slideUp {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        /* Footer */
        footer {
            border-top: 1px solid var(--border);
            padding: 24px;
            padding: 30px 24px;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.85rem;
            background: white;
            margin-top: 40px;
        }
        /* PRINT STYLING */
        @media print {
            body {
                background: white;
                color: black;
                font-size: 12pt;
                font-size: 11pt;
            }
            header, .search-card, .btn-print, footer, .btn-settings, .modal {
            header, .hero-card, .search-card, .tool-center, footer, .btn-settings, .modal {
                display: none !important;
            }
            .main-container {
                display: block;
                padding: 0;
                margin: 0;
                max-width: 100%;
            }
            .results-section {
                display: block !important;
            }
            .results-header {
                border-bottom: 2px solid #000;
                margin-bottom: 20px;
            }
            .results-grid {
                display: block;
            }
            .card {
                border: 1px solid #ccc;
            .drug-card {
                border: 1px solid #aaa;
                box-shadow: none !important;
                transform: none !important;
                margin-bottom: 20px;
                margin-bottom: 30px;
                page-break-inside: avoid;
                border-left: 6px solid #666 !important;
                padding: 15px;
                padding: 20px;
            }
            .card-info { border-left-color: #0f766e !important; }
            .card-rules { border-left-color: #4f46e5 !important; }
            .card-avoid { border-left-color: #ef4444 !important; }
            .card-recommend { border-left-color: #10b981 !important; }
            
            .card-icon-wrapper {
                display: none;
            .block-content {
                background: #fdfdfd;
                border-left: 4px solid #666;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-container">
            <a href="#" class="logo">
                <i data-lucide="heart-pulse"></i>
                Care<span>Guide</span>
                <i data-lucide="shield-check"></i>
                Prosta<span>Med</span>
            </a>
            <div class="header-actions">
                <button class="btn-settings" id="btn-open-settings">
                    <i data-lucide="key" style="width: 16px; height: 16px;"></i>
                    API 설정
                    Gemini API 설정
                </button>
            </div>
        </div>
    </header>
    <main class="main-container">
        <section class="hero-section">
            <h1>환자 맞춤형 <span>케어 가이드</span></h1>
            <p>환자의 진단명을 입력하면 정확하고 쉬운 질환 정보, 일상생활 속 수칙, 주의해야 할 음식 정보를 제공합니다.</p>
        </section>
        <!-- Left Column: Medications Portal -->
        <div class="guide-center">
            <div class="hero-card">
                <h1>전립선비대증 약물 가이드</h1>
                <p>비뇨의학과에서 처방받으신 약물 이름을 검색하거나 계열을 선택해 보세요. 복용법, 약리 작용, 그리고 부작용 대처법을 일반인의 눈높이에 맞추어 친절하게 설명해 드립니다.</p>
            </div>
        <section class="search-card">
            <form class="search-form" id="search-form">
                <div class="input-group">
                    <i data-lucide="search" class="input-icon"></i>
                    <input type="text" id="search-input" class="search-input" placeholder="진단명 또는 질환명을 입력하세요 (예: 당뇨병, 고혈압, 아토피)" required autocomplete="off">
            <!-- Search Area -->
            <div class="search-card">
                <div class="search-label">
                    <i data-lucide="search" style="width: 18px; height: 18px; color: var(--primary);"></i>
                    약물 이름 또는 성분명 검색
                </div>
                <button type="submit" class="btn-submit">
                    <span>분석하기</span>
                    <i data-lucide="sparkles" style="width: 18px; height: 18px;"></i>
                </button>
            </form>
                <form class="search-form" id="search-form">
                    <div class="input-group">
                        <i data-lucide="search" class="input-icon"></i>
                        <input type="text" id="search-input" class="search-input" placeholder="예: 하루날디, 아보다트, 탐스로신, 피나스테리드 등" required autocomplete="off">
                    </div>
                    <button type="submit" class="btn-submit">
                        <span>검색</span>
                        <i data-lucide="arrow-right" style="width: 16px; height: 16px;"></i>
                    </button>
                </form>
            <div class="quick-chips">
                <span class="chips-label">자주 찾는 질환:</span>
                <button class="chip" type="button" data-disease="당뇨병">당뇨병</button>
                <button class="chip" type="button" data-disease="고혈압">고혈압</button>
                <button class="chip" type="button" data-disease="역류성 식도염">역류성 식도염</button>
                <button class="chip" type="button" data-disease="아토피 피부염">아토피 피부염</button>
                <button class="chip" type="button" data-disease="통풍">통풍</button>
                <div class="quick-chips">
                    <span class="chips-label">주요 약물:</span>
                    <button class="chip" type="button" data-search="하루날디">하루날디</button>
                    <button class="chip" type="button" data-search="아보다트">아보다트</button>
                    <button class="chip" type="button" data-search="프로스카">프로스카</button>
                    <button class="chip" type="button" data-search="듀오다트">듀오다트</button>
                    <button class="chip" type="button" data-search="시알리스">시알리스 5mg</button>
                    <button class="chip" type="button" data-search="트루패스">트루패스</button>
                </div>
            </div>
        </section>
        <!-- Loading State -->
        <div class="loader-container" id="loader">
            <div class="pulse-loader"></div>
            <p>Gemini AI가 질환 맞춤형 가이드를 생성하고 있습니다...</p>
            <!-- Filter tabs by Class -->
            <div class="filter-section">
                <button class="filter-tab active" data-class="all">전체보기</button>
                <button class="filter-tab" data-class="알파차단제">알파차단제 (배뇨개선)</button>
                <button class="filter-tab" data-class="5-알파 환원효소 억제제">5-AR억제제 (크기감소)</button>
                <button class="filter-tab" data-class="복합제">복합제</button>
                <button class="filter-tab" data-class="PDE5 억제제">PDE5억제제</button>
                <button class="filter-tab" data-class="과민성 방광">과민성 방광 (조절제)</button>
            </div>
            <!-- Loader -->
            <div class="loader" id="loader">
                <div class="spinner"></div>
                <p style="color: var(--text-muted); font-weight: 500;">AI 약학 카운셀러가 질문을 분석하여 답변을 구성하고 있습니다...</p>
            </div>
            <!-- Detailed Results Container -->
            <div class="results-section" id="results-section">
                <!-- Drug info cards will be dynamically inserted here -->
            </div>
        </div>
        <!-- Results Display -->
        <section class="results-section" id="results-section">
            <div class="results-header">
                <h2 class="results-title" id="results-title">
                    <i data-lucide="file-text" style="color: var(--primary);"></i>
                    [<span id="disease-name">진단명</span>] 케어 가이드
                </h2>
                <button class="btn-print" id="btn-print">
                    <i data-lucide="printer" style="width: 18px; height: 18px;"></i>
                    인쇄 / PDF 저장
                </button>
        <!-- Right Column: Interactive AI & Lifestyle Guide -->
        <div class="tool-center">
            <!-- AI Counseling Room -->
            <div class="ai-chat-card">
                <div class="ai-chat-header">
                    <div class="ai-chat-title">
                        <i data-lucide="bot" style="width: 20px; height: 20px;"></i>
                        AI 약물 상담실 
                        <span>Gemini 3.5</span>
                    </div>
                    <i data-lucide="sparkles" style="width: 18px; height: 18px;"></i>
                </div>
                <div class="chat-body" id="chat-body">
                    <div class="chat-msg msg-bot">
                        안녕하세요! ProstaMed AI 상담원입니다. 비뇨의학과 전립선 약에 대해 평소 궁금했던 점을 질문해 보세요. 
                        <br><br>
                        예시:<br>
                        - "전립선 약 먹고 머리가 왜 어지러운가요?"<br>
                        - "탈모약과 전립선비대증 약을 같이 먹어도 되나요?"<br>
                        - "감기약 먹을 때 전립선 약 복용자가 주의해야 할 점은 무엇인가요?"
                    </div>
                </div>
                <div class="chat-input-area">
                    <input type="text" id="chat-input" class="chat-input" placeholder="메시지를 입력하세요..." autocomplete="off">
                    <button class="btn-chat-send" id="btn-chat-send">
                        <i data-lucide="send" style="width: 16px; height: 16px;"></i>
                    </button>
                </div>
            </div>
            <div class="results-grid">
                <!-- 1. Disease Info (Full Width) -->
                <div class="card card-info grid-full-width">
                    <div class="card-header">
                        <div class="card-icon-wrapper">
                            <i data-lucide="activity"></i>
                        </div>
                        <h3 class="card-title">어떤 질환인가요? (질환 설명)</h3>
            <!-- Important Lifestyle Precautions -->
            <div class="info-card">
                <div class="info-card-title">
                    <i data-lucide="alert-triangle"></i>
                    전립선비대증 생활 가이드 & 주의사항
                </div>
                
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>1. 감기약 복용 시 절대 주의! (급성 요폐 위험)</span>
                        <i data-lucide="chevron-down" style="width: 16px; height: 16px;"></i>
                    </div>
                    <div class="card-body" id="info-body">
                        <!-- Content goes here -->
                    <div class="accordion-body">
                        <p>콧물 감기약에 흔히 포함된 <strong>'항히스타민제'</strong>나 <strong>'교감신경흥분제(코막힘 완화)'</strong> 성분은 방광 근육을 수축시키고 요도를 더 강하게 쪼이게 만듭니다.</p>
                        <p>이로 인해 소변이 한 방울도 나오지 않는 <strong>'급성 요폐'</strong>가 발생할 수 있습니다. 감기나 비염 약을 처방받거나 약국에서 구매하실 때 반드시 <strong>"전립선비대증 약을 먹고 있습니다"</strong>라고 말씀하셔야 합니다.</p>
                    </div>
                </div>
                <!-- 2. Action Rules -->
                <div class="card card-rules">
                    <div class="card-header">
                        <div class="card-icon-wrapper">
                            <i data-lucide="check-circle-2"></i>
                        </div>
                        <h3 class="card-title">일상생활 행동 수칙</h3>
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>2. 기립성 저혈압 대처하기</span>
                        <i data-lucide="chevron-down" style="width: 16px; height: 16px;"></i>
                    </div>
                    <div class="card-body" id="rules-body">
                        <!-- Content goes here -->
                    <div class="accordion-body">
                        <p>알파차단제 계열(하루날디, 트루패스 등)은 요도 근육뿐 아니라 온몸의 혈관도 약간 이완시킵니다. 따라서 누워 있거나 앉아 있다가 갑자기 일어날 때 머리로 피가 늦게 전달되어 <strong>어지러움(기립성 저혈압)</strong>을 유발할 수 있습니다.</p>
                        <p>이를 예방하기 위해 잠자리나 의자에서 일어날 때는 <strong>2~3초간 천천히 일어나는 습관</strong>을 들이시는 것이 좋고, 주로 저녁이나 취침 전에 약을 드시는 것이 도움이 됩니다.</p>
                    </div>
                </div>
                <!-- 3. Foods to Avoid -->
                <div class="card card-avoid">
                    <div class="card-header">
                        <div class="card-icon-wrapper">
                            <i data-lucide="ban"></i>
                        </div>
                        <h3 class="card-title">주의해야 할 음식</h3>
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>3. 저녁 수분 및 카페인 섭취 조절</span>
                        <i data-lucide="chevron-down" style="width: 16px; height: 16px;"></i>
                    </div>
                    <div class="card-body" id="avoid-body">
                        <!-- Content goes here -->
                    <div class="accordion-body">
                        <p>밤에 자다 깨서 소변을 보는 <strong>야간뇨</strong> 증상이 있는 분들은 저녁 식사 이후(특히 주무시기 2~3시간 전)에는 가급적 수분 섭취를 최소화하는 것이 좋습니다.</p>
                        <p>커피(카페인), 탄산음료, 술은 방광을 자극해 이뇨 작용을 촉진하고 빈뇨를 악화시키므로 최대한 피하시는 것이 현명합니다.</p>
                    </div>
                </div>
                <!-- 4. Recommended Foods (Extra) -->
                <div class="card card-recommend grid-full-width">
                    <div class="card-header">
                        <div class="card-icon-wrapper">
                            <i data-lucide="apple"></i>
                        </div>
                        <h3 class="card-title">섭취를 권장하는 좋은 음식</h3>
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>4. 오랜 시간 앉아있는 자세 피하기</span>
                        <i data-lucide="chevron-down" style="width: 16px; height: 16px;"></i>
                    </div>
                    <div class="card-body" id="recommend-body">
                        <!-- Content goes here -->
                    <div class="accordion-body">
                        <p>오랫동안 한 자리에 앉아 있거나 장시간 운전을 하면 회음부와 전립선 부위가 압박을 받아 혈액 순환이 잘 되지 않고 전립선 울혈이 발생하여 소변 증상이 즉시 악화될 수 있습니다.</p>
                        <p>최소 1시간에 한 번씩은 일어나서 <strong>5분 정도 가볍게 걷거나 스트레칭</strong>을 해주는 것이 골반 근육을 완화하고 증상을 완화하는 데 큰 도움이 됩니다.</p>
                    </div>
                </div>
            </div>
        </section>
        </div>
    </main>
    <!-- Settings Modal -->
                <label for="api-key-input">Gemini API Key</label>
                <input type="password" id="api-key-input" placeholder="AI Studio에서 발급받은 API 키를 입력하세요">
                <p class="info-text">
                    * 이 브라우저의 로컬 스토리지에 저장되어 개인정보가 유출되지 않습니다.<br>
                    * 프로젝트 폴더의 <code>API key.txt</code> 파일에 키를 저장하면 자동으로 로드됩니다.
                    * 이 브라우저의 로컬 스토리지에 저장되어 안전합니다.<br>
                    * 프로젝트 폴더 내 <code>API key.txt</code>에 키를 적어두면 자동으로 읽어옵니다.
                </p>
            </div>
            <div class="modal-footer">
                <button class="btn-cancel" id="btn-cancel-settings">취소</button>
                <button class="btn-save" id="btn-save-settings">저장</button>
            </div>
        </div>
    </div>
    <!-- Notification Toast -->
    <!-- Toast Notification -->
    <div class="toast" id="toast">
        <i data-lucide="info" style="width: 18px; height: 18px;"></i>
        <span id="toast-message">메시지 내용</span>
        <span id="toast-message">알림 메시지</span>
    </div>
    <footer>
        <p>© 2026 CareGuide. 이 정보는 AI가 생성한 참고용 가이드이며, 실제 치료 계획은 전문 의료진과 상담하십시오.</p>
        <p>© 2026 ProstaMed Guide. 이 웹사이트의 모든 의학 정보는 참고용이며, 정확한 처방과 치료 지침은 반드시 비뇨의학과 전문의와 직접 상담하십시오.</p>
    </footer>
    <!-- App Logic -->
    <script src="db.js"></script>
    <script src="app.js"></script>
    <script>
        // Accordion functionality
        document.querySelectorAll('.accordion-header').forEach(header => {
            header.addEventListener('click', () => {
                const body = header.nextElementSibling;
                const icon = header.querySelector('[data-lucide="chevron-down"]');
                const isVisible = body.style.display === 'block';
                
                // Close all other accordions
                document.querySelectorAll('.accordion-body').forEach(b => b.style.display = 'none');
                document.querySelectorAll('.accordion-header [data-lucide="chevron-down"]').forEach(i => {
                    i.style.transform = 'rotate(0deg)';
                });
                if (!isVisible) {
                    body.style.display = 'block';
                    if (icon) icon.style.transform = 'rotate(180deg)';
                } else {
                    body.style.display = 'none';
                    if (icon) icon.style.transform = 'rotate(0deg)';
                }
            });
        });
        // Initialize Lucide icons
        lucide.createIcons();
    </script>
</body>
</html>
