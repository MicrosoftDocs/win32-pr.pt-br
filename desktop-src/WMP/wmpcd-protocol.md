---
title: Protocolo WMPCD
description: Protocolo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolos
- Modelo de objeto do Windows Media Player, protocolos
- modelo de objeto, protocolos
- Controle ActiveX do Windows Media Player, protocolos para o modelo de objeto
- Controle ActiveX, protocolos para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, protocolos para modelo de objeto
- Windows Media Player Mobile, protocolos para modelo de objeto
- protocolos, modelo de objeto do Windows Media Player
- protocolos, WMPCD
- Protocolo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159762"
---
# <a name="wmpcd-protocol"></a>Protocolo WMPCD

O protocolo WMPCD permite que você especifique faixas em um CD usando a sintaxe de URL. Esta é a sintaxe geral do protocolo:


```C++
wmpcd://drive/track
```



O segmento da *unidade* é o índice da unidade de CD. O segmento de *faixa* é o número da faixa. O exemplo a seguir demonstra o uso do protocolo WMPCD.


```C++
player.url = "wmpcd://0/4";
```



O exemplo reproduz a quarta faixa no disco na primeira unidade de CD (a unidade cujo índice é 0).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tipos de arquivos e protocolos com suporte**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




