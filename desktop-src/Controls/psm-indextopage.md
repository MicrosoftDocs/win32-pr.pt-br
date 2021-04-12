---
title: Mensagem de PSM_INDEXTOPAGE (Prsht. h)
description: Obtém o índice de uma página de folha de propriedades e retorna seu identificador HPROPSHEETPAGE. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Controles de PSM_INDEXTOPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455654"
---
# <a name="psm_indextopage-message"></a>Mensagem de PSM \_ INDEXTOPAGE

Obtém o índice de uma página de folha de propriedades e retorna seu identificador HPROPSHEETPAGE. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da página.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador HPROPSHEETPAGE da página da folha de propriedades especificada por *wParam* , se bem-sucedida. Caso contrário, retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





