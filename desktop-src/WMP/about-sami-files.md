---
title: Sobre arquivos SAMI
description: Sobre arquivos SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Arquivos SAMI (intercâmbio de mídia acessível) sincronizados
- SAMI (sincronizado com o intercâmbio de mídia acessível), arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822693"
---
# <a name="about-sami-files"></a>Sobre arquivos SAMI

Os arquivos SAMI são arquivos de texto que têm uma extensão de nome de arquivo. SMI ou. Sami. Elas contêm as cadeias de caracteres de texto usadas para legendas codificadas sincronizadas, legendas e descrições de áudio. Eles também especificam os parâmetros de tempo usados pelo controle do Windows Media Player para sincronizar texto de legenda oculta com conteúdo de áudio ou vídeo. Quando um arquivo de mídia digital atinge um horário designado no arquivo SAMI, o texto é alterado de acordo na área de exibição da legenda oculta da página da Web.

Além de um editor de texto simples (como o Microsoft Notepad), o software especial não é necessário para criar um arquivo SAMI. SAMI e HTML compartilham elementos comuns, como as <HEAD> marcas e <BODY> . Como no HTML, as marcas usadas em arquivos SAMI sempre devem ser usadas em pares. Por exemplo, um elemento BODY começa com uma <BODY> marca e sempre deve terminar com uma </BODY> marca.

Um arquivo SAMI básico requer três marcas fundamentais: <SAMI> , <HEAD> e <BODY> .

A <SAMI> marca identifica o documento como um documento Sami para que outros aplicativos possam reconhecer seu formato de arquivo.

Entre as marcas <HEAD> e </HEAD> , você define as diretrizes básicas e outras informações de formato para o documento Sami, como o título do documento, informações gerais e propriedades de estilo para legendas ocultas. Como HTML, o conteúdo declarado dentro do elemento HEAD não é exibido como saída.

Elementos e atributos definidos entre as marcas <BODY> e </BODY> exibem o conteúdo visto pelo usuário. No SAMI, o elemento BODY contém os parâmetros para sincronização e as cadeias de caracteres de texto usadas para legendas codificadas.

Definido dentro do elemento HEAD, o elemento STYLE fornece a funcionalidade adicional no SAMI. Entre as marcas <STYLE> e </STYLE> , você pode definir vários seletores de folha de estilo em cascata (CSS) para estilo e layout. Propriedades de estilo, como fontes, tamanhos e alinhamentos, podem ser personalizadas para fornecer uma experiência de usuário avançada e também promover a acessibilidade. Por exemplo, a definição de uma classe de estilo de fonte de texto grande pode melhorar a legibilidade para os usuários que têm dificuldade de ler texto pequeno. Além disso, ao definir várias classes de linguagem diferentes, você pode ajudar os usuários internacionais a entender melhor o conteúdo de mídia digital.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




