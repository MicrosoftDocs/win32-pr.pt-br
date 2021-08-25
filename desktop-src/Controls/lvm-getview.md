---
title: LVM_GETVIEW mensagem (Commctrl.h)
description: Recupera a exibição atual de um controle de exibição de lista.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431b0a7b3fba9a45370c372347285489a56082c4a04396c273a45c4da41b05b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915506"
---
# <a name="lvm_getview-message"></a>Mensagem GETVIEW do LVM \_

Recupera a exibição atual de um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **DWORD** que especifica a exibição atual.

## <a name="remarks"></a>Comentários

A seguir estão os valores para exibições.

-   DETALHES DA \_ EXIBIÇÃO \_ LV
-   ÍCONE DE \_ EXIBIÇÃO \_ LV
-   LISTA DE \_ EXIBIÇÃO \_ LV
-   \_SMALLICON DE EXIBIÇÃO DE LV \_
-   LV \_ VIEW \_ TILE

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





