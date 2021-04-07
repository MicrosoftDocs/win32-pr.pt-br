---
title: Mensagem de EM_SETOLECALLBACK (RichEdit. h)
description: Fornece um controle de edição rico de um objeto IRichEditOleCallback que o controle usa para obter informações e recursos relacionados ao OLE do cliente.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- Controles de EM_SETOLECALLBACK de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918618"
---
# <a name="em_setolecallback-message"></a>\_Mensagem em SETOLECALLBACK

Fornece um controle de edição rico de um objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) que o controle usa para obter informações e recursos relacionados ao OLE do cliente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um objeto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) . O controle chama o método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para o objeto antes de retornar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

