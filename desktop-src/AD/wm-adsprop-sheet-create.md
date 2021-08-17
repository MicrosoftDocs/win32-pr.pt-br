---
title: WM_ADSPROP_SHEET_CREATE mensagem
description: Enviado ao objeto de notificação para criar uma folha de propriedades secundária em um Active Directory snap-in do MMC.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ec88eaed682fd16fecb717b851b902d5ba52ce08d5360aa78b881a4b8cb4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024194"
---
# <a name="wm_adsprop_sheet_create-message"></a>\_ \_ Página \_ criar mensagem do WM ADSPROP

A mensagem de **\_ criação da \_ planilha \_ do WM ADSPROP** é enviada ao objeto de notificação para criar uma folha de propriedades secundária em um snap-in do Active Directory MMC.

> [!Note]  
> Esse valor de mensagem não está definido em um arquivo de cabeçalho publicado. Para usar esse valor de mensagem, você mesmo deve defini-lo no formato exato mostrado.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

O identificador do objeto de notificação. Para obter esse identificador, chame [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Contém um ponteiro para uma estrutura de [**\_ \_ \_ informações da página DSA s**](dsa-sec-page-info.md) que define a página secundária a ser criada. Somente uma folha de propriedades secundária pode ser criada com **a \_ planilha do WM ADSPROP \_ \_ criar** mensagem para que a estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) possa conter apenas uma estrutura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado. Deve ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem é sempre zero.

## <a name="remarks"></a>Comentários

O chamador deve alocar a estrutura de [**\_ \_ \_ informações da página DSA s**](dsa-sec-page-info.md) , a cadeia de título e todas as cadeias de caracteres [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) usando uma única chamada para a função [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) . A mensagem de **\_ criação da \_ planilha \_ do WM ADSPROP** é uma mensagem assíncrona, portanto, será retornada antes da criação da planilha secundária. Por isso, a memória deve permanecer intacta após o retorno da mensagem. O receptor liberará essa memória com uma única chamada para a função [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) depois que a planilha secundária for criada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CFSTR \_ DS \_ PARENTHWND**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**\_ \_ informações da página DSA SEC \_**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

