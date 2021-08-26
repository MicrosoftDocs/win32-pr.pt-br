---
title: Função RasAdminServerGetInfo (Rassapi. h)
description: A função RasAdminServerGetInfo Obtém a configuração de servidor de um servidor RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- Função RasAdminServerGetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f6f83f7310700e774692d876bda979343da80aa45ea8012bf187e50f0af67bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028446"
---
# <a name="rasadminservergetinfo-function"></a>Função RasAdminServerGetInfo

\[essa função é fornecida somente para compatibilidade com versões anteriores com o Windows NT Server 4,0. ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]

A função **RasAdminServerGetInfo** Obtém a configuração de servidor de um servidor RAS.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

ponteiro para uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome do servidor RAS Windows NT/Windows 2000. Se esse parâmetro for **nulo**, a função retornará informações sobre o computador local. Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.

</dd> <dt>

*pRasServer0* \[ fora\]
</dt> <dd>

Ponteiro para a estrutura do [**\_ servidor RAS \_ 0**](ras-server-0-str.md) que recebe o número de portas configuradas no servidor, o número de portas em uso no momento e o número de versão do servidor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro. Os códigos de erro possíveis incluem aqueles retornados por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para a função [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) . Não há informações de erro estendidas para esta função; Não chame **GetLastError**.

## <a name="remarks"></a>Comentários

Para enumerar todos os servidores RAS em um domínio, chame a função [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) e especifique a \_ \_ discagem do tipo VA para o parâmetro *ServerType* .

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

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**\_Servidor RAS \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

