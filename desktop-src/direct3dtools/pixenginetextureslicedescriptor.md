---
description: Representa uma descrição de uma fatia de textura.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixEngineTextureSliceDescriptor
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b10d66a7843198f86eeaebcf8f49b13abdd8c100
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625542"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span id="vspixengine.pixenginetextureslicedescriptor"></span>Estrutura PixEngineTextureSliceDescriptor

Representa uma descrição de uma fatia de textura.

## <a name="syntax"></a>Sintaxe


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a>Membros

**width**  
A largura (número de amostras no eixo X) da fatia.

**altura**  
A altura (número de amostras no eixo Y) da fatia.

**blockRowBytes**  
O número de bytes por linha em cada bloco.

**offset**  
O deslocamento da fatia dentro da textura inteira.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



