<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>NGUYỄN ĐỨC NHÂN | HOME</title>
    
    <!-- Font chữ giống nguyên bản -->
    <link href="https://fonts.googleapis.com/css2?family=Righteous&family=Saira+Condensed:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>
    
    <style>
        *{margin:0;padding:0;box-sizing:border-box}
        :root{
            --bg-main:#0f111a;
            --bg-card:rgba(15,17,26,0.85);
            --accent-cyan:#00ffff;
            --accent-pink:#ff7eb8;
            --text-primary:#e6e6e6;
            --text-secondary:#888ea8;
            --border-glow:rgba(0,255,255,0.25);
        }
        body{
            background:var(--bg-main);
            min-height:100vh;
            font-family:'Saira Condensed',sans-serif;
            color:var(--text-primary);
            overflow-x:hidden;
            position:relative;
        }
        
        /* ===== HOA ANH ĐÀO RƠI ===== */
        .petal{
            position:fixed;
            width:14px;height:14px;
            background:linear-gradient(135deg,#ffd6e0,#ffb3c6);
            border-radius:50% 0 50% 50%;
            opacity:0.75;
            pointer-events:none;
            z-index:2;
            animation:fall linear infinite;
            filter:drop-shadow(0 0 2px rgba(255,180,200,0.4));
        }
        @keyframes fall{
            0%{transform:translateY(-15px) rotate(0deg);opacity:0.85}
            50%{opacity:0.6}
            100%{transform:translateY(105vh) rotate(420deg);opacity:0}
        }
        
        /* ===== NỀN & KẾT CẤU ===== */
        .bg-overlay{
            position:fixed;inset:0;
            background:radial-gradient(circle at top, rgba(0,255,255,0.06), transparent 55%),
                        radial-gradient(circle at bottom right, rgba(255,126,184,0.05), transparent 55%);
            z-index:0;
        }
        .container{
            max-width:680px;
            margin:0 auto;
            padding:0 15px;
            position:relative;z-index:10;
        }
        
        /* ===== THANH ĐIỀU HƯỞNG TRÊN ===== */
        .topbar{
            display:flex;justify-content:space-between;align-items:center;
            padding:14px 10px;border-bottom:1px solid var(--border-glow);
            margin-bottom:25px;
        }
        .brand{
            font-family:'Righteous',cursive;
            font-size:21px;letter-spacing:1.5px;
            color:var(--accent-cyan);
            text-shadow:0 0 8px rgba(0,255,255,0.4);
        }
        .navmenu a{
            color:var(--text-secondary);
            text-decoration:none;
            font-size:14px;font-weight:600;
            margin-left:18px;
            text-transform:uppercase;
            transition:all 0.25s;
        }
        .navmenu a.active{color:var(--accent-cyan);text-shadow:0 0 6px rgba(0,255,255,0.3)}
        .navmenu a:hover{color:var(--accent-cyan)}
        .fps-tag{
            font-size:12px;color:var(--accent-cyan);
            font-family:monospace;background:rgba(0,255,255,0.08);
            padding:3px 8px;border-radius:4px;
        }
        
        /* ===== KHỐI CHÍNH ===== */
        .profile-card{
            background:var(--bg-card);
            border:1px solid var(--border-glow);
            border-radius:12px;
            padding:35px 25px;
            box-shadow:0 0 25px rgba(0,255,255,0.08), inset 0 0 40px rgba(0,255,255,0.03);
            backdrop-filter:blur(8px);
        }
        .avatar-wrap{text-align:center;margin-bottom:18px}
        .avatar{
            width:140px;height:140px;border-radius:50%;
            object-fit:cover;border:3px solid var(--accent-cyan);
            box-shadow:0 0 20px rgba(0,255,255,0.35),
                        inset 0 0 12px rgba(0,255,255,0.15);
        }
        .name-row{
            text-align:center;margin-bottom:10px;
        }
        .fullname{
            font-family:'Righteous',cursive;
            font-size:26px;
            color:#fff;
            display:inline-flex;align-items:center;gap:8px;
        }
        .verified-badge{
            width:22px;height:22px;border-radius:50%;
            background:linear-gradient(135deg,#2ecc71,#27ae60);
            display:inline-flex;align-items:center;justify-content:center;
            font-size:12px;color:#fff;box-shadow:0 0 8px rgba(46,204,113,0.35);
        }
        .greeting{
            text-align:center;
            font-size:16px;color:var(--accent-cyan);
            margin-bottom:6px;
            font-weight:600;
        }
        .sub-info{
            text-align:center;
            font-size:14px;color:var(--text-secondary);
            line-height:1.7;
            margin-bottom:8px;
        }
        .highlight-text{color:#ffd700}
        .divider{
            height:1px;
            background:linear-gradient(90deg, transparent, var(--border-glow), transparent);
            margin:28px 0;
        }
        .section-heading{
            font-size:15px;color:var(--text-secondary);
            text-transform:uppercase;letter-spacing:1px;
            margin-bottom:16px;
            display:flex;align-items:center;gap:8px;
        }
        .section-heading::after{
            content:'';flex:1;height:1px;background:var(--border-glow);
        }
        
        /* ===== NÚT MẠNG XÃ HỘI ===== */
        .social-btn{
            display:flex;align-items:center;justify-content:space-between;
            padding:13px 20px;border-radius:8px;
            color:#fff;text-decoration:none;font-weight:600;
            margin-bottom:10px;transition:all 0.3s;
            border:1px solid rgba(255,255,255,0.08);
        }
        .social-btn:hover{
            transform:translateY(-2px);
            box-shadow:0 6px 18px rgba(0,0,0,0.3);
        }
        .fb{background:linear-gradient(90deg,#1877f2,#2b80f4)}
        .yt{background:linear-gradient(90deg,#e62117,#ff2e2e)}
        .dc{background:linear-gradient(90deg,#5865f2,#7289da)}
        .tg{background:linear-gradient(90deg,#0088cc,#229edc)}
        .zalo{background:linear-gradient(90deg,#00c300,#7dd42f)}
        .btn-left{display:flex;align-items:center;gap:10px}
        .btn-meta{font-size:12px;opacity:0.75;font-weight:400}
        
        /* ===== NHÂN VẬT TRANG TRÍ BÊN DƯỚI ===== */
        .char-deco{
            position:fixed;bottom:0;r...
