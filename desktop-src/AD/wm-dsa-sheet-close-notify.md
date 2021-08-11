---
title: WM_DSA_SHEET_CLOSE_NOTIFY mensagem
description: Postado no snap-in do MMC do Active Directory quando uma folha de propriedades secundária é destruída.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY mensagem do Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840790de51ce712b33fc9a9611934e8be9a76a35a0fc01a4ce0abe4ba040d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181659"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>Mensagem WM \_ DSA \_ SHEET \_ CLOSE \_ NOTIFY

A **mensagem WM \_ DSA \_ SHEET CLOSE \_ \_ NOTIFY** é postada no snap-in do MMC do Active Directory quando uma folha de propriedades secundária é destruída.

> [!Note]  
> Esse valor da mensagem não está definido em um arquivo de header publicado. Para usar esse valor de mensagem, você deve defini-lo por conta própria no formato exato mostrado.

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
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

Contém um valor de 32 bits definido pelo aplicativo. Isso é obtido do **membro wParamSheetClose** da [**estrutura PROPSHEETCFG.**](propsheetcfg.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 





