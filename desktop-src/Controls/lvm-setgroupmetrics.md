---
title: Mensagem de LVM_SETGROUPMETRICS (commctrl. h)
description: Define informações sobre a exibição de grupos.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- controles de Windows de mensagem de LVM_SETGROUPMETRICS
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f978c763fd1602d06f921a5da38a895fb1d3c76573341d9ca4f2987a0d3c7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077256"
---
# <a name="lvm_setgroupmetrics-message"></a>\_Mensagem SETGROUPMETRICS LVM

Define informações sobre a exibição de grupos.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser **NULL**.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> que contém as métricas a serem definidas.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





