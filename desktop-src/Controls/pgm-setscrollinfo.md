---
title: Mensagem de PGM_SETSCROLLINFO (commctrl. h)
description: Define os parâmetros de rolagem do controle de pager, incluindo o valor de tempo limite, as linhas por tempo limite e os pixels por linha. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetScrollInfo do pager.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- Controles de PGM_SETSCROLLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824335"
---
# <a name="pgm_setscrollinfo-message"></a>\_Mensagem SETSCROLLINFO do PGM

\[Destinado ao uso interno; Não recomendado para uso em aplicativos. Essa mensagem pode não ter suporte em versões futuras do Windows.\]

Define os parâmetros de rolagem do controle de pager, incluindo o valor de tempo limite, as linhas por tempo limite e os pixels por linha. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetScrollInfo do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **uint** que especifica o valor de tempo limite para a rolagem, em milissegundos.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **uint** que especifica o número de linhas a rolar por tempo limite. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **uint** que especifica o número de pixels por linha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="security-considerations"></a>Considerações de segurança

O uso dessa mensagem pode comprometer a segurança do seu programa.

## <a name="remarks"></a>Comentários

O valor de tempo limite *wParam* controla a taxa na qual o controle de pager gera eventos de rolagem quando o controle capturou a entrada do mouse e o botão esquerdo do mouse é pressionado. Valores menores resultam em rolagem mais rápida; valores maiores resultam em uma rolagem mais lenta. O valor padrão é um oitavo do tempo de clique duplo. Para obter mais informações, consulte [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).

Por padrão, com cada evento de rolagem, o controle de pager rola um valor igual à largura ou altura inteira do controle, dependendo se o controle de pager tem uma orientação horizontal ou vertical. Os valores em *lParam* são usados para substituir o valor de rolagem padrão. Se forem fornecidos valores diferentes de zero, o valor de rolagem será o produto dos dois valores (LOWORD (*lParam*) \* HIWORD (*lParam*)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Paginar \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

