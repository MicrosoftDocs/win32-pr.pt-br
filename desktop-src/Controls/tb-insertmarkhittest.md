---
title: Mensagem de TB_INSERTMARKHITTEST (commctrl. h)
description: Recupera as informações de marca de inserção de um ponto em uma barra de ferramentas.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- Controles de TB_INSERTMARKHITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009192"
---
# <a name="tb_insertmarkhittest-message"></a>TB de \_ mensagem INSERTMARKHITTEST

Recupera as informações de marca de inserção de um ponto em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que contém as coordenadas de teste de clique, em relação à área do cliente da barra de ferramentas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recebe as informações de marca de inserção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se o ponto for uma marca de inserção, ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

