---
title: Função RasAdminUserGetInfo (Rassapi. h)
description: A função RasAdminUserGetInfo Obtém as permissões RAS e as informações de número de telefone de retorno de chamada para um usuário especificado.
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
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759602"
---
# <a name="rasadminusergetinfo-function"></a>Função RasAdminUserGetInfo

\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0. Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]

A função **RasAdminUserGetInfo** Obtém as permissões RAS e as informações de número de telefone de retorno de chamada para um usuário especificado.

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

*lpszUserAccountServer* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do controlador de domínio primário ou de backup que tem o banco de dados de conta de usuário. Use a função [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter esse nome de servidor.

</dd> <dt>

*lpszUser* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário para quem obter informações de RAS.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Ponteiro para a estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) que recebe os dados RAS para o usuário especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.



| Valor                                                                                            | Significado                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl> | Memória insuficiente para executar esta função.<br/> |



 

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**Usuário do RAS \_ \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

