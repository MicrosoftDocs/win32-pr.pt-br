---
title: Mensagem de EM_GETCUEBANNER (commctrl. h)
description: Obtém o texto que é exibido como a indicação textual, ou Tip, em um controle de edição.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Controles de EM_GETCUEBANNER de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919128"
---
# <a name="em_getcuebanner-message"></a>\_Mensagem em GETCUEBANNER

Obtém o texto que é exibido como a indicação textual, ou Tip, em um controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um ponteiro para um buffer Unicode que recebe o texto definido como a indicação textual. O chamador é responsável por alocar o buffer.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

O tamanho do buffer apontado por *wParam* em **WCHAR**, incluindo o **nulo** de terminação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Editar \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





