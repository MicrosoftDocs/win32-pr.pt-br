---
description: Remove o objeto IWiaItem2 atual da árvore de objetos do dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: 'IWiaItem2: método eleteItem de:D (WIA. h)'
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
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793855"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2: método eleteItem de:D

Remove o objeto [**IWiaItem2**](-wia-iwiaitem2.md) atual da árvore de objetos do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O sistema de tempo de execução da Windows Image Acquisition (WIA) 2,0 representa cada dispositivo de hardware WIA 2,0 conectado ao computador do usuário como uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) . Um determinado dispositivo WIA 2,0 pode ou não permitir que aplicativos excluam objetos **IWiaItem2** de sua árvore. Itens que têm filhos não podem ser excluídos. A interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) deve ser usada para consultar o dispositivo para a funcionalidade de exclusão de itens.

Se o dispositivo der suporte à exclusão de itens em sua árvore [**IWiaItem2**](-wia-iwiaitem2.md) , chame o método **IWiaItem2::D eleteitem** para remover o objeto **IWiaItem2** . Observe que esse método só exclui um objeto depois que todas as referências ao objeto forem liberadas. Se a exclusão de um item tiver falhado, E \_ DELETEITEM será retornado. O valor numérico para esse erro ainda não foi definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




