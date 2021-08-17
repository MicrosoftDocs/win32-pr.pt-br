---
title: Função RasAdminUserGetInfo (Rassapi.h)
description: A função RasAdminUserGetInfo obtém as permissões RAS e as informações de número de telefone de retorno de chamada para um usuário especificado.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- Função RasAdminUserGetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4cda41447af832bd4ae04a14c6f8038fee4b61a17ac98c919c0b085261b242d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788680"
---
# <a name="rasadminusergetinfo-function"></a>Função RasAdminUserGetInfo

\[Essa função é fornecida apenas para compatibilidade com compatibilidade com Windows NT Server 4.0. Ele retorna ERROR \_ CALL NOT IMPLEMENTED no Windows Server \_ \_ 2003. Os aplicativos devem usar [**a função MprAdminUserGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)\]

A **função RasAdminUserGetInfo** obtém as permissões RAS e as informações de número de telefone de retorno de chamada para um usuário especificado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszUserAccountServer* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do controlador de domínio primário ou de backup que tem o banco de dados da conta de usuário. Use a [**função RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter esse nome de servidor.

</dd> <dt>

*lpszUser* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário para o qual obter informações de RAS.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Ponteiro para a [**estrutura \_ RAS USER \_ 0**](ras-user-0-str.md) que recebe os dados RAS para o usuário especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno poderá ser o código de erro a seguir.



| Valor                                                                                            | Significado                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl> | Memória insuficiente para executar essa função.<br/> |



 

Não há informações de erro estendidas para essa função; não chame [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fim do suporte ao servidor<br/> | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do RAS (Serviço de Acesso Remoto)](about-remote-access-service.md)
</dt> <dt>

[Funções de administração de servidor RAS](ras-server-administration-functions.md)
</dt> <dt>

[**USUÁRIO \_ RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

