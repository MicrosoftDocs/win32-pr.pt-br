---
title: WM_DSA_SHEET_CLOSE_NOTIFY mensagem
description: Postado no snap-in do Active Directory MMC quando uma folha de propriedades secundária é destruída.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769119"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>\_Mensagem de \_ notificação de fechamento da folha do DSA do \_ WM \_

A mensagem de **\_ notificação de \_ \_ fechamento \_ da folha DSA do WM** é postada no snap-in do Active Directory MMC quando uma folha de propriedades secundária é destruída.

> [!Note]  
> Esse valor de mensagem não está definido em um arquivo de cabeçalho publicado. Para usar esse valor de mensagem, você mesmo deve defini-lo no formato exato mostrado.

 


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

*HWND* 
</dt> <dd>

O identificador de janela da janela de snap-in que processará essa mensagem. Esse identificador é obtido do membro **hwndHidden** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Contém um valor de 32 bits definido pelo aplicativo. Isso é obtido do membro **wParamSheetClose** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 





