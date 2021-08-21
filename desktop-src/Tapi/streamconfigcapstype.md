---
description: O tipo de enumeração StreamConfigCapsType é usado pela estrutura TAPI STREAM CONFIG CAPS como uma opção para indicar se o streaming de \_ áudio ou vídeo está \_ \_ envolvido.
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: Enumeração StreamConfigCapsType (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408ae42041be01c1cad0a763132814500da231a4dcab92e5629ccf27bda7b65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861596"
---
# <a name="streamconfigcapstype-enumeration"></a>Enumeração StreamConfigCapsType

\[Essa enumeração não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O tipo de enumeração **StreamConfigCapsType** é usado pela estrutura [**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md) como uma opção para indicar se o streaming de áudio ou vídeo está envolvido.

## <a name="syntax"></a>Syntax


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**
</dt> <dd>

Configuração de streaming de áudio.

</dd> <dt>

<span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**
</dt> <dd>

Configuração de streaming de vídeo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                       |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




