---
title: PSM_INDEXTOPAGE mensagem (Prsht.h)
description: Pega o índice de uma página de folha de propriedades e retorna seu alça HPROPSHEETPAGE. Você pode enviar essa mensagem explicitamente ou usar a macro \_ PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- PSM_INDEXTOPAGE controles de Windows mensagem
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
ms.openlocfilehash: 1f5cfe971ebdb85f444b20e66fcfaf77f87448f71b3a677bea104a5068daac9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078830"
---
# <a name="psm_indextopage-message"></a>Mensagem PSM \_ INDEXTOPAGE

Pega o índice de uma página de folha de propriedades e retorna seu alça HPROPSHEETPAGE. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ PropSheet IndexToPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da página.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça HPROPSHEETPAGE da página de folha de propriedades especificada por *wParam* se for bem-sucedida. Caso contrário, retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





