---
title: Mensagem de CB_GETCUEBANNER (WinUser. h)
description: Obtém o texto da faixa de indicação exibido no controle de edição de uma caixa de combinação. Envie essa mensagem explicitamente ou usando a \_ macro GetCueBannerText da ComboBox.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- controles de Windows de mensagem de CB_GETCUEBANNER
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81ddcd8123f28317726f412255f440d47f53310aa035ab34d25190658550163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089266"
---
# <a name="cb_getcuebanner-message"></a>\_Mensagem de GETCUEBANNER CB

Obtém o texto da faixa de indicação exibido no controle de edição de uma caixa de combinação. Envie essa mensagem explicitamente ou usando a macro [**\_ GetCueBannerText da ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um ponteiro para um buffer de cadeia de caracteres Unicode que recebe o texto da faixa de indicação. O aplicativo de chamada é responsável por alocar a memória para o buffer. O tamanho do buffer deve ser igual ao tamanho da cadeia de caracteres do banner de indicação em **WCHARs**, mais 1 para o encerramento **nulo** de **WCHAR**.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

O tamanho do buffer apontado por *lpcwText* em **WCHAR**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 1 se for bem-sucedido ou um valor de erro de outra forma.

Se não houver nenhum texto de faixa de indicação a ser obtido, o valor de retorno será 0. Se o aplicativo de chamada falhar em alocar um buffer ou definir *lParam* antes de enviar essa mensagem, o comportamento indefinido poderá ser resultado e o valor de retorno poderá não ser confiável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Recursos da caixa de combinação](combo-box-features.md)
</dt> </dl>

 

 





