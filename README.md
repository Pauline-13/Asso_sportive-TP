# Asso_sportive-TP

Pour créer un bouton effet vague : 

<!-- HTML -->
<button type="submit">Click Me!</button>

<!-- CSS -->
button[type=submit] {
            padding: 15px 40px;
            font-size: 20px;
            border: none;
            border-radius: 8px;
            background-color: transparent;
            border: #cacaca solid 1px;
            color: #fff;
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        button[type=submit]::before {
            content: '';
            position: absolute;
            left: 0;
            right: 0;
            bottom: 0;
            top: 0;
            border-radius: 8px;
            z-index: -1;
        }

        button[type=submit]:hover::before {
            background-color: #03a9f4;
            animation: loadingWave 4s linear;
        }

        @keyframes loadingWave {
            0% {
                clip-path: polygon(0% 100%, 100% 100%, 99% 100%, 81% 100%, 64% 100%, 46% 100%, 29% 100%, 14% 100%, 0 100%);
            }

            10% {
                clip-path: polygon(0% 100%, 100% 100%, 100% 90%, 84% 94%, 66% 95%, 47% 94%, 31% 95%, 14% 96%, 0 94%);    
            }

            20% {
                clip-path: polygon(0% 100%, 100% 100%, 100% 74%, 81% 72%, 63% 72%, 44% 75%, 33% 77%, 16% 78%, 0 74%);                
            }

            40% {
                clip-path: polygon(0% 100%, 100% 100%, 100% 53%, 85% 55%, 67% 58%, 44% 54%, 30% 48%, 15% 47%, 0 49%);                
            }

            60% {
                clip-path: polygon(0% 100%, 100% 100%, 100% 24%, 86% 25%, 69% 29%, 53% 34%, 37% 38%, 18% 40%, 0 38%); 
            }
            
            80% {
                clip-path: polygon(0% 100%, 100% 100%, 100% 22%, 84% 29%, 67% 31%, 45% 27%, 26% 17%, 12% 14%, 0 15%);    
            }

            90% {
                clip-path: polygon(0% 100%, 100% 100%, 100% 5%, 86% 10%, 73% 10%, 55% 6%, 33% 3%, 15% 5%, 0 9%);   
            }

            100% {
                clip-path: polygon(0% 100%, 100% 100%, 100% 0, 86% 0, 71% 0, 55% 0, 34% 0, 18% 0, 0 0);    
            }
        }