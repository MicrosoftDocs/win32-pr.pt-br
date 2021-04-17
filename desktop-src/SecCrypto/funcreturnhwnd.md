---
description: Usado por um CSP (provedor de serviços de criptografia) para obter o identificador de janela que o CSP deve usar como pai ou proprietário de qualquer interface do usuário que é exibida.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: Ponteiro de função CRYPT_RETURN_HWND (Cspdk. h)
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
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755048"
---
# <a name="crypt_return_hwnd-function-pointer"></a>\_Ponteiro de \_ função HWND de retorno cript

A função de retorno de chamada **FuncReturnhWnd** é usada por um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para obter o identificador de janela que o CSP deve usar como pai ou proprietário de qualquer interface do usuário que é exibida.

## <a name="syntax"></a>Sintaxe


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phWnd* \[ entrada, saída\]
</dt> <dd>

O endereço de uma variável **HWND** que recebe o identificador de janela pai.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse ponteiro de função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
