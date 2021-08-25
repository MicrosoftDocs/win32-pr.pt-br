---
title: LVM_SETVIEW mensagem (Commctrl.h)
description: Define a exibição de um controle de exibição de lista.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8d07b636a14624632d0e41ebcf6db66f420b9df4f8ca852e55ab2f3e1578e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656196"
---
# <a name="lvm_setview-message"></a>Mensagem SETVIEW do LVM \_

Define a exibição de um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>**DWORD** que especifica a exibição.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 1 se for bem-sucedido ou -1 caso contrário. Por exemplo, -1 será retornado se a exibição for inválida.

## <a name="remarks"></a>Comentários

A seguir estão os valores para exibições.

-   DETALHES DA \_ EXIBIÇÃO \_ LV
-   ÍCONE DE \_ EXIBIÇÃO \_ LV
-   LISTA DE \_ EXIBIÇÃO \_ LV
-   \_SMALLICON DE EXIBIÇÃO DE LV \_
-   LV \_ VIEW \_ TILE

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comctl32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





