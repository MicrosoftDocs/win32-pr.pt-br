---
title: Mensagem de LVM_GETGROUPINFO (commctrl. h)
description: Obtém informações do grupo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- controles de Windows de mensagem de LVM_GETGROUPINFO
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
ms.openlocfilehash: f5c48a21a1bba0c6dd1af3fd567ea853dc922591c553ea11a935fb705ad65bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411390"
---
# <a name="lvm_getgroupinfo-message"></a>\_Mensagem GETGROUPINFO LVM

Obtém informações do grupo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Uma ID que especifica o grupo cujas informações são recuperadas.</dd> <dt>

*lParam* 
</dt> <dd>Um ponteiro de uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que recebe as informações recuperadas. Defina o membro **cbSize** dessa estrutura como sizeof (LVGROUP). </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a ID do grupo se for bem-sucedida ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Antes de tentar recuperar o cabeçalho de um grupo, primeiro verifique se o grupo não tem o \_ estilo NOheader LBGS.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





