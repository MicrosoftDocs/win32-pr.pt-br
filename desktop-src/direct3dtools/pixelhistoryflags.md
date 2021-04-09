---
description: Um enum que contém sinalizadores usados para descrever um resultado de histórico de pixel. Consulte PixelHistoryOperation.
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
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087485"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>Enumeração PIXELHISTORYFLAGS

Um enum que contém sinalizadores usados para descrever um resultado de histórico de pixel. Consulte PixelHistoryOperation.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ inicialvalue**  
Um sinalizador que corresponde ao valor de cor inicial (antes do quadro).

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ limpar**  
Um sinalizador que corresponde ao resultado da cor clara.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ desenho**  
Um sinalizador que corresponde ao resultado da cor de desenho.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**\_FinalValue de PHF**  
Um sinalizador que corresponde ao resultado da cor final.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**  
Um sinalizador que corresponde a se o resultado da cor está presente no struct PixelHistoryOperation.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**  
Um sinalizador que corresponde a se o resultado da cor do buffer final está presente no struct PixelHistoryOperation.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**erro de PHF \_**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**  
Não usado.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**  
Um sinalizador que corresponde a não ser capaz de executar o teste de profundidade ou de estêncil.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



