---
title: Protocolo WMPCD
description: Protocolo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolos
- Windows Media Player modelo de objeto, protocolos
- modelo de objeto, protocolos
- Windows Media Player ActiveX controle, protocolos para o modelo de objeto
- ActiveX controle, protocolos para o modelo de objeto
- Windows Media Player Controle ActiveX dispositivo móvel, protocolos para o modelo de objeto
- Windows Media Player Dispositivos móveis, protocolos para o modelo de objeto
- protocolos, Windows Media Player modelo de objeto
- protocolos, WMPCD
- Protocolo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b1359d22b792587f7cceeb46f0f9e621585dfba296422a227e9012077df7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900136"
---
# <a name="wmpcd-protocol"></a>Protocolo WMPCD

O protocolo WMPCD permite que você especifique faixas em um compact disc usando a sintaxe de URL. Essa é a sintaxe geral do protocolo:


```C++
wmpcd://drive/track
```



O *segmento* de unidade é o índice da unidade de CD. O *segmento* de faixa é o número da faixa. O exemplo a seguir demonstra o uso do protocolo WMPCD.


```C++
player.url = "wmpcd://0/4";
```



O exemplo reproduz a quarta faixa no disco na primeira unidade de CD (a unidade cujo índice é 0).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Protocolos e tipos de arquivo com suporte**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




