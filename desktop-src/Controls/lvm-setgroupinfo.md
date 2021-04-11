---
title: Mensagem de LVM_SETGROUPINFO (commctrl. h)
description: Define informações do grupo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- Controles de LVM_SETGROUPINFO de mensagens do Windows
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
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008858"
---
# <a name="lvm_setgroupinfo-message"></a>\_Mensagem SETGROUPINFO LVM

Define informações do grupo. Envie essa mensagem explicitamente ou usando a macro [**\_ SetGroupInfo do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>ID que especifica o grupo cujas informações serão definidas.</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>Ponteiro para uma estrutura [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) que contém as informações a serem definidas.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a ID do grupo se for bem-sucedida ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Para alterar uma ID de grupo de um grupo existente, adicione <b>LVGF_GROUPID</b> a <b>LVGROUP. Mask</b> e defina <b>LVGROUP. iGroupId</b> como a nova ID. A chamada falhará se <b>LVGROUP. iGroupId</b> contiver a ID de um grupo existente.

Para atualizar outras propriedades de um grupo existente (por exemplo, atualizar um alinhamento do texto do cabeçalho ou rodapé do grupo, <b>uAlign</b>) <b>LVGROUP. Mask</b> não deve conter <b>LVGF_GROUPID</b>, senão a atualização falhará.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





