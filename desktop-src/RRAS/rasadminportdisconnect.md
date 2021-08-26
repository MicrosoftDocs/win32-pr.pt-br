---
title: Função RasAdminPortDisconnect (Rassapi. h)
description: A função RasAdminPortDisconnect desconecta uma porta que está em uso no momento.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- Função RasAdminPortDisconnect RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a0f3abf4cee54f92c9bfd846557623de5e23fffd4724a701ca7c04aa818af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028516"
---
# <a name="rasadminportdisconnect-function"></a>Função RasAdminPortDisconnect

\[essa função é fornecida somente para compatibilidade com versões anteriores com o Windows NT Server 4,0. ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]

A função **RasAdminPortDisconnect** desconecta uma porta que está em uso no momento.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS Windows NT/Windows 2000. Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.

</dd> <dt>

*lpszPort* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta no servidor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.



| Valor                                                                                               | Significado                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**porta de erro \_ inválida \_**</dt> </dl> | A porta especificada é inválida.<br/>    |
| <dl> <dt>**NERR \_ UserNotFound**</dt> </dl>   | A porta não está em uso no momento.<br/> |



 

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/> | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funções de administração do servidor RAS](ras-server-administration-functions.md)
</dt> </dl>

 

