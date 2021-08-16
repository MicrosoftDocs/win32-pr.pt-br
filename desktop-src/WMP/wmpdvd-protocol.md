---
title: Protocolo WMPDVD
description: Protocolo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player, protocolos
- modelo de objeto Windows Media Player, protocolos
- modelo de objeto, protocolos
- Windows Media Player ActiveX controle, protocolos para o modelo de objeto
- ActiveX controle, protocolos para o modelo de objeto
- Windows Media Player controle de ActiveX móvel, protocolos para o modelo de objeto
- Windows Media Player Móvel, protocolos para modelo de objeto
- protocolos, Windows Media Player modelo de objeto
- protocolos, WMPDVD
- Protocolo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca67f3cdee6f040aeb266e02493425ca76715ade2e3269f4377ba340af89cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761286"
---
# <a name="wmpdvd-protocol"></a>Protocolo WMPDVD

O protocolo WMPDVD permite que você especifique a mídia de um DVD usando a sintaxe de URL. Essa é a forma geral do protocolo:


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



O segmento da *unidade* é a letra da unidade de DVD; Ele não inclui os dois-pontos normalmente usados com especificadores de unidade. Esse segmento é sempre necessário.

O segmento de *título* é o número do título a ser tocado. Ela não é necessária, a menos que você queira iniciar a reprodução em um título específico ou em um capítulo específico de um título específico.

O segmento do *capítulo* é o número do capítulo a ser tocado. Isso não é necessário, a menos que você queira iniciar a reprodução em um capítulo específico de um título específico.

O argumento contentdir é o caminho para um TS de vídeo \_ . Arquivo IFO, que pode estar no armazenamento local ou em um compartilhamento de rede. Se você incluir esse segmento, o segmento da *unidade* será ignorado, embora ainda seja necessário. Se você também incluir o segmento do *título* ou os segmentos do *título* e do *capítulo* , eles serão relativos ao conteúdo do DVD especificado no segmento contentdir, não ao segmento da *unidade* .

O exemplo a seguir usa o protocolo WMPDVD para reproduzir o DVD desde o início, como se ele estivesse sendo iniciado automaticamente.


```C++
player.url = "wmpdvd://F";
```



O exemplo a seguir usa o protocolo WMPDVD para reproduzir o DVD do início do título especificado.


```C++
player.url = "wmpdvd://F/2";
```



O exemplo a seguir usa o protocolo WMPDVD para reproduzir o DVD do capítulo especificado.


```C++
player.url = "wmpdvd://F/2/4";
```



O exemplo a seguir usa o protocolo WMPDVD para reproduzir conteúdo de DVD do armazenamento local. A cadeia de caracteres de *caminho* termina com a pasta que contém o vídeo \_ TS. Arquivo IFO; Ele não inclui o nome do arquivo. Neste exemplo, o valor do segmento da *unidade* não tem nenhum efeito, embora seja necessário, e a reprodução começa no capítulo 4 do título 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



a atribuição de uma cadeia de caracteres WMPDVD à propriedade **url** requer Windows Media Player 9 Series ou posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tipos de arquivos e protocolos com suporte**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




