---
description: sobre os codecs de mídia Windows
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: sobre os codecs de mídia Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 319f7ab16eea462233df994f32b3e3128997f1074e3c7ff69df9885b437f2783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065486"
---
# <a name="about-the-windows-media-codecs"></a>sobre os codecs de mídia Windows

-   [Windows Codecs de áudio de mídia](#windows-media-audio-codecs)
    -   [Windows Áudio de mídia 9](#windows-media-audio-9)
    -   [Windows Áudio de mídia 10 Professional](#windows-media-audio-10-professional)
    -   [Windows Áudio de mídia 9 sem perdas](#windows-media-audio-9-lossless)
    -   [Windows Voz de áudio de mídia 9](#windows-media-audio-9-voice)
    -   [Compatibilidade](#compatibility)
-   [Windows Codecs da Media Video 9 Series](#windows-media-video-9-series-codecs)
    -   [Windows Vídeo de mídia 9](#windows-media-video-9-series-codecs)
    -   [Windows Tela de vídeo de mídia 9](#windows-media-video-9-screen)
    -   [Windows Imagem de vídeo de mídia 9 versão 2](#windows-media-video-9-image-version-2)
    -   [Windows Vídeo de mídia 9 VCM](#windows-media-video-9-vcm)
    -   [Compatibilidade](#compatibility)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-media-audio-codecs"></a>Windows Codecs de áudio de mídia

### <a name="windows-media-audio-9"></a>Windows Áudio de mídia 9

Esse codec amostras de áudio em 44,1 ou 48 kilohertz (kHz) usando 16 bits, semelhante ao padrão do CD atual, oferecendo a qualidade do CD em taxas de dados de 64 a 192 kilobits por segundo (Kbps). a qualidade de som resultante é de 20% melhor do que o áudio de amostra com Windows mídia de áudio 8 em taxas de dados equivalentes.

o codec Windows Media Audio 9 (WMA 9) dá suporte à VBR (codificação de taxa de bits) variável, que permite um áudio de qualidade ainda maior em tamanhos de arquivo menores, variando automaticamente a taxa de bits de codificação de acordo com a complexidade dos dados de áudio. Com a VBR, a taxa de bits de codificação aumenta para capturar seções complexas de dados e, em seguida, diminui para maximizar a compactação das seções menos complexas, produzindo compactação compacta e de alta qualidade.

o wma 9 é compatível com versões anteriores com decodificadores de mídia Windows com áudio anteriores, o que significa que o conteúdo do WMA 9 pode ser reproduzido com versões anteriores de Windows Media Player ou dispositivos eletrônicos mais antigos que dão suporte à mídia Windows. assim como acontece com todos os Windows codecs da série 9 media, ele dá suporte à plataforma de gerenciamento de direitos digitais de mídia Windows, que é usada para empacotar e distribuir mídia digital protegida por cópia com segurança.

### <a name="windows-media-audio-10-professional"></a>Windows Áudio de mídia 10 Professional

Windows o áudio de mídia 10 Professional (WMA 10 Pro) é o codec de áudio de mídia mais flexível Windows disponível – perfis de suporte que incluem tudo, desde áudio de resolução completa de 24 bits/96 kHz em estéreo, canal de 5,1 ou até mesmo 7,1 canais surround sound, para recursos móveis altamente eficientes a 24 128 96 kbps para o áudio de canal de 256. o WMA 10 Pro oferece qualidade incrível para consumidores que usam hardware de alta fidelidade e computadores equipados com surround de canal de 5,1, e para consumidores que reproduzem conteúdo de áudio em seus dispositivos móveis. o WMA 10 Pro dá suporte a streaming, download progressivo ou entrega de download e reprodução às 128 a 768 Kbps.

ao usar o áudio surround sound 5,1 compactado em 384 Kbps com o WMA 10 Pro, a maioria dos ouvintes não pode discernir nenhuma diferença entre a música compactada e os arquivos PCM (modulação de código de pulso) originais. o WMA Pro também oferece controle de intervalo dinâmico usando as amplitudes de áudio máxima e média calculadas durante o processo de codificação. usando o recurso de modo silencioso no Windows Media Player 9 e posteriores, os usuários podem ouvir o intervalo dinâmico completo, um intervalo de diferença média de até 12 decibéis (dB) acima da média ou um pequeno intervalo de diferenças de até 6 dB acima da média.

Se um usuário tentar reproduzir um arquivo que foi codificado usando o canal 5,1, recursos de amostragem de 24 bits, 96 kHz, mas não tem um sistema ou placa de som que dá suporte a som de alta resolução ou de vários canais, vários canais são combinados em áudio estéreo (por exemplo, 16 bits, dois canais de áudio), garantindo que os usuários obtenham a melhor experiência de reprodução que seus sistemas podem fornecer.

a tabela a seguir compara Pro WMA com a tecnologia de compactação em competição.



| Dados de áudio              | Compactação do setor\*        | Windows Meio\*            | Economia de compactação |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 ch x 48 kHz x 16 bits | Dolby Digital 2,0 a 220 kbps | Pro de WMA 10 a 128 Kbps     | 1.7:1               |
| 6 ch x 48 kHz x 20 bits | Dolby Digital 5,1 a 384 kbps | WMA 10 Pro em 192 a 256 Kbps | 1,5 – 2:1             |
| 6 ch x 48 kHz x 24 bits | DTS 5,1 a 1.536 kbps         | Pro de WMA 10 a 768 Kbps     | 2:1                 |



 

\* Dependente de conteúdo

### <a name="windows-media-audio-9-lossless"></a>Windows Áudio de mídia 9 sem perdas

a qualidade de áudio do conteúdo que é compactada usando esse codec é o melhor de todos os Windows codecs de áudio de mídia. Ele cria uma duplicata bit a bit do arquivo de áudio original para que nenhum dado seja perdido, o que o torna ideal para o arquivamento de mestres de conteúdo.

Dependendo da complexidade do original, o conteúdo será compactado com uma proporção de 2:1 ou 3:1. embora isso seja menor do que a taxa obtida com outros Windows codecs de mídia de áudio 9 Series, ele fornece os mesmos benefícios de compactação, deixando os dados intactos.

assim como Windows media audio 9 Professional, o codec de mídia de áudio 9 sem perdas do Windows também oferece controle de intervalo dinâmico usando as amplitudes de áudio máximo e média calculadas durante o processo de codificação. usando o recurso de modo silencioso no Windows Media Player 9 e posterior, os usuários podem ouvir o intervalo dinâmico completo, um intervalo de diferença média de até 12 db acima da média ou um pequeno intervalo de diferenças de até 6 db acima da média.

### <a name="windows-media-audio-9-voice"></a>Windows Voz de áudio de mídia 9

Esse codec de taxa de bits baixa é direcionado principalmente para conteúdo de fala, mas é executado muito bem com conteúdo de modo misto que inclui voz e música. No modo de voz, o codec aproveita a faixa de frequência relativamente menos complicada e mais estreita da voz humana para maximizar a compactação. no modo de música, o codec funciona como o codec padrão Windows Media Audio 9. O conteúdo codificado pode ser configurado para alternar entre os modos de voz e música automaticamente.

o codec de voz Windows Media Audio 9 oferece qualidade superior para cenários de streaming de taxa de bits baixa (menos de 20 Kbps), como difusões de rádio, publicidade, livros eletrônicos, podcasts e voz. O codec de voz também pode compactar conteúdo para até 4 kbps a 8 kHz.

### <a name="compatibility"></a>Compatibilidade

a tabela a seguir descreve o que seu público-alvo terá ao reproduzir Windows conteúdo do Media Audio 9 Series em sistemas operacionais anteriores do Microsoft Windows do que Windows XP ou com versões anteriores do Windows Media Player. esta tabela também lista a compatibilidade para o Apple Mac OS X e plataformas baseadas em Windows CE.



| Codec                              | Recurso                                       | Compatibilidade com versões anteriores do Player                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Áudio de mídia 9              | Codificação de taxa de bits constante (CBR)              | <dl> <dt>Windows Media Player 6,4 ou posterior em dispositivos não portáteis (usando transcodificação conforme necessário)</dt> <dt>Windows Media Player 9 para Mac OS X</dt> <dt>Windows Media Player 9 series e Windows Media Player 9,1 para Pocket PC \* a</dt> <dt>série 9 Windows Media Player e Windows Media Player 9,1 para Smartphone \* </dt> </dl> |
|                                    | Codificação de taxa de bits variável (VBR)              | Windows Media Player 7 ou posterior em todos os dispositivos que dão suporte ao Player (usando transcodificação conforme necessário)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Áudio de mídia 9 Professional | Geral                                       | <dl> <dt>Windows Media Player 7 ou posterior</dt> <dt>Windows Media Player 9 para Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reprodução de canal discreto (por exemplo, 5,1) | requer o Windows Media Player 9 Series (ou SDK) ou posterior, Windows XP e uma placa de áudio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | Áudio de alta resolução (24 bits, 96 kHz)        | requer o Windows Media Player 9 Series (ou SDK) ou posterior, Windows XP e uma placa de áudio de alta resolução.                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | Controle de intervalo dinâmico                         | requer o Windows Media Player 9 Series (ou SDK) ou posterior e Windows XP.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Windows Áudio de mídia 9 sem perdas     | Geral                                       | <dl> <dt>Windows Media Player 7 ou posterior</dt> <dt>Windows Media Player 9 para Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reprodução de canal discreto (por exemplo, 5,1) | requer o Windows Media Player 9 Series (ou SDK) ou posterior, Windows XP e uma placa de áudio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Voz de áudio de mídia 9        | Geral                                       | <dl> <dt>Windows Media Player 6,4 ou posterior</dt> <dt>Windows Media Player 9 para Mac OS X</dt> <dt>Windows Media Player 9 series e Windows Media Player 9,1 para o \* Pocket PC</dt> <dt>Windows Media Player 9 series e o Windows Media Player 9,1 \* for Smartphone</dt> </dl>                                                       |



 

> [!Note]  
> \*todas as versões do Windows Media Player para Pocket PC e Smartphone são fornecidas como parte do sistema operacional Microsoft Windows Mobile. Windows Media Player para Pocket PC e Windows Media Player para Smartphone não estão disponíveis para download da Microsoft.

 

## <a name="windows-media-video-9-series-codecs"></a>Windows Codecs da Media Video 9 Series

Em 2006, a sociedade de imagem e os engenheiros de televisão (SMPTE) publicaram formalmente a especificação final para SMPTE 421M, também conhecida como VC-1. A padronização formal do VC-1 representa a culminação de anos de investigação técnica de mais de 75 empresas, levando a um codec bem documentado, extremamente estável, fácil de licenciamento e aceito pelo setor. O VC-1 dá suporte a três perfis: simples, principal e avançado. Os perfis simples e principal foram concluídos por vários anos, e implementações existentes, como o WMV 9, têm suporte da criação e reprodução de conteúdo usando esses perfis, bem como uma implementação antecipada do perfil avançado. A conclusão do perfil avançado e da padronização resultante de todos os perfis no VC-1 representa a etapa final em uma especificação abrangente que fornece conteúdo de alta definição, entrelaçado ou progressivo, em qualquer meio e em qualquer dispositivo compatível.

### <a name="windows-media-video-9"></a>Windows Vídeo de mídia 9

Windows O Vídeo de Mídia 9 é a implementação da Microsoft do padrão VC-1 SMPTE. Ele dá suporte a perfis Simples, Principal e Avançado.

### <a name="simple-and-main-profiles"></a>Perfis simples e principais

Os perfis Windows Media Video 9 Simple e Main estão totalmente em conformidade com o padrão SMPTE VC-1 e fornecem vídeo de alta qualidade para streaming e download. Esses perfis são compatíveis com uma ampla gama de taxas de bits, desde o conteúdo de alta definição de um a metade a um terceiro da taxa de bits do MPEG-2, até o vídeo de Internet de baixa taxa de bits entregue em um modem discado. Esse codec também dá suporte a vídeo para download de qualidade profissional com codificação VBR (taxa de bits variável e de duas passagem). Windows O Vídeo de Mídia 9 já é compatível com uma ampla variedade de players e dispositivos.

### <a name="advanced-profile"></a>Perfil Avançado

O perfil Windows Media Video 9 Advanced está totalmente em conformidade com o padrão SMPTE VC-1, dá suporte a conteúdo entrelaçado e é independente de transporte. Os criadores de conteúdo podem usar esse perfil para fornecer conteúdo progressivo ou entrelaçado a taxas de dados tão baixas quanto um terceiro do codec MPEG-2 — com a mesma qualidade que MPEG-2.

No passado, o conteúdo do vídeo entrelaçado sempre era desacalçado antes da codificação com o codec Windows Media Video. Agora, a codificação de aplicativos como o Windows Media 9 Series e soluções de codificação de terceiros pode dar suporte à compactação de conteúdo entrelaçado sem primeiro convertê-lo em conteúdo progressivo. Manter o entrelaçamento em um arquivo codificado é importante se o conteúdo for renderizado em uma exibição entrelaçada, como uma tv.

A independência de transporte também permite a entrega do perfil avançado do Windows Media Video Windows 9 em sistemas que não são baseados em mídia, como infraestruturas de difusão baseadas em padrões (por meio de fluxos de transporte MPEG-2 nativos), infraestruturas sem fio (usando o protocolo RTP de transferência em tempo real) ou até \[ \] mesmo DVDs.

A tabela a seguir compara Windows Perfil Avançado do Vídeo de Mídia 9 com a tecnologia de compactação concorrente.



| Dados de vídeo                                                  | Compactação do setor\* | Windows Mídia\*                                      | Economia de compactação |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720x480 pixels/quadro x 8 bits por canal x 24 fps  | MPEG-2 a 4 a 6 Mbps     | Windows Perfil Avançado do Vídeo de Mídia 9 de 1,3 a 2 Mbps | 3:1                 |
| 480/30i 720x480 pixels/quadro x 8 bits por canal x 30 fps  | MPEG-2 a 6 a 8 Mbps     | Windows Perfil Avançado do Vídeo de Mídia 9 de 2 a 4 Mbps   | 2–3:1               |
| 720/24p 1280x720 pixels/quadro x 8 bits por canal x 24 fps | MPEG-2 a 19 Mbps      | Windows Perfil Avançado do Vídeo de Mídia 9 de 5 a 8 Mbps   | 2.4–3.8:1           |



 

\*Dependente de conteúdo

### <a name="windows-media-video-9-screen"></a>Windows Tela 9 do Vídeo de Mídia

O codec de tela Windows Media Video 9 é otimizado para compactar capturas de tela sequenciais e vídeo altamente estático capturado da exibição do computador, o que o torna ideal para fornecer demonstrações ou demonstrar o uso do computador para treinamento. O codec aproveita a simplicidade típica da imagem e a falta relativa de movimento para obter uma taxa de compactação muito alta.

Durante o processo de codificação, o codec alterna automaticamente entre os modos de codificação sem perda e sem perda, dependendo da complexidade dos dados de vídeo. Para dados complexos, o modo sem perda preserva uma cópia exata dos dados. Para dados menos complexos, o modo de perda descarta alguns dados para obter uma taxa de compactação mais alta. Alternando automaticamente entre esses dois modos, o codec mantém a qualidade do vídeo enquanto maximiza a compactação.

Em geral, o codec Windows Media Video 9 fornece uma melhor manipulação de imagens de bitmap e movimento de tela, mesmo em CPUs relativamente discretas. Ele também é até 100 vezes mais eficiente do que a codificação de comprimento de run length comumente usada.

### <a name="windows-media-video-9-image-version-2"></a>Windows Vídeo de mídia 9 Imagem versão 2

O codec Windows Media Video 9 Image Versão 2 é diferente dos outros codecs de vídeo. Em vez de processar um vídeo descompactado, ele transforma imagens ainda em vídeo usando transições panorênteses, de zoom e de esmaeçamento cruzado entre clipes para criar um número ilimitado de efeitos.

Os resultados podem ser entregues com taxas de dados de até 20 Kbps (quilobits por segundo). Esses arquivos são compactados usando os modos CBR (taxa de bits constante) ou VBR (taxa de bits variável de uma passagem).

> [!Note]  
> O codec Windows Media Video 9 Image Versão 2 não é compatível com o codec Windows Media Video 9.

 

### <a name="windows-media-video-9-vcm"></a>Windows VCM do Vídeo de Mídia 9

A versão do VCM (Video Compression Manager) do codec da série Windows Media Video 9 permite que versões anteriores de codificação e edição de aplicativos deem suporte ao codec da Série Windows 9 do Media Video 9 em contêineres de arquivo, como AVI (Intercalado de Vídeo de Áudio). Esse pacote codec também permite que Windows arquivos WMV (Vídeo de Mídia) baseados no Windows Media Format 9 Series sejam tocadas no Windows Media Player 6.4, em contêineres de arquivo ASF e AVI.

### <a name="compatibility"></a>Compatibilidade

A tabela a seguir descreve o que seu público-alvo experimentará ao tocar o conteúdo da série Windows Media Video 9 em sistemas operacionais microsoft Windows anteriores ou com versões anteriores do Windows Media Player. Esta tabela também lista a compatibilidade para plataformas baseadas em Mac OS X e Windows CE Apple.



| Codec                                  | Recurso             | Compatibilidade com compatibilidade                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vídeo de mídia 9                  | Geral             | <dl> <dt>Windows Media Player 6.4</dt> ou <dt>posterior Windows Media Player 9</dt> para Mac OS X Windows Media Player série 9 e <dt>Windows Media Player 9.1 \* </dt> para Pocket PC Windows Media Player Série 9 e <dt>Windows Media Player 9.1 para Smartphone \* </dt> </dl> |
|                                        | Interpolação de quadros | Requer Windows Media Player série 9 (ou Software Development Kit) ou posterior e Windows XP.                                                                                                                                                                                                                                                                                                                                                                           |
| Windows Perfil Avançado do Vídeo de Mídia 9 | Geral             | Windows Media Player 7 ou posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Tela 9 do Vídeo de Mídia           | Geral             | Windows Media Player 7 ou posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Vídeo de mídia 9 Imagem versão 2  | Geral             | Windows Media Player 7 ou posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Todas as versões Windows Media Player para Pocket PC e Smartphone são enviadas como parte do sistema operacional Microsoft Windows Mobile. Windows Media Player para Pocket PC e Windows Media Player para Smartphone não estão disponíveis para download da Microsoft.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



