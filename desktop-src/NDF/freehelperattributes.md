---
title: Função FreeHelperAttributes (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de \_ estruturas de atributo auxiliar.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- NDF da função FreeHelperAttributes
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb16ad2d7f505a90d806e3f6a155f2c20affce2c71267316c2278e2320c371b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802426"
---
# <a name="freehelperattributes-function"></a>Função FreeHelperAttributes

A função **FreeHelperAttributes** Desaloca a memória alocada internamente a uma matriz de estruturas de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.

## <a name="syntax"></a>Sintaxe


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* \[ no\]
</dt> <dd>

Tipo: **[ **\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

A matriz de estruturas. A memória alocada apontada por essas estruturas será liberada.

</dd> <dt>

*HelperAttributeCount* 
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

[**\_atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

