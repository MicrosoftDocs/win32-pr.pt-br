---
title: LVM_SETGROUPINFO mensagem (Commctrl.h)
description: Define informações do grupo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO controles Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553a81c3cfe962ae6daf5ae4c988964028554bc662cec08df40c16fd8b4eb43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077266"
---
# <a name="lvm_setgroupinfo-message"></a>Mensagem LVM \_ SETGROUPINFO

Define informações do grupo. Envie essa mensagem explicitamente ou usando a [**macro \_ ListView SetGroupInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>ID que especifica o grupo cujas informações devem ser definidas.</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Ponteiro para uma [**estrutura LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) que contém as informações a definir.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a ID do grupo se for bem-sucedido ou -1 caso contrário.

## <a name="remarks"></a>Comentários

Para alterar uma ID de grupo de um grupo existente, adicione <b>LVGF_GROUPID</b> a <b>LVGROUP.mask</b> e de definir <b>LVGROUP.iGroupId</b> como a nova ID. A chamada falhará se <b>LVGROUP.iGroupId</b> contiver a ID de um grupo existente.

Para atualizar outras propriedades de um grupo existente (por exemplo, atualizar um alinhamento do texto de rodapé ou de rodapé para o grupo, <b>uAlign</b>) <b>LVGROUP.mask</b> não deve conter LVGF_GROUPID , <b>caso contrário, a</b>atualização falhará.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





