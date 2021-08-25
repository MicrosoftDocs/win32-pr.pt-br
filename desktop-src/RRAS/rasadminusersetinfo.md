---
title: Função RasAdminUserSetInfo (Rassapi. h)
description: A função RasAdminUserSetInfo define as permissões RAS e o número de telefone de retorno de chamada para um usuário especificado.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- Função RasAdminUserSetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51bc4b56b9aa606892002fbef0eda8036c45442c06ce06b8561afba57620b7a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028426"
---
# <a name="rasadminusersetinfo-function"></a>Função RasAdminUserSetInfo

\[essa função é fornecida somente para compatibilidade com versões anteriores com o Windows NT Server 4,0. ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]

A função **RasAdminUserSetInfo** define as permissões RAS e o número de telefone de retorno de chamada para um usuário especificado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszUserAccountServer* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do controlador de domínio primário ou de backup que tem o banco de dados de conta de usuário. Use a função [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter esse nome de servidor.

</dd> <dt>

*lpszUser* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário para quem as informações de RAS serão definidas.

</dd> <dt>

*pRasUser0* \[ no\]
</dt> <dd>

Ponteiro para a estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) que especifica os novos dados RAS para o usuário especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.



| Valor                                                                                                           | Descrição                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRO de \_ dados inválidos \_**</dt> </dl>             | O buffer *pRasUser0* contém dados inválidos.<br/>                                        |
| <dl> <dt>**ERRO \_ \_ número de retorno de chamada inválido \_**</dt> </dl> | O número de retorno de chamada especificado no buffer *pRasUser0* contém caracteres inválidos.<br/> |
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl>               | Memória insuficiente para executar esta função.<br/>                                        |



 

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Ao definir as permissões de RAS para um usuário, o membro **bfPrivilege** da estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) deve especificar pelo menos um dos sinalizadores de retorno de chamada. Por exemplo, para definir privilégios de um usuário para permitir o privilégio de discagem, mas sem privilégios de retorno de chamada, defina **bfPrivilege** como RASPRIV \_ DialinPrivilege \| RASPRIV \_ nocallback.

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
</dt> <dt>

[**Usuário do RAS \_ \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

