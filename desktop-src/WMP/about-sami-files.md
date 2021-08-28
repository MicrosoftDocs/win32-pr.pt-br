---
title: Sobre arquivos SAMI
description: Sobre arquivos SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player de objeto, SAMI (Synchronized Accessible Media Interchange)
- modelo de objeto, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Controle ActiveX dispositivo móvel, SAMI (Synchronized Accessible Media Interchange)
- ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), arquivos
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f03d3e4079a117831ed8afb53648abf6a128ee
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880539"
---
# <a name="about-sami-files"></a>Sobre arquivos SAMI

Arquivos SAMI são arquivos de texto que têm uma extensão de nome de arquivo .smi ou .sami. Eles contêm as cadeias de caracteres de texto usadas para legendas fechadas sincronizadas, subtítulos e descrições de áudio. Eles também especificam os parâmetros de tempo usados pelo controle Windows Media Player para sincronizar o texto de legenda fechada com conteúdo de áudio ou vídeo. Quando um arquivo de mídia digital atinge um tempo designado no arquivo SAMI, o texto muda de acordo na área de exibição de legenda fechada da página da Web.

Além de um editor de texto simples (como o Microsoft Bloco de notas), o software especial não é necessário para criar um arquivo SAMI. Os elementos comuns de compartilhamento SAMI e HTML, como o <HEAD> e &lt; marcas &gt; BODY. Como em HTML, as marcas usadas em arquivos SAMI sempre devem ser usadas em pares. Por exemplo, um elemento BODY começa com uma marca &lt; BODY e sempre deve terminar com uma marca &gt; &lt; &gt; /BODY.

Um arquivo SAMI básico requer três marcas fundamentais: &lt; SAMI &gt; , <HEAD>, e &lt; &gt; BODY.

A marca SAMI identifica o documento como um documento SAMI para que outros &lt; &gt; aplicativos possam reconhecer seu formato de arquivo.

Entre o <HEAD> e </HEAD> marcas, você define diretrizes básicas e outras informações de formato para o documento SAMI, como o título do documento, informações gerais e propriedades de estilo para legendas fechadas. Como HTML, o conteúdo declarado dentro do elemento HEAD não é exibido como saída.

Elementos e atributos definidos entre as &lt; marcas BODY &gt; e &lt; /BODY &gt; exibem o conteúdo visto pelo usuário. No SAMI, o elemento BODY contém os parâmetros para sincronização e as cadeias de caracteres de texto usadas para legendas fechadas.

Definido dentro do elemento HEAD, o elemento STYLE fornece funcionalidade adicional no SAMI. Entre as marcas STYLE e , você pode definir vários seletores CSS (Folha de Estilos em &lt; &gt; </STYLE> Cascata) para estilo e layout. Propriedades de estilo, como fontes, tamanhos e alinhamentos, podem ser personalizadas para fornecer uma experiência de usuário rica, além de promover a acessibilidade. Por exemplo, definir uma classe de estilo de fonte de texto grande pode melhorar a capacidade de leitura para usuários que têm dificuldade para ler texto pequeno. Além disso, definindo várias classes de linguagem diferentes, você pode ajudar usuários internacionais a entender melhor o conteúdo de mídia digital.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




