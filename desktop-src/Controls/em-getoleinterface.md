---
title: Mensagem de EM_GETOLEINTERFACE (RichEdit. h)
description: Recupera um objeto IRichEditOle que um cliente pode usar para acessar uma funcionalidade COM (Component Object Model de controle de edição rica).
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- Controles de EM_GETOLEINTERFACE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085935"
---
# <a name="em_getoleinterface-message"></a>\_Mensagem em GETOLEINTERFACE

Recupera um objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) que um cliente pode usar para acessar uma funcionalidade COM (Component Object Model de controle de edição rica).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um ponteiro que recebe o objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) . O controle chama o método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para o objeto antes de retornar, portanto, o aplicativo de chamada deve chamar o método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando ele é feito com o objeto.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

