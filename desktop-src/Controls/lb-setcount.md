---
title: Mensagem de LB_SETCOUNT (WinUser. h)
description: Define a contagem de itens em uma caixa de listagem criada com o \_ estilo NOdata de lbs e não é criada com o \_ estilo lbs HASSTRINGS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- Controles de LB_SETCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009653"
---
# <a name="lb_setcount-message"></a>\_Mensagem do número de contagem lb

Define a contagem de itens em uma caixa de listagem criada com o estilo [**\_ NODATA de lbs**](list-box-styles.md) e não é criada com o estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a nova contagem de itens na caixa de listagem.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será um erro de LB \_ . Se não houver memória suficiente para armazenar os itens, o valor de retorno será LB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

Há suporte para a mensagem de **\_ número de lb** somente por caixas de listagem criadas com o estilo do [**lbs \_ NODATA**](list-box-styles.md) e não criadas com o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) . Todas as outras caixas de listagem retornam o \_ erro lb.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetCount de LB \_**](lb-getcount.md)
</dt> </dl>

 

 





