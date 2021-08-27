---
title: Mensagem de IPM_SETFOCUS (commctrl. h)
description: Define o foco do teclado para o campo especificado no controle de endereço IP. Todo o texto nesse campo será selecionado.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- controles de Windows de mensagem de IPM_SETFOCUS
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a74d98aa4d4259d11d7fef6e0bfdad2bfe741447ddffab27fa41545e7eda515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085566"
---
# <a name="ipm_setfocus-message"></a>\_Mensagem IPM SETFOCUS

Define o foco do teclado para o campo especificado no controle de endereço IP. Todo o texto nesse campo será selecionado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um índice de campo baseado em zero ao qual o foco deve ser definido. Se esse valor for maior que o número de campos, o foco será definido como o primeiro campo em branco. Se todos os campos não estiverem em branco, o foco será definido como o primeiro campo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





