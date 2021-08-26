---
title: Função RasAdminGetUserAccountServer (Rassapi.h)
description: A função RasAdminGetUserAccountServer recupera o nome do servidor que tem o banco de dados da conta de usuário. Use o nome do servidor retornado nas funções RasAdminUserGetInfo e RasAdminUserSetInfo para obter ou definir informações sobre um usuário especificado.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer função RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2ac4052ad4638c3e0e2483adb68857f4c2b670322434107d93100b6a177855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028536"
---
# <a name="rasadmingetuseraccountserver-function"></a>Função RasAdminGetUserAccountServer

\[Essa função é fornecida apenas para compatibilidade com compatibilidade com Windows NT Server 4.0. Ele retorna ERROR \_ CALL NOT IMPLEMENTED no Windows Server \_ \_ 2003. Os aplicativos devem usar [**a função MprAdminGetPDCServer.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)\]

A **função RasAdminGetUserAccountServer** recupera o nome do servidor que tem o banco de dados da conta de usuário. Use o nome do servidor retornado nas funções [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obter ou definir informações sobre um usuário especificado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszDomain* \[ Em\]
</dt> <dd>

Ponteiro para uma **cadeia de** caracteres Unicode terminada em nulo que especifica o nome do domínio ao qual o servidor RAS pertence. Esse parâmetro é **NULL para** os aplicativos de administração RAS em execução em estações de trabalho ou servidores que não são membros de um domínio. Se esse parâmetro for **NULL,** *o parâmetro lpszServer* deverá ser não **NULL.**

</dd> <dt>

*lpszServer* \[ Em\]
</dt> <dd>

Ponteiro para uma **cadeia de** caracteres Unicode terminada em nulo que especifica o nome do servidor RAS. Especifique o nome com \\ \\ os caracteres " " à frente, no formato: \\ \\ *servername*. Esse parâmetro poderá ser **NULL** se *o parâmetro lpszDomain* não for **NULL.**

</dd> <dt>

*lpszUserAccountServer* \[ out\]
</dt> <dd>

Ponteiro para um buffer que recebe uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de um controlador de domínio que tem o banco de dados da conta de usuário. O buffer deve ser grande o suficiente para manter o nome do servidor (TAMBÉMN +1). A função prefixa o nome do servidor retornado com caracteres \\ \\ "" à frente, no formato: \\ \\ *servername*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno poderá ser o código de erro a seguir.



| Valor                                                                                                    | Significado                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**ERRO \_ PARÂMETRO \_ INVÁLIDO**</dt> </dl> | *LpszDomain e* *lpszServer são* **NULL.**<br/> |



 

Não há informações de erro estendidas para essa função; não chame [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentários

A **função RasAdminGetUserAccountServer** obtém o nome do servidor com o banco de dados de contas de usuário. Essa função requer o nome do servidor RAS ou o nome do domínio no qual o servidor RAS reside.

O *parâmetro lpszDomain* deve especificar um nome de domínio válido. Esse parâmetro é **NULL para** aplicativos de administração RAS em execução em servidores que não são membros de um domínio (por exemplo, o servidor está em seu próprio grupo de trabalho). Nesse caso, o *parâmetro lpszServer* deve especificar o nome do servidor. Para obter o nome do servidor, chame a [**função GetComputerName.**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) Certifique-se de prefixar o nome do servidor com os \\ \\ caracteres " ".

Se o nome do servidor especificado por *lpszServer* for um servidor autônomo (ou seja, o servidor ou estação de trabalho não for membro de um domínio), o nome do servidor em si será retornado no buffer *lpszUserAccountServer.*

Em seguida, use o nome do servidor de conta de usuário em uma chamada para a função [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar os usuários no banco de dados da conta de usuário.

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

