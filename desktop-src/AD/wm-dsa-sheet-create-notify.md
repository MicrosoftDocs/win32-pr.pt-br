---
title: WM_DSA_SHEET_CREATE_NOTIFY mensagem
description: Postado no snap-in do Active Directory MMC para criar uma folha de propriedades secundária.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918527"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>\_Folha DSA do WM \_ \_ criar notificação de \_ mensagem

A mensagem de **\_ \_ \_ notificação criar \_ notificar do WM DSA sheet** é postada no snap-in Active Directory MMC para criar uma folha de propriedades secundária.

> [!Note]  
> Esse valor de mensagem não está definido em um arquivo de cabeçalho publicado. Para usar esse valor de mensagem, defina-o no formato exato mostrado.

 


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

*HWND* 
</dt> <dd>

O identificador de janela da janela de snap-in que processará essa mensagem. Esse identificador é obtido do membro **hwndHidden** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Contém um ponteiro para uma estrutura de [**\_ \_ \_ informações da página DSA s**](dsa-sec-page-info.md) que define a folha de propriedades secundária a ser criada. O receptor da mensagem deve liberar essa memória com a função [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) quando ela não for mais necessária.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

[**\_ \_ informações da página DSA SEC \_**](dsa-sec-page-info.md)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

