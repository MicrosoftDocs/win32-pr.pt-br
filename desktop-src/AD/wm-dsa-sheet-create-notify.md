---
title: WM_DSA_SHEET_CREATE_NOTIFY mensagem
description: Postado no snap-in do MMC do Active Directory para criar uma folha de propriedades secundária.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY mensagem do Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51fc850504eb4455a41b881aed1109554d0482a8f889fafa2eaf7050488e450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024184"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>Mensagem WM \_ DSA \_ SHEET \_ CREATE \_ NOTIFY

A **mensagem WM \_ DSA \_ SHEET CREATE \_ \_ NOTIFY** é postada no snap-in do MMC do Active Directory para criar uma folha de propriedades secundária.

> [!Note]  
> Esse valor da mensagem não está definido em um arquivo de header publicado. Para usar esse valor de mensagem, defina-o no formato exato mostrado.

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

O alça de janela da janela de snap-in que processará essa mensagem. Esse handle é obtido do membro **hwndHidden** da [**estrutura PROPSHEETCFG.**](propsheetcfg.md)

</dd> <dt>

*wParam* 
</dt> <dd>

Contém um ponteiro para uma estrutura [**DSA \_ SEC \_ PAGE \_ INFO**](dsa-sec-page-info.md) que define a folha de propriedades secundária a ser criado. O receptor da mensagem deve liberar essa memória com a [**função LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) quando ela não for mais necessária.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Não usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> <dt>

[**INFORMAÇÕES DA PÁGINA DSA \_ SEC \_ \_**](dsa-sec-page-info.md)
</dt> <dt>

[**Localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

