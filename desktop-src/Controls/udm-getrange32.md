---
title: Mensagem de UDM_GETRANGE32 (commctrl. h)
description: Recupera o intervalo de 32 bits de um controle acima-abaixo.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- Controles de UDM_GETRANGE32 de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455004"
---
# <a name="udm_getrange32-message"></a>\_Mensagem de GETRANGE32 UDM

Recupera o intervalo de 32 bits de um controle acima-abaixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para um inteiro assinado que recebe o limite inferior do intervalo de controle acima-abaixo. Esse parâmetro pode ser **nulo**.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um inteiro assinado que recebe o limite superior do intervalo de controle acima-abaixo. Esse parâmetro pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





