---
title: Mensagem de PSM_QUERYSIBLINGS (Prsht. h)
description: Enviado a uma folha de propriedades, que, em seguida, encaminha a mensagem para cada uma de suas páginas. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- Controles de PSM_QUERYSIBLINGS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499437"
---
# <a name="psm_querysiblings-message"></a>Mensagem de PSM \_ QUERYSIBLINGS

Enviado a uma folha de propriedades, que, em seguida, encaminha a mensagem para cada uma de suas páginas. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Primeiro parâmetro definido pelo aplicativo.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parâmetro definido pelo aplicativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor diferente de zero de uma página na folha de propriedades ou zero se nenhuma página retornar um valor diferente de zero.

## <a name="remarks"></a>Comentários

Se uma página retornar um valor diferente de zero, a folha de propriedades não enviará a mensagem para as páginas subsequentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





