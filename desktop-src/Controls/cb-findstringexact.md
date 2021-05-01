---
title: Mensagem de CB_FINDSTRINGEXACT (WinUser. h)
description: Localiza a primeira cadeia de caracteres da caixa de listagem em uma caixa de combinação que corresponde à cadeia de caracteres especificada no parâmetro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- Controles de CB_FINDSTRINGEXACT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327171"
---
# <a name="cb_findstringexact-message"></a>\_Mensagem de FINDSTRINGEXACT CB

Localiza a primeira cadeia de caracteres da caixa de listagem em uma caixa de combinação que corresponde à cadeia de caracteres especificada no parâmetro *lParam* .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item que antecede o primeiro item a ser pesquisado. Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará na parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* . Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo para pesquisa. A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de base zero do item correspondente. Se a pesquisa não for bem-sucedida, será CB \_ Err.

## <a name="remarks"></a>Comentários

Essa função será bem-sucedida somente se a cadeia de caracteres especificada e um item de caixa de combinação tiverem o mesmo comprimento (exceto para o caractere nulo de terminação) e os mesmos caracteres.

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , a funcionalidade da mensagem **CB \_ FINDSTRINGEXACT** dependerá se o aplicativo usa o estilo de [**\_ classificação CBS**](combo-box-styles.md) . Se você usar o estilo de **\_ classificação CBS** , as mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) serão enviadas ao proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada. Se você não usar o estilo **de \_ classificação CBS** , a mensagem **CB \_ FINDSTRINGEXACT** procurará um item de lista que corresponda ao valor do parâmetro *lParam* .

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

[**localização da CB \_**](cb-findstring.md)
</dt> <dt>

[**seleção do CB \_**](cb-selectstring.md)
</dt> <dt>

[**COMPAREITEM do WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





