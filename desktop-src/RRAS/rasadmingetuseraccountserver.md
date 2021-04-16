---
title: Função RasAdminGetUserAccountServer (Rassapi. h)
description: A função RasAdminGetUserAccountServer recupera o nome do servidor que tem o banco de dados da conta de usuário. Use o nome do servidor retornado nas funções RasAdminUserGetInfo e RasAdminUserSetInfo para obter ou definir informações sobre um usuário especificado.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- Função RasAdminGetUserAccountServer RAS
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
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779586"
---
# <a name="rasadmingetuseraccountserver-function"></a>Função RasAdminGetUserAccountServer

\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0. Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]

A função **RasAdminGetUserAccountServer** recupera o nome do servidor que tem o banco de dados da conta de usuário. Use o nome do servidor retornado nas funções [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obter ou definir informações sobre um usuário especificado.

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

*lpszDomain* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome do domínio ao qual o servidor RAS pertence. Esse parâmetro é **nulo** para os aplicativos de administração de Ras em execução em estações de trabalho ou servidores que não são membros de um domínio. Se esse parâmetro for **NULL**, o parâmetro *lpszServer* deverá ser não **nulo**.

</dd> <dt>

*lpszServer* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome do servidor RAS. Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*. Esse parâmetro poderá ser **nulo** se o parâmetro *LpszDomain* não for **nulo**.

</dd> <dt>

*lpszUserAccountServer* \[ fora\]
</dt> <dd>

Ponteiro para um buffer que recebe uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome de um controlador de domínio que tem o banco de dados de conta de usuário. O buffer deve ser grande o suficiente para conter o nome do servidor (UNCLEN + 1). A função prefixa o nome do servidor retornado com caracteres "" à esquerda \\ \\ , no formato: \\ \\ *ServerName*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.



| Valor                                                                                                    | Significado                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl> | *LpszDomain* e *lpszServer* são **nulos**.<br/> |



 

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

A função **RasAdminGetUserAccountServer** Obtém o nome do servidor com o banco de dados de contas de usuário. Essa função requer o nome do servidor RAS ou o nome do domínio no qual o servidor RAS reside.

O parâmetro *lpszDomain* deve especificar um nome de domínio válido. Esse parâmetro é **nulo** para aplicativos de administração de Ras em execução em servidores que não são membros de um domínio (por exemplo, o servidor está em seu próprio grupo de trabalho). Nesse caso, o parâmetro *lpszServer* deve especificar o nome do servidor. Para obter o nome do servidor, chame a função [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) . Certifique-se de prefixar o nome do servidor com os \\ \\ caracteres "".

Se o nome do servidor especificado por *lpszServer* for um servidor autônomo (ou seja, o servidor ou a estação de trabalho não for um membro de um domínio), o nome do servidor em si será retornado no buffer *lpszUserAccountServer* .

Em seguida, use o nome do servidor de conta de usuário em uma chamada para a função [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar os usuários no banco de dados de conta de usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/> | Windows 2000 Server<br/>                                                         |
| parâmetro<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funções de administração do servidor RAS](ras-server-administration-functions.md)
</dt> <dt>

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

