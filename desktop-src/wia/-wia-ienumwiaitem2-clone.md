---
description: Cria uma instância adicional da interface IEnumWiaItem2 e envia de volta um ponteiro para ela.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'Método IEnumWiaItem2:: clone (WIA. h)'
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
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647492"
---
# <a name="ienumwiaitem2clone-method"></a>Método IEnumWiaItem2:: clone

Cria uma instância adicional da interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) e envia de volta um ponteiro para ela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppIEnum* \[ fora\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Recebe o endereço da instância de interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que **IEnumWiaItem2:: clone** cria.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
