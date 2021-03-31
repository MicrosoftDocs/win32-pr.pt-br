---
description: Sobre os codecs de mídia do Windows
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: Sobre os codecs de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240176de22682451814609abc94f33a52300563
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172480"
---
# <a name="about-the-windows-media-codecs"></a>Sobre os codecs de mídia do Windows

-   [Codecs de áudio do Windows Media](#windows-media-audio-codecs)
    -   [Áudio do Windows Media 9](#windows-media-audio-9)
    -   [Áudio do Windows Media 10 Professional](#windows-media-audio-10-professional)
    -   [Áudio do Windows Media 9 sem perdas](#windows-media-audio-9-lossless)
    -   [Voz do Windows Media Audio 9](#windows-media-audio-9-voice)
    -   [Compatibilidade](#compatibility)
-   [Codecs da série Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Vídeo do Windows Media 9](#windows-media-video-9-series-codecs)
    -   [Tela do Windows Media Video 9](#windows-media-video-9-screen)
    -   [Imagem do Windows Media Video 9 versão 2](#windows-media-video-9-image-version-2)
    -   [Windows Media Video 9 VCM](#windows-media-video-9-vcm)
    -   [Compatibilidade](#compatibility)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-media-audio-codecs"></a>Codecs de áudio do Windows Media

### <a name="windows-media-audio-9"></a>Áudio do Windows Media 9

Esse codec amostras de áudio em 44,1 ou 48 kilohertz (kHz) usando 16 bits, semelhante ao padrão do CD atual, oferecendo a qualidade do CD em taxas de dados de 64 a 192 kilobits por segundo (Kbps). A qualidade de som resultante é de 20% melhor do que o áudio amostrado com o Windows Media Audio 8 em taxas de dados equivalentes.

O codec do Windows Media Audio 9 (WMA 9) dá suporte à VBR (codificação de taxa de bits) variável, que permite um áudio de qualidade ainda maior em tamanhos de arquivo menores, variando automaticamente a taxa de bits de codificação de acordo com a complexidade dos dados de áudio. Com a VBR, a taxa de bits de codificação aumenta para capturar seções complexas de dados e, em seguida, diminui para maximizar a compactação das seções menos complexas, produzindo compactação compacta e de alta qualidade.

O WMA 9 é compatível com versões anteriores com decodificadores compatíveis com o Windows Media Audio, o que significa que o conteúdo do WMA 9 pode ser reproduzido com versões anteriores do Windows Media Player ou dispositivos eletrônicos mais antigos do consumidor que dão suporte à mídia do Windows. Assim como acontece com todos os codecs da série Windows Media 9, ele dá suporte à plataforma de gerenciamento de direitos digitais do Windows Media, que é usada para empacotar e distribuir mídia digital protegida por cópia com segurança.

### <a name="windows-media-audio-10-professional"></a>Áudio do Windows Media 10 Professional

O Windows Media Audio 10 Professional (WMA 10 pro) é o codec de áudio de mídia do Windows mais flexível disponível – os perfis de suporte que incluem tudo, desde áudio de resolução completa de 24 bits/96 kHz em estéreo, canal de 5,1 ou até mesmo 7,1 de som surround de canal, até recursos móveis altamente eficientes a 24 96 kbps para o som 128 do canal de 256. O WMA 10 Pro oferece uma qualidade incrível para os consumidores que usam hardware de alta fidelidade e computadores equipados com surround de canal de 5,1, e para consumidores que reproduzem conteúdo de áudio em seus dispositivos móveis. O WMA 10 pro dá suporte a streaming, download progressivo ou entrega de download e reprodução às 128 a 768 Kbps.

Ao usar o áudio surround sound 5,1 compactado em 384 Kbps com o WMA 10 pro, a maioria dos ouvintes não pode discernir nenhuma diferença entre a música compactada e os arquivos PCM (modulação de código de pulso) originais. O WMA pro também oferece controle de intervalo dinâmico usando as amplitudes de áudio máxima e média calculadas durante o processo de codificação. Usando o recurso de modo silencioso no Windows Media Player 9 e posterior, os usuários podem ouvir o intervalo dinâmico completo, um intervalo de diferença média de até 12 decibéis (dB) acima da média ou um pequeno intervalo de diferença de até 6 dB acima da média.

Se um usuário tentar reproduzir um arquivo que foi codificado usando o canal 5,1, recursos de amostragem de 24 bits, 96 kHz, mas não tem um sistema ou placa de som que dá suporte a som de alta resolução ou de vários canais, vários canais são combinados em áudio estéreo (por exemplo, 16 bits, dois canais de áudio), garantindo que os usuários obtenham a melhor experiência de reprodução que seus sistemas podem fornecer.

A tabela a seguir compara o WMA pro com a tecnologia de compactação em competição.



| Dados de áudio              | Compactação do setor\*        | Mídia do Windows\*            | Economia de compactação |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 ch x 48 kHz x 16 bits | Dolby Digital 2,0 a 220 kbps | WMA 10 pro a 128 kbps     | 1.7:1               |
| 6 ch x 48 kHz x 20 bits | Dolby Digital 5,1 a 384 kbps | WMA 10 pro a 192 – 256 kbps | 1,5 – 2:1             |
| 6 ch x 48 kHz x 24 bits | DTS 5,1 a 1.536 kbps         | WMA 10 pro a 768 Kbps     | 2:1                 |



 

\* Dependente de conteúdo

### <a name="windows-media-audio-9-lossless"></a>Áudio do Windows Media 9 sem perdas

A qualidade de áudio do conteúdo que é compactada usando esse codec é o melhor de todos os codecs de áudio do Windows Media. Ele cria uma duplicata bit a bit do arquivo de áudio original para que nenhum dado seja perdido, o que o torna ideal para o arquivamento de mestres de conteúdo.

Dependendo da complexidade do original, o conteúdo será compactado com uma proporção de 2:1 ou 3:1. Embora isso seja menor do que a taxa obtida com outros codecs da série Windows Media Audio 9, ele fornece os mesmos benefícios de compactação, deixando os dados intactos.

Como o Windows Media Audio 9 Professional, o codec Windows Media Audio 9 Lossless também oferece controle de intervalo dinâmico usando as amplitudes de áudio máxima e média calculadas durante o processo de codificação. Usando o recurso de modo silencioso no Windows Media Player 9 e posterior, os usuários podem ouvir o intervalo dinâmico completo, um intervalo de diferença média de até 12 dB acima da média ou um pequeno intervalo de diferenças de até 6 dB acima da média.

### <a name="windows-media-audio-9-voice"></a>Voz do Windows Media Audio 9

Esse codec de taxa de bits baixa é direcionado principalmente para conteúdo de fala, mas é executado muito bem com conteúdo de modo misto que inclui voz e música. No modo de voz, o codec aproveita a faixa de frequência relativamente menos complicada e mais estreita da voz humana para maximizar a compactação. No modo música, o codec funciona como o codec padrão do Windows Media Audio 9. O conteúdo codificado pode ser configurado para alternar entre os modos de voz e música automaticamente.

O codec de voz do Windows Media Audio 9 oferece qualidade superior para cenários de streaming de taxa de bits baixa (menos de 20 kbps), como difusões de rádio, publicidade, livros eletrônicos, podcasts e voz. O codec de voz também pode compactar conteúdo para até 4 kbps a 8 kHz.

### <a name="compatibility"></a>Compatibilidade

A tabela a seguir descreve o que seu público-alvo terá ao executar o conteúdo do Windows Media Audio 9 Series em sistemas operacionais anteriores do Microsoft Windows do que no Windows XP ou em versões anteriores do Windows Media Player. Esta tabela também lista a compatibilidade para o Apple Mac OS X e plataformas baseadas em Windows CE.



| Codec                              | Recurso                                       | Compatibilidade com versões anteriores do Player                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Áudio do Windows Media 9              | Codificação de taxa de bits constante (CBR)              | <dl> <dt>Windows Media Player 6,4 ou posterior em dispositivos não portáteis (usando transcodificação conforme necessário)</dt> <dt>Windows Media Player 9 para Mac os X</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 para Pocket \* PC</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 para Smartphone \* </dt> </dl> |
|                                    | Codificação de taxa de bits variável (VBR)              | Windows Media Player 7 ou posterior em todos os dispositivos que dão suporte ao Player (usando transcodificação conforme necessário)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Áudio do Windows Media 9 Professional | Geral                                       | <dl> <dt>Windows Media Player 7 ou posterior</dt> <dt>Windows Media player 9 para Mac os X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reprodução de canal discreto (por exemplo, 5,1) | Requer o Windows Media Player 9 Series (ou SDK) ou posterior, o Windows XP e uma placa de áudio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | Áudio de alta resolução (24 bits, 96 kHz)        | Requer o Windows Media Player 9 Series (ou SDK) ou posterior, o Windows XP e um cartão de áudio de alta resolução.                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | Controle de intervalo dinâmico                         | Requer o Windows Media Player 9 Series (ou SDK) ou posterior e o Windows XP.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Áudio do Windows Media 9 sem perdas     | Geral                                       | <dl> <dt>Windows Media Player 7 ou posterior</dt> <dt>Windows Media player 9 para Mac os X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reprodução de canal discreto (por exemplo, 5,1) | Requer o Windows Media Player 9 Series (ou SDK) ou posterior, o Windows XP e uma placa de áudio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Voz do Windows Media Audio 9        | Geral                                       | <dl> Windows <dt>Media Player 6,4 ou posterior</dt> <dt>Windows Media Player 9 para Mac os X</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 para Pocket PC \* </dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 para Smartphone \* </dt> </dl>                                                       |



 

> [!Note]  
> \* Todas as versões do Windows Media Player para Pocket PC e Smartphone são fornecidas como parte do sistema operacional Microsoft Windows Mobile. O Windows Media Player para Pocket PC e o Windows Media Player para Smartphone não estão disponíveis para download da Microsoft.

 

## <a name="windows-media-video-9-series-codecs"></a>Codecs da série Windows Media Video 9

Em 2006, a sociedade de imagem e os engenheiros de televisão (SMPTE) publicaram formalmente a especificação final para SMPTE 421M, também conhecida como VC-1. A padronização formal do VC-1 representa a culminação de anos de investigação técnica de mais de 75 empresas, levando a um codec bem documentado, extremamente estável, fácil de licenciamento e aceito pelo setor. O VC-1 dá suporte a três perfis: simples, principal e avançado. Os perfis simples e principal foram concluídos por vários anos, e implementações existentes, como o WMV 9, têm suporte da criação e reprodução de conteúdo usando esses perfis, bem como uma implementação antecipada do perfil avançado. A conclusão do perfil avançado e da padronização resultante de todos os perfis no VC-1 representa a etapa final em uma especificação abrangente que fornece conteúdo de alta definição, entrelaçado ou progressivo, em qualquer meio e em qualquer dispositivo compatível.

### <a name="windows-media-video-9"></a>Vídeo do Windows Media 9

O Windows Media Video 9 é a implementação da Microsoft do padrão do VC-1 SMPTE. Ele dá suporte a perfis simples, principais e avançados.

### <a name="simple-and-main-profiles"></a>Perfis simples e principais

Os perfis simples e principais do vídeo do Windows Media 9 estão em conformidade com o padrão SMPTE VC-1 e fornecem vídeo de alta qualidade para streaming e download. Esses perfis dão suporte a uma ampla gama de taxas de bits, de conteúdo de alta definição em uma metade a uma taxa de bits de MPEG-2, até o vídeo da Internet com taxa de bits baixa entregue por um modem dial-up. Esse codec também dá suporte a vídeo que pode ser baixado com qualidade profissional com codificação de duas passagens e taxa de bits variável (VBR). O Windows Media Video 9 já tem suporte por uma ampla variedade de players e dispositivos.

### <a name="advanced-profile"></a>Perfil avançado

O perfil avançado do Windows Media Video 9 está em conformidade com o padrão SMPTE VC-1, dá suporte a conteúdo entrelaçado e é independente de transporte. Os criadores de conteúdo podem usar esse perfil para fornecer conteúdo progressivo ou entrelaçado em taxas de dados como um terço do codec MPEG-2, com a mesma qualidade de MPEG-2.

No passado, o conteúdo de vídeo entrelaçado era sempre desentrelaçado antes da codificação com o codec de vídeo do Windows Media. Agora, a codificação de aplicativos, como o Windows Media 9 Series, e soluções de codificação de terceiros podem dar suporte à compactação de conteúdo entrelaçado sem primeiro convertê-lo em conteúdo progressivo. Manter o entrelaçamento em um arquivo codificado é importante se o conteúdo for renderizado em uma exibição entrelaçada, como uma televisão.

A independência de transporte também permite a entrega do perfil avançado do Windows Media Video 9 em sistemas que não são baseados no Windows Media, como infraestruturas de difusão baseadas em padrões (por meio de fluxos de transporte MPEG-2 nativos), infraestruturas sem fio (usando RTP de protocolo de transferência em tempo real \[ \] ) ou até mesmo DVDs.

A tabela a seguir compara o perfil avançado do Windows Media Video 9 com a tecnologia de compactação de concorrência.



| Dados de vídeo                                                  | Compactação do setor\* | Mídia do Windows\*                                      | Economia de compactação |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720x480 pixels/quadro x 8 bits por canal x 24 fps  | MPEG-2 a 4 – 6 Mbps     | Perfil do Windows Media Video 9 avançado a 1,3 – 2 Mbps | 3:1                 |
| 480/30i 720x480 pixels/quadro x 8 bits por canal x 30 fps  | MPEG-2 em 6 a 8 Mbps     | Perfil avançado do Windows Media Video 9 com 2 a 4 Mbps   | 2 – 3:1               |
| 720/24p 1280x720 pixels/quadro x 8 bits por canal x 24 fps | MPEG-2 a 19 Mbps      | Perfil avançado do Windows Media Video 9 com 5 a 8 Mbps   | 2.4 – 3,8:1           |



 

\*Dependente de conteúdo

### <a name="windows-media-video-9-screen"></a>Tela do Windows Media Video 9

O codec de tela do Windows Media Video 9 é otimizado para compactação de capturas de tela sequenciais e vídeos altamente estáticos que são capturados na exibição do computador, o que o torna ideal para a entrega de demonstrações ou a demonstração do uso do computador para treinamento. O codec aproveita a simplicidade de imagem típica e a falta de movimento relativa para atingir uma taxa de compactação muito alta.

Durante o processo de codificação, o codec alterna automaticamente entre os modos de codificação com e sem perdas, dependendo da complexidade dos dados de vídeo. Para dados complexos, o modo sem perdas preserva uma cópia exata dos dados. Para dados menos complexos, o modo de perda descarta alguns dados para atingir uma taxa de compactação maior. Alternando automaticamente entre esses dois modos, o codec mantém a qualidade do vídeo ao mesmo tempo em que maximiza a compactação.

Em geral, o codec de tela do Windows Media Video 9 oferece melhor manipulação de imagens de bitmap e de movimentos de tela, mesmo em CPUs relativamente modestas. Ele também é de até 100 vezes mais eficiente do que a codificação de comprimento de execução comumente usada.

### <a name="windows-media-video-9-image-version-2"></a>Imagem do Windows Media Video 9 versão 2

O codec de imagem do Windows Media Video 9 versão 2 é diferente dos outros codecs de vídeo. Em vez de processar vídeo descompactado, ele transforma imagens ainda em vídeo usando a panorâmica, o zoom e as transições de esmaecimento cruzado entre os clipes para criar um número ilimitado de efeitos.

Os resultados podem ser entregues em taxas de dados como 20 kilobits por segundo (Kbps). Esses arquivos são compactados usando a taxa de bits constante (CBR) ou modos de taxa de bits variável (VBR) de uma passagem.

> [!Note]  
> O codec de imagem do Windows Media Video 9 versão 2 não é compatível com o codec de imagem do Windows Media Video 9.

 

### <a name="windows-media-video-9-vcm"></a>Windows Media Video 9 VCM

A versão do Gerenciador de compactação de vídeo (VCM) do codec da série Windows Media Video 9 permite versões anteriores de codificação e edição de aplicativos para dar suporte ao codec da série Windows Media Video 9 em contêineres de arquivos, como AVI (vídeo de áudio Intercalado). Esse pacote de codec também permite que arquivos de vídeo do Windows Media (WMV) com base no Windows Media Format 9 Series sejam reproduzidos no Windows Media Player 6,4, nos contêineres de arquivos ASF e AVI.

### <a name="compatibility"></a>Compatibilidade

A tabela a seguir descreve o que seu público-alvo terá ao reproduzir conteúdo do Windows Media Video 9 Series em sistemas operacionais Microsoft Windows anteriores ou em versões anteriores do Windows Media Player. Esta tabela também lista a compatibilidade para o Apple Mac OS X e plataformas baseadas em Windows CE.



| Codec                                  | Recurso             | Compatibilidade com versões anteriores do Player                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vídeo do Windows Media 9                  | Geral             | <dl> Windows <dt>Media Player 6,4 ou posterior</dt> <dt>Windows Media Player 9 para Mac os X</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 para Pocket PC \* </dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 para Smartphone \* </dt> </dl> |
|                                        | Interpolação de quadros | Requer o Windows Media Player 9 Series (ou Software Development Kit) ou posterior e o Windows XP.                                                                                                                                                                                                                                                                                                                                                                           |
| Perfil avançado do Windows Media Video 9 | Geral             | Windows Media Player 7 ou posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Tela do Windows Media Video 9           | Geral             | Windows Media Player 7 ou posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Imagem do Windows Media Video 9 versão 2  | Geral             | Windows Media Player 7 ou posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Todas as versões do Windows Media Player para Pocket PC e Smartphone são fornecidas como parte do sistema operacional Microsoft Windows Mobile. O Windows Media Player para Pocket PC e o Windows Media Player para Smartphone não estão disponíveis para download da Microsoft.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



