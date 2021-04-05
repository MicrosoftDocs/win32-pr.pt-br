---
title: Mensagem de RB_GETBANDINFO (commctrl. h)
description: Recupera informações sobre uma faixa especificada em um controle rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- Controles de RB_GETBANDINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085926"
---
# <a name="rb_getbandinfo-message"></a>\_Mensagem GETBANDINFO RB

Recupera informações sobre uma faixa especificada em um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da banda para a qual as informações serão recuperadas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que receberá as informações de banda solicitadas. Antes de enviar essa mensagem, você deve definir o membro **cbSize** dessa estrutura como o tamanho da estrutura **REBARBANDINFO** e definir o membro **fMask** para os itens que você deseja recuperar. Além disso, você deve definir o membro **cch** da estrutura **REBARBANDINFO** para o tamanho do buffer **lpText** quando o \_ texto RBBIM for especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) e **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





