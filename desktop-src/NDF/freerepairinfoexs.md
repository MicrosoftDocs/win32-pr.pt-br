---
title: Função FreeRepairInfoExs (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de estruturas RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- NDF da função FreeRepairInfoExs
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b75d3d3ee8ba710b0b0ed4755e5ee01309f955bcc1658145dc1d42fe3b9e1ed8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802416"
---
# <a name="freerepairinfoexs-function"></a>Função FreeRepairInfoExs

A função **FreeRepairInfoExs** Desaloca a memória alocada internamente a uma matriz de estruturas [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) . Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.

## <a name="syntax"></a>Sintaxe


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* \[ no\]
</dt> <dd>

Tipo: **[ **RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\***

A matriz de estruturas. A memória alocada apontada por essas estruturas será liberada.

</dd> <dt>

*RepairCount* 
</dt> <dd>

Tipo: **ULONG**

O número de estruturas na matriz apontada por *pInfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Tipo: **bool**

True se a matriz de estruturas também deve ser excluída; caso contrário, false.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

