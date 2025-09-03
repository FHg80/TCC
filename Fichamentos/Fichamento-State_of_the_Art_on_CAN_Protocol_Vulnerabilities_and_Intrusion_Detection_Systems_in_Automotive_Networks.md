# State of the Art on CAN Protocol Vulnerabilities and Intrusion Detection Systems in Automotive Networks

DAROUICHE, M. S.; TAZI, E.; SATORI, H. "State of the Art on CAN Protocol Vulnerabilities and Intrusion Detection Systems in Automotive Networks," in: 2024 3rd International Conference on Embedded Systems and Artificial Intelligence (ESAI). [s.l.] IEEE, 2024. doi: [10.1109/ESAI62891.2024.10913954](https://doi.org/10.1109/ESAI62891.2024.10913954).

## 1. Fichamento de Conteúdo 

O artigo apresenta uma análise sobre a segurança em redes automotivas, focando no protocolo CAN (_Controller Area Network_), que é o principal meio de comunicação entre as Unidades de Controle Eletrônico (ECUs) em veículos modernos. Os autores destacam que o protocolo CAN, por não ter sido projetado com a cibersegurança em mente, possui vulnerabilidades significativas que o tornam suscetível a ataques como _spoofing_ de mensagens, _eavesdropping_ e ataques de negação de serviço (DoS). Como principal contramedida, o estudo aborda os Sistemas de Detecção de Intrusão (IDS), que monitoram a rede para identificar e bloquear atividades maliciosas. O texto explora e compara diferentes técnicas de IDS, como as baseadas em assinatura, anomalia, aprendizado de máquina, entropia e voltagem, discutindo suas vantagens e desvantagens. O artigo conclui que, apesar dos avanços, existem desafios importantes, como altas taxas de falsos positivos, restrições de recursos de hardware nos veículos e a necessidade de adaptação a ameaças em constante evolução. Por fim, são apontadas direções para pesquisas futuras, incluindo o desenvolvimento de algoritmos mais eficientes e leves, a adaptabilidade em tempo real e a criação de padrões de avaliação (_benchmarks_) para comparar as diferentes soluções de IDS.

## 2. Fichamento Bibliográfico

* _CAN (Controller Area Network) Protocol (protocolo de controlador de rede em área)_ é o principal protocolo de comunicação em veículos modernos, permitindo a comunicação em tempo real entre diferentes Unidades de Controle Eletrônico (página 1).
* _ECU (Electronic Control Units - unidade de controle eletrônico)_ unidades de controle eletrônico conectadas à rede de um veículo que se comunicam através do protocolo CAN (página 1).
* _Message Spoofing (falsificação de mensagem)_ um tipo de ataque onde o invasor injeta mensagens falsas na rede CAN para se passar por uma ECU legítima e controlar funções críticas do veículo (página 1).
* _Eavesdropping (interceptação)_ ataque que explora a falta de criptografia das mensagens CAN, permitindo que um invasor leia, analise e realize engenharia reversa das comunicações da rede (página 2).
* _DoS (Denial of Service) Attacks (ataques de negação de serviço)_ consiste em inundar a rede CAN com mensagens de alta prioridade para perturbar a comunicação normal entre as ECUs, podendo desabilitar sistemas de segurança (página 2).
* _IDS (Intrusion Detection Systems - sistemas de detecção de intrusão)_ soluções de segurança que monitoram a atividade da rede para identificar potenciais violações e bloquear ataques antes que causem danos significativos (página 1).
* _Signature-based detection (detecção baseada em assinatura)_ técnica de IDS que compara o tráfego da rede com um banco de dados de assinaturas de ataques conhecidos. É eficaz contra ameaças conhecidas, mas ineficaz contra ataques novos (página 2).
* _Anomaly-based detection (detecção baseada em anomalia)_ técnica de IDS que estabelece um perfil de comportamento normal da rede e sinaliza qualquer desvio como uma possível ameaça. É mais eficaz contra ataques novos, mas pode gerar uma alta taxa de falsos positivos (página 2).

## 3. Fichamento de Citações

* _"Although the CAN protocol is widely used, it was not initially created with cybersecurity in consideration, leaving it open to different cyberattacks [1]."_
* _"IDS solutions are crucial for monitoring network activity, identifying potential breaches, and blocking attacks before they result in significant harm."_
* _"This method is more effective at detecting new and unknown attacks but may produce a higher rate of false positives."_
* _"Anomaly based IDS is known for its effectiveness to detect new and unknown attacks but suffer from the high positives rate that can easily mislead the system with false alerts, leading to a reduction of the overall efficiency of the IDS."_
* _"Therefore, IDS solutions with high complexity would be difficult to implement."_
* _"The lack of standardized evaluation metrics for IDS in automotive networks has made it difficult to compare the effectiveness of different solutions."_