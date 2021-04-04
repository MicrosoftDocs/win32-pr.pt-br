---
title: Mensagem de LM_SETITEM (commctrl. h)
description: Define os Estados e atributos de um item.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- Controles de LM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085181"
---
# <a name="lm_setitem-message"></a>\_Mensagem SETITEM de LM

Define os Estados e atributos de um item.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser **NULL**. </dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> que contém os novos Estados e atributos desejados para o link. </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a mensagem tiver sucesso na definição dos valores e atributos especificados.

## <a name="remarks"></a>Comentários

Com a [**mensagem \_ GETITEM do LM**](lm-getitem.md) , os links só podem ser acessados por meio do índice numérico retornado no membro **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem). Não há suporte para o acesso ao link por meio do nome de ID retornado em **szID** .

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comctl32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





