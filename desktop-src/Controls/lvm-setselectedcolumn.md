---
title: LVM_SETSELECTEDCOLUMN mensagem (Commctrl.h)
description: Define o índice da coluna selecionada.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- LVM_SETSELECTEDCOLUMN controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6564e1fda50d11b3d4c520f85184439b0465f1cf5767e7926e6e1c9476f786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019164"
---
# <a name="lvm_setselectedcolumn-message"></a>Mensagem LVM \_ SETSELECTEDCOLUMN

Define o índice da coluna selecionada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Valor do tipo **int** que especifica o índice de coluna.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Os índices de coluna são armazenados em uma **matriz int.** Consulte o **membro puColumns** de [**LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





