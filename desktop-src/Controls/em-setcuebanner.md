---
title: Mensagem de EM_SETCUEBANNER (commctrl. h)
description: Define a indicação textual ou Tip, que é exibida pelo controle de edição para solicitar informações ao usuário.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- controles de Windows de mensagem de EM_SETCUEBANNER
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08694d7368a994c639f236f18537e13d81f57083521599c23671941c74889bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673099"
---
# <a name="em_setcuebanner-message"></a>\_Mensagem em SETCUEBANNER

Define a indicação textual ou Tip, que é exibida pelo controle de edição para solicitar informações ao usuário.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

**True** se a faixa de indicação deve ser mostrada mesmo quando o controle de edição tem foco; caso contrário, **false**. **False** é o comportamento padrão que a faixa de indicação desaparece quando o usuário clica no controle.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que contém o texto a ser exibido como a indicação textual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver sucesso, retornará **true**. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Um controle de edição que é usado para iniciar uma pesquisa pode exibir "Insira a pesquisa aqui" em texto cinza como uma indicação textual. Quando o usuário clica no texto, o texto desaparece e o usuário pode digitar.

Não é possível definir uma faixa de indicação em um controle de edição de várias linhas ou em um controle de edição com formatação.

> [!Note]  
> Para usar essa API, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Editar \_ SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





