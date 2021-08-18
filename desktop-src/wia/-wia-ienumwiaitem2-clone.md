---
description: Cria uma instância adicional da interface IEnumWiaItem2 e envia de volta um ponteiro para ela.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: Método IEnumWiaItem2::Clone (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 21c94c634a6930f28f48cdc35a4d3cf199b8fa33e9fb5f08444797fd76f50c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965845"
---
# <a name="ienumwiaitem2clone-method"></a>Método IEnumWiaItem2::Clone

Cria uma instância adicional da interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) e envia de volta um ponteiro para ela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Recebe o endereço da instância da interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que **IEnumWiaItem2::Clone** cria.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar [o método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface que recebem por meio do *parâmetro ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
