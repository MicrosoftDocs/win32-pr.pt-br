---
title: Função FreeRootCauseInfos (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de estruturas RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- NDF da função FreeRootCauseInfos
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644498"
---
# <a name="freerootcauseinfos-function"></a>Função FreeRootCauseInfos

A função **FreeRootCauseInfos** Desaloca a memória alocada internamente a uma matriz de estruturas [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) . Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.

## <a name="syntax"></a>Sintaxe


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* \[ no\]
</dt> <dd>

Tipo: **[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

A matriz de estruturas. A memória alocada apontada por essas estruturas será liberada.

</dd> <dt>

_RootCauseCount * 
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

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

