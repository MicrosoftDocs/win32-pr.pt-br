---
description: Remove o objeto IWiaItem2 atual da árvore de objetos do dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: Método IWiaItem2::D eleteItem (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 791d596ee48c4d3e2efd67259ec2e37249c930c6da32f704d332df1da6930503
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592996"
---
# <a name="iwiaitem2deleteitem-method"></a>Método IWiaItem2::D eleteItem

Remove o objeto [**IWiaItem2**](-wia-iwiaitem2.md) atual da árvore de objetos do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Atualmente não éusado. Deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O sistema de tempo de Windows wia (image acquisition) 2.0 representa cada dispositivo de hardware WIA 2.0 conectado ao computador do usuário como uma árvore hierárquica de objetos [**IWiaItem2.**](-wia-iwiaitem2.md) Um determinado dispositivo WIA 2.0 pode ou não permitir que os aplicativos excluam **objetos IWiaItem2** de sua árvore. Itens que têm filhos não podem ser excluídos. A interface [**CAPS IEnumWIA \_ DEV \_ DEVE**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) ser usada para consultar o dispositivo quanto à funcionalidade de exclusão de item.

Se o dispositivo dá suporte à exclusão de itens em sua árvore [**IWiaItem2,**](-wia-iwiaitem2.md) chame o método **IWiaItem2::D eleteItem** para remover o objeto **IWiaItem2.** Observe que esse método exclui apenas um objeto depois que todas as referências ao objeto foram liberadas. Se a exclusão de um item tiver falhado, E \_ DELETEITEM será retornado. O valor numérico para esse erro ainda não está definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




