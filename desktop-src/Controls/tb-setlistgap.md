---
title: Mensagem de TB_SETLISTGAP (commctrl. h)
description: Define a distância entre os botões da barra de ferramentas em uma barra de ferramentas específica.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- Controles de TB_SETLISTGAP de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824148"
---
# <a name="tb_setlistgap-message"></a>TB de \_ mensagem SETLISTGAP

Define a distância entre os botões da barra de ferramentas em uma barra de ferramentas específica.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A lacuna, em pixels, entre os botões na barra de ferramentas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A lacuna entre os botões aplica-se apenas à janela de controle da barra de ferramentas que recebe essa mensagem. O recebimento dessa mensagem dispara um redesenho da barra de ferramentas, se a barra de ferramentas estiver visível no momento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





