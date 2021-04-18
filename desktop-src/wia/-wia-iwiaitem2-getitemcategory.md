---
description: Obtém as informações de categoria de um item.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'Método IWiaItem2:: GetItemCategory (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771375"
---
# <a name="iwiaitem2getitemcategory-method"></a>Método IWiaItem2:: GetItemCategory

Obtém as informações de categoria de um item.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pItemCategoryGUID* \[ fora\]
</dt> <dd>

Tipo: **GUID \** _

Recebe um ponteiro para o GUID que identifica a categoria do item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore hierárquica de objetos associados a um dispositivo de hardware WIA (Windows Image Acquisition) 2,0 tem uma categoria específica. Esse método permite que os aplicativos identifiquem a categoria de qualquer item em uma árvore hierárquica de objetos de item em um dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




