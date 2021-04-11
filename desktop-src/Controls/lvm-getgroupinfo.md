---
title: Mensagem de LVM_GETGROUPINFO (commctrl. h)
description: Obtém informações do grupo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Controles de LVM_GETGROUPINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009201"
---
# <a name="lvm_getgroupinfo-message"></a>\_Mensagem GETGROUPINFO LVM

Obtém informações do grupo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Uma ID que especifica o grupo cujas informações são recuperadas.</dd> <dt>

*lParam* 
</dt> <dd>Um ponteiro de uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que recebe as informações recuperadas. Defina o membro **cbSize** dessa estrutura como sizeof (LVGROUP). </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a ID do grupo se for bem-sucedida ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Antes de tentar recuperar o cabeçalho de um grupo, primeiro verifique se o grupo não tem o \_ estilo NOheader LBGS.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





