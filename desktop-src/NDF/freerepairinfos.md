---
title: Função FreeRepairInfos (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de estruturas RepairInfo.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- NDF da função FreeRepairInfos
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085367"
---
# <a name="freerepairinfos-function"></a>Função FreeRepairInfos

A função **FreeRepairInfos** Desaloca a memória alocada internamente a uma matriz de estruturas [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) . Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.

## <a name="syntax"></a>Sintaxe


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* \[ no\]
</dt> <dd>

Tipo: **[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

A matriz de estruturas. A memória alocada apontada por essas estruturas será liberada.

</dd> <dt>

_RepairCount * 
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

