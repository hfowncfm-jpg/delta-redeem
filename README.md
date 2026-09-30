<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Delta Dodge</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    user-select: none;
}

body {
    background: #080b10;
    color: white;
    font-family: Arial, sans-serif;
    overflow: hidden;
    text-align: center;
}

h1 {
    margin: 15px 0 5px;
    color: #00ff88;
    font-size: 28px;
}

#game {
    position: relative;
    width: 360px;
    height: 600px;
    max-width: 95vw;
    margin: 10px auto;
    background:
        linear-gradient(rgba(0,255,136,0.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0,255,136,0.04) 1px, transparent 1px),
        #10151c;
    background-size: 30px 30px;
    border: 2px solid #00ff88;
    border-radius: 12px;
    overflow: hidden;
}

#player {
    position: absolute;
    width: 45px;
    height: 45px;
    bottom: 20px;
    left: 157px;
    background: #00ff88;
    border-radius: 8px;
    box-shadow: 0 0 20px #00ff88;
}

.enemy {
    position: absolute;
    width: 40px;
    height: 40px;
    background: #ff3344;
    border-radius: 7px;
    box-shadow: 0 0 15px #ff3344;
}

#score {
    font-size: 18px;
    margin: 5px;
}

#menu {
    margin: 10px auto;
}

button {
    border: none;
    background: #00ff88;
    color: #07100b;
    font-weight: bold;
    padding: 12px 25px;
    margin: 5px;
    border-radius: 8px;
    font-size: 16px;
}

button:active {
    transform: scale(0.95);
}

.controls {
    display: flex;
    justify-content: center;
    gap: 20px;
}

.controls button {
    width: 120px;
    height
