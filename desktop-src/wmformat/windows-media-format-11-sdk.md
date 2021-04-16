---
title: SDK do Windows Media Format 11
description: SDK do Windows Media Format 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- SDK do Windows Media Format, sobre
- SDK do Windows Media
- SDK do Windows Media Format, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), sobre
- ASF (formato de sistemas avançados), sobre
- SDK do Windows Media Format, recursos
- SDK do Windows Media Format, principais recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363c268194b476b6d3326a9c57fe1e709d17e2fe
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104454423"
---
# <a name="windows-media-format-11-sdk"></a>SDK do Windows Media Format 11

Esta documentação descreve o SDK (Software Development Kit) do Microsoft Windows Media Format e aplica-se às versões de 32 bits e baseadas em x64 do SDK.

O SDK do Windows Media Format é um componente do SDK (Software Development Kit) do Microsoft Windows Media. Outros componentes incluem o SDK do Windows Media Services, o SDK do Windows Media Encoder, o SDK do Windows Media Rights Manager, o SDK do Windows Media Gerenciador de Dispositivos e o SDK do Windows Media Player.

O Windows Media Format SDK fornece aos desenvolvedores de aplicativos acesso aos componentes do formato de mídia do Windows. Esses componentes incluem o contêiner de arquivo ASF (Advanced Systems Format), os codecs de áudio e vídeo do Windows Media, a capacidade básica de transmissão de rede e o gerenciamento de direitos digitais. Os objetos do Windows Media Format SDK manipulam os componentes do Windows Media em um nível baixo; os outros componentes do SDK do Windows Media incluem objetos que funcionam em um nível superior.

A principal finalidade do SDK do Windows Media Format é permitir que os desenvolvedores criem aplicativos que reproduzem, gravem, editem, criptografem e forneçam arquivos ASF (Advanced Systems Format) e fluxos de rede. Esses arquivos e fluxos normalmente contêm conteúdo de áudio e vídeo codificado usando os codecs de áudio e vídeo do Windows Media. No entanto, o ASF pode conter qualquer tipo de dados. Para obter mais informações sobre a estrutura de contêiner do formato de sistemas avançados, consulte [visão geral do formato ASF](overview-of-the-asf-format.md).

Os principais recursos do Windows Media Format SDK são:

-   Suporte para codecs líderes do setor. O SDK do Windows Media Format 11 inclui o codec Microsoft Windows Media Video 9 e o codec Microsoft Windows Media Audio 9,1. Ambos os codecs fornecem codificação excepcional de conteúdo de mídia digital. O novo para esta versão é o codec de perfil avançado do Windows Media Video 9, que fornece otimizações para transmissão de vídeo. Esse SDK também inclui o codec de tela do Microsoft Windows Media Video 9 para compactar a atividade de tela de computador durante sessões de aplicativos de usuário e o codec de voz do Windows Media Audio 9,1, que codifica o áudio de baixa complexidade, como fala e se adapta de forma inteligente a áudio mais complexo, como música, para uma representação superior dos cenários combinados de música em voz.
-   Suporte para gravação de arquivos ASF. Os arquivos são criados com base em perfis personalizáveis, permitindo a fácil configuração e padronização de arquivos. Esse SDK pode ser usado para gravar arquivos com mais de 2 gigabytes, permitindo arquivos contínuos mais longos e de melhor qualidade.
-   Suporte para leitura de arquivos ASF. Esse SDK fornece suporte para a leitura de arquivos ASF locais, bem como a leitura de dados ASF transmitidos por uma rede. O suporte também é fornecido para muitos recursos avançados de leitura, como suporte nativo para arquivos de taxa de bits múltipla (MBR), que contêm vários fluxos com o mesmo conteúdo codificado em diferentes taxas de bits. O leitor seleciona automaticamente qual fluxo de MBR usar, dependendo da largura de banda disponível no momento da reprodução.
-   Suporte para fornecimento de fluxos ASF em uma rede. Esse SDK fornece suporte para a entrega de dados ASF por meio de HTTP a computadores remotos em uma rede e também para o fornecimento de dados diretamente a um Windows Media Server remoto.
-   Suporte para edição de metadados em arquivos ASF. Informações sobre um arquivo e seu conteúdo são manipuladas facilmente com esse SDK. Os desenvolvedores podem usar o sistema robusto de atributos de metadados incluídos no SDK ou criar atributos personalizados para atender às suas necessidades.
-   Suporte para aplicativos de edição de conteúdo. Esse SDK permite que os aplicativos busquem pontos dentro de um arquivo por hora da apresentação e por quadro de vídeo. Além disso, os arquivos criados usando o Windows Media Format SDK podem manter carimbos de data/hora em formatos usados em produção de filmes e televisão.
-   Suporte para leitura e edição de metadados em arquivos MP3. Esse SDK fornece suporte integrado para a leitura de arquivos MP3 com os mesmos métodos usados para ler arquivos ASF. Os aplicativos criados com o Windows Media Format SDK também podem editar atributos de metadados em arquivos MP3 usando suporte interno para as marcas ID3 mais comuns usadas pelos criadores de conteúdo.
-   Suporte para proteção de Rights Management digital. Esse SDK fornece métodos para ler e gravar arquivos ASF e fluxos de rede protegidos pelo Rights Management digital para impedir a reprodução ou cópia não autorizada do conteúdo.

Para baixar o SDK do Windows Media Format, consulte a página de [downloads do Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) no site da Microsoft.

Este documento descreve como você pode desenvolver aplicativos de mídia digital usando o SDK do Windows Media Format. Ele é dividido nas seções a seguir.

> [!Note]  
> Embora este documento contenha informações sobre a versão mais recente do SDK do Windows Media Format, a maioria dos recursos que ele descreve tem suporte nas versões mais antigas do SDK. As páginas de referência para os métodos, as funções, as estruturas e as enumerações do Windows Media Format SDK incluem os requisitos de versão.

 



| Seção                                                                                                          | Descrição                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o SDK do Windows Media Format](about-the-windows-media-format-sdk.md)                                     | Fornece uma visão geral e informações básicas com as quais você deve estar familiarizado antes de tentar criar aplicativos.                                                                                  |
| [Guia de programação](programming-guide.md)                                                                       | Fornece instruções detalhadas para executar várias tarefas, como leitura, gravação e indexação de arquivos, proteção de arquivos com Rights Management digital, transmissão de dados ASF em uma rede e assim por diante. |
| [Referência de programação](programming-reference.md)                                                               | Fornece informações de referência para as interfaces, métodos, funções, estruturas, tipos de enumeração e constantes relacionadas ao formato de mídia do Windows.                                                     |
| [Interfaces do codec de áudio e vídeo do Windows Media](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Fornece instruções sobre como usar o DMOs (objetos de mídia digital) do Windows Media Audio e Video Codec diretamente.                                                                                           |
| [*Glossário*](wmformat-glossary.md)                                                                              | Define os termos usados na documentação do SDK do Windows Media Format.                                                                                                                                    |



 

 

 




