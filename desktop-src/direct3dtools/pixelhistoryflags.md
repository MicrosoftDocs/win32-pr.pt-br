---
description: Uma enum que contém sinalizadores usados para descrever um resultado de histórico de pixels. Consulte PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ff4447bdf19342dd2932f5b93eaf2722072660ae5007b40747834d603a6c57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726676"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>Enumeração PIXELHISTORYFLAGS

Uma enum que contém sinalizadores usados para descrever um resultado de histórico de pixels. Consulte PixelHistoryOperation.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ INITIALVALUE**  
Um sinalizador que corresponde ao valor de cor inicial (antes do quadro).

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ CLEAR**  
Um sinalizador que corresponde ao resultado de cor clara.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ DRAW**  
Um sinalizador que corresponde ao resultado da cor de desenho.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ FINALVALUE**  
Um sinalizador que corresponde ao resultado da cor final.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**  
Um sinalizador que corresponde a se o resultado da cor está presente no struct PixelHistoryOperation.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**  
Um sinalizador que corresponde a se o resultado final da cor do buffer está presente no struct PixelHistoryOperation.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**ERRO \_ DE PHF**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**  
Não usado.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ NÃO PODERUNFULLDEPTHSTENCILTEST**  
Um sinalizador que corresponde a não conseguir executar o teste de profundidade ou estêncil.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



