---
description: Representa um pacote de quatro chamadas.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PackedCallPkg
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39be8828cf3ea0fbf773965db7272d566d43546b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626522"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span id="vspixengine.packedcallpkg"></span>Estrutura PackedCallPkg

Representa um pacote de quatro chamadas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a>Membros

**pcp1**  
A primeira chamada no pacote.

**pcp2**  
A segunda chamada no pacote.

**pcp3**  
A terceira chamada no pacote.

**pcp4**  
A quarta chamada no pacote.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



