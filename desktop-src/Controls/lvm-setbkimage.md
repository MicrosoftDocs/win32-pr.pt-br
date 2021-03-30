---
title: Mensagem de LVM_SETBKIMAGE (commctrl. h)
description: Define a imagem de plano de fundo em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetBkImage do ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Controles de LVM_SETBKIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455429"
---
# <a name="lvm_setbkimage-message"></a>\_Mensagem SETBKIMAGE LVM

Define a imagem de plano de fundo em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetBkImage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que contém as novas informações da imagem de fundo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro. Retornará zero se o membro **ulFlags** da estrutura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) for **LVBKIF \_ Source \_ None**.

## <a name="remarks"></a>Comentários

Como o controle List-View usa OLE COM para manipular as imagens de plano de fundo, o aplicativo de chamada deve chamar [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de enviar essa mensagem. É melhor chamar uma dessas funções quando o aplicativo é inicializado e chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) ou [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) quando o aplicativo estiver sendo encerrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ SETBKIMAGEW** (Unicode) e **LVM \_ SETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_GETBKIMAGE LVM**](lvm-getbkimage.md)
</dt> </dl>

 

