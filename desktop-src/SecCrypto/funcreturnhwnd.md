---
description: Usado por um CSP (provedor de serviços criptográficos) para obter o controle de janela que o CSP deve usar como o pai ou proprietário de qualquer interface do usuário exibida.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND ponteiro de função (Cspdk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 387e1e9140dac8081acf851eb7125a612506783adbeefe1174137ff7f74fae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006744"
---
# <a name="crypt_return_hwnd-function-pointer"></a>Ponteiro da função CRYPT \_ RETURN \_ HWND

[*A*](../secgloss/c-gly.md) função de retorno de chamada **FuncReturnhWnd** é usada por um CSP (provedor de serviços de criptografia) para obter o alça de janela que o CSP deve usar como o pai ou proprietário de qualquer interface do usuário exibida.

## <a name="syntax"></a>Sintaxe


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phWnd* \[ in, out\]
</dt> <dd>

O endereço de uma **variável HWND** que recebe o alça de janela pai.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse ponteiro de função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
