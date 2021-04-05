---
title: Mensagem de CB_FINDSTRING (WinUser. h)
description: Pesquisa na caixa de listagem de uma caixa de combinação um item que começa com os caracteres em uma cadeia de caracteres especificada.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- Controles de CB_FINDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085539"
---
# <a name="cb_findstring-message"></a>Mensagem de localização do CB \_

Pesquisa na caixa de listagem de uma caixa de combinação um item que começa com os caracteres em uma cadeia de caracteres especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item que antecede o primeiro item a ser pesquisado. Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará na parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* . Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que contém os caracteres para pesquisa. A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de base zero do item correspondente. Se a pesquisa não for bem-sucedida, será CB \_ Err.

## <a name="remarks"></a>Comentários

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o que a mensagem de **\_ FindString do CB** dependerá se seu aplicativo usar o estilo de [**\_ classificação CBS**](combo-box-styles.md) . Se você usar o estilo de **\_ classificação CBS** , as mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) serão enviadas ao proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada. Se você não usar o estilo **de \_ classificação CBS** , a mensagem de **\_ FindString CB** procurará um item de lista que corresponda ao valor do parâmetro *lParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_FINDSTRINGEXACT CB**](cb-findstringexact.md)
</dt> <dt>

[**seleção do CB \_**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETcurseal**](cb-setcursel.md)
</dt> <dt>

[**COMPAREITEM do WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





