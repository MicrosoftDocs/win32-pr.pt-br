---
title: Mensagem de TCM_SETMINTABWIDTH (commctrl. h)
description: Define a largura mínima dos itens em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- Controles de TCM_SETMINTABWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749303"
---
# <a name="tcm_setmintabwidth-message"></a>\_Mensagem SETMINTABWIDTH de TCM

Define a largura mínima dos itens em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Largura mínima a ser definida para um item de controle de guia. Se esse parâmetro for definido como-1, o controle usará a largura de guia padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor INT que representa a largura de tabulação mínima anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





