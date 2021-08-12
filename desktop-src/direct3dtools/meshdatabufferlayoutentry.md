---
description: Representa informações sobre uma única entrada no layout do buffer de uma malha.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura MeshDataBufferLayoutEntry
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44cc67402c69b690ba9070fa51bf8d26f316faa7d10ac991226db2c05b6d6a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282265"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Estrutura MeshDataBufferLayoutEntry

Representa informações sobre uma única entrada no layout do buffer de uma malha.

## <a name="syntax"></a>Sintaxe


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Membros

**Pname**  
Uma cadeia de caracteres COM que contém o nome da entrada.

**numComponents**  
O número de componentes homogêneos (valores) que comem essa entrada.

**isPosition**  
true se a entrada for uma posição; caso contrário, false.

**format**  
O formato de dados da entrada (registrar). Para obter mais informações, consulte a enumeração REGISTER \_ FORMAT.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



