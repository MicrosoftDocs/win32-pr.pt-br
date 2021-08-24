---
title: Windows SDK do formato de mídia 11
description: Windows SDK do formato de mídia 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows SDK do formato de mídia, sobre
- Windows SDK de mídia
- Windows SDK do formato de mídia, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), sobre
- ASF (formato de sistemas avançados), sobre
- Windows SDK do formato de mídia, recursos
- Windows SDK do formato de mídia, principais recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70af68402ea5a22a9499ca09fd4b2e4022f304ee5ebf68a4f877a978ad168e4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839426"
---
# <a name="windows-media-format-11-sdk"></a>Windows SDK do formato de mídia 11

esta documentação descreve o sdk (Software Development Kit) do Microsoft Windows Media Format e aplica-se às versões de 32 bits e baseadas em x64 do sdk.

o sdk do formato de mídia Windows é um componente do sdk (Software Development Kit) do Microsoft Windows Media. outros componentes incluem o sdk do Windows Media Services, o sdk do media Encoder Windows, Windows sdk do media rights Manager, sdk do Windows de mídia Gerenciador de Dispositivos e sdk do Windows Media Player.

o SDK do formato de mídia Windows fornece aos desenvolvedores de aplicativos acesso aos componentes do formato de mídia Windows. esses componentes incluem o contêiner de arquivo ASF (Advanced Systems Format), os codecs de áudio e vídeo de mídia Windows, o recurso de streaming de rede básico e o gerenciamento de direitos digitais. os objetos do SDK do formato de mídia Windows manipulam os componentes da mídia do Windows em um nível baixo; os outros componentes do SDK de mídia do Windows incluem objetos que funcionam em um nível superior.

a principal finalidade do SDK do formato de mídia Windows é permitir que os desenvolvedores criem aplicativos que reproduzem, gravam, editam, criptografam e fornecem arquivos ASF (Advanced Systems Format) e fluxos de rede. esses arquivos e fluxos normalmente contêm conteúdo de áudio e vídeo codificado usando os codecs de áudio e vídeo de mídia Windows. No entanto, o ASF pode conter qualquer tipo de dados. Para obter mais informações sobre a estrutura de contêiner do formato de sistemas avançados, consulte [visão geral do formato ASF](overview-of-the-asf-format.md).

os principais recursos do SDK do formato de mídia do Windows são:

-   Suporte para codecs líderes do setor. o SDK do formato de mídia 11 do Windows inclui o codec microsoft Windows media Video 9 e o codec microsoft Windows media Audio 9,1. Ambos os codecs fornecem codificação excepcional de conteúdo de mídia digital. o novo para esta versão é o codec de perfil avançado do Windows Media Video 9, que fornece otimizações para transmissão de vídeo. esse SDK também inclui o codec de tela Microsoft Windows Media Video 9 para compactar a atividade de tela de computador durante sessões de aplicativos de usuário e o codec de voz Windows Media Audio 9,1, que codifica o áudio de baixa complexidade, como fala e se adapta de forma inteligente a áudio mais complexo, como música, para uma representação superior dos cenários de música de voz combinados.
-   Suporte para gravação de arquivos ASF. Os arquivos são criados com base em perfis personalizáveis, permitindo a fácil configuração e padronização de arquivos. Esse SDK pode ser usado para gravar arquivos com mais de 2 gigabytes, permitindo arquivos contínuos mais longos e de melhor qualidade.
-   Suporte para leitura de arquivos ASF. Esse SDK fornece suporte para a leitura de arquivos ASF locais, bem como a leitura de dados ASF transmitidos por uma rede. O suporte também é fornecido para muitos recursos avançados de leitura, como suporte nativo para arquivos de taxa de bits múltipla (MBR), que contêm vários fluxos com o mesmo conteúdo codificado em diferentes taxas de bits. O leitor seleciona automaticamente qual fluxo de MBR usar, dependendo da largura de banda disponível no momento da reprodução.
-   Suporte para fornecimento de fluxos ASF em uma rede. esse SDK fornece suporte para a entrega de dados ASF por meio de HTTP a computadores remotos em uma rede e também para o fornecimento de dados diretamente para um servidor de mídia de Windows remoto.
-   Suporte para edição de metadados em arquivos ASF. Informações sobre um arquivo e seu conteúdo são manipuladas facilmente com esse SDK. Os desenvolvedores podem usar o sistema robusto de atributos de metadados incluídos no SDK ou criar atributos personalizados para atender às suas necessidades.
-   Suporte para aplicativos de edição de conteúdo. Esse SDK permite que os aplicativos busquem pontos dentro de um arquivo por hora da apresentação e por quadro de vídeo. além disso, os arquivos criados usando o SDK do formato de mídia Windows podem manter os carimbos de data/hora em formatos usados na produção de filmes e televisão.
-   Suporte para leitura e edição de metadados em arquivos MP3. Esse SDK fornece suporte integrado para a leitura de arquivos MP3 com os mesmos métodos usados para ler arquivos ASF. os aplicativos criados com o SDK do formato de mídia Windows também podem editar atributos de metadados em arquivos MP3 usando suporte interno para as marcas ID3 mais comuns usadas pelos criadores de conteúdo.
-   Suporte para proteção de Rights Management digital. Esse SDK fornece métodos para ler e gravar arquivos ASF e fluxos de rede protegidos pelo Rights Management digital para impedir a reprodução ou cópia não autorizada do conteúdo.

para baixar o SDK do formato de mídia do Windows, consulte a página [Downloads de mídia do Windows](https://msdn.microsoft.com/windows/desktop/aa904949) no site da Microsoft.

este documento descreve como você pode desenvolver aplicativos de mídia digital usando o SDK do formato de mídia Windows. Ele é dividido nas seções a seguir.

> [!Note]  
> embora este documento contenha informações sobre a versão mais recente do sdk do formato de mídia Windows, a maioria dos recursos que ele descreve tem suporte nas versões mais antigas do sdk. as páginas de referência para os métodos, as funções, as estruturas e as enumerações do SDK do formato de mídia Windows incluem os requisitos de versão.

 



| Seção                                                                                                          | Descrição                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sobre o SDK do formato de mídia Windows](about-the-windows-media-format-sdk.md)                                     | Fornece uma visão geral e informações básicas com as quais você deve estar familiarizado antes de tentar criar aplicativos.                                                                                  |
| [Guia de programação](programming-guide.md)                                                                       | Fornece instruções detalhadas para executar várias tarefas, como leitura, gravação e indexação de arquivos, proteção de arquivos com Rights Management digital, transmissão de dados ASF em uma rede e assim por diante. |
| [Referência de programação](programming-reference.md)                                                               | fornece informações de referência para as interfaces, métodos, funções, estruturas, tipos de enumeração e constantes relacionadas ao formato de mídia Windows.                                                     |
| [Windows Interfaces de áudio de mídia e codec de vídeo](windows-media-audio-and-video-codec-interfaces--deprecated.md) | fornece instruções sobre como usar os DMOs (objetos de mídia digital) do codec de áudio e vídeo de mídia Windows diretamente.                                                                                           |
| [*Glossário*](wmformat-glossary.md)                                                                              | define os termos usados na documentação do SDK do formato de mídia Windows.                                                                                                                                    |



 

 

 




