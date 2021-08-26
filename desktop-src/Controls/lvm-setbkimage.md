---
title: Mensagem de LVM_SETBKIMAGE (commctrl. h)
description: Define a imagem de plano de fundo em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetBkImage do ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- controles de Windows de mensagem de LVM_SETBKIMAGE
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
ms.openlocfilehash: 4f00fbf02d4e354115c01af637251782adb9f95b11923d12cba4bc9f1a0f9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919966"
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

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro. Retornará zero se o membro **ulFlags** da estrutura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) for **LVBKIF \_ Source \_ None**.

## <a name="remarks"></a>Comentários

Como o controle List-View usa OLE COM para manipular as imagens de plano de fundo, o aplicativo de chamada deve chamar [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de enviar essa mensagem. É melhor chamar uma dessas funções quando o aplicativo é inicializado e chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) ou [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) quando o aplicativo estiver sendo encerrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ SETBKIMAGEW** (Unicode) e **LVM \_ SETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETBKIMAGE LVM**](lvm-getbkimage.md)
</dt> </dl>

 

