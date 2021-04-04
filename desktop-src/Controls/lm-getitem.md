---
title: Mensagem de LM_GETITEM (commctrl. h)
description: Recupera os Estados e atributos de um item.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- Controles de LM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085183"
---
# <a name="lm_getitem-message"></a>\_Mensagem GETITEM de LM

Recupera os Estados e atributos de um item.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser **NULL**. </dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> a ser preenchida com informações sobre o item. </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a mensagem tiver sucesso ao obter os valores e os atributos especificados.

## <a name="remarks"></a>Comentários

Com a **mensagem \_ GETITEM do LM** , os links só podem ser acessados por meio do índice numérico retornado no membro **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem). Não há suporte para o acesso ao link por meio do nome de ID retornado em **szID** .

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





