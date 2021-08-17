---
title: EM_GETOLEINTERFACE mensagem (Richedit.h)
description: Recupera um objeto IRichEditOle que um cliente pode usar para acessar a funcionalidade COM (Component Object Model) de um controle de edição avançada.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE controles de Windows mensagem
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
ms.openlocfilehash: e4e1799039081ed8250cb062aa3d1348a2fe8a8dbdcfa768fab74855d18d8e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831667"
---
# <a name="em_getoleinterface-message"></a>Mensagem EM \_ GETOLEINTERFACE

Recupera um [**objeto IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) que um cliente pode usar para acessar a funcionalidade COM (Component Object Model) de um controle de edição avançada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um ponteiro que recebe o [**objeto IRichEditOle.**](/windows/desktop/api/Richole/nn-richole-iricheditole) O controle chama o [**método AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para o objeto antes de retornar, portanto, o aplicativo de chamada deve chamar o método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando terminar com o objeto .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for bem-sucedida, o valor de retorno será um valor não zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

