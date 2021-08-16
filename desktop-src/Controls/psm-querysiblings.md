---
title: Mensagem de PSM_QUERYSIBLINGS (Prsht. h)
description: Enviado a uma folha de propriedades, que, em seguida, encaminha a mensagem para cada uma de suas páginas. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- controles de Windows de mensagem de PSM_QUERYSIBLINGS
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
ms.openlocfilehash: c270a3c7a667894f7821f6c0c169115846b6ddc2492648f5f9d75a0c85d21d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088646"
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

## <a name="return-value"></a>Valor retornado

Retorna o valor diferente de zero de uma página na folha de propriedades ou zero se nenhuma página retornar um valor diferente de zero.

## <a name="remarks"></a>Comentários

Se uma página retornar um valor diferente de zero, a folha de propriedades não enviará a mensagem para as páginas subsequentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





