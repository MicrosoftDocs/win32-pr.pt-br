---
title: Função RasAdminPortClearStatistics (Rassapi.h)
description: A função RasAdminPortClearStatistics redefine os contadores que representam as várias estatísticas relatadas pela função RasAdminPortGetInfo na estrutura RAS \_ PORT \_ STATISTICS. Os contadores são redefinidos para zero e começam a se acumular.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics função RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da7d17516e7dd7708821a7c60c2d93db913f25c38471524367ae96494e41f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788983"
---
# <a name="rasadminportclearstatistics-function"></a>Função RasAdminPortClearStatistics

\[Essa função é fornecida apenas para compatibilidade com compatibilidade com Windows NT Server 4.0. Ele retorna ERROR \_ CALL NOT IMPLEMENTED no Windows Server \_ \_ 2003. Os aplicativos devem usar [**a função MprAdminPortClearStats.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)\]

A **função RasAdminPortClearStatistics** redefine os contadores que representam as várias estatísticas relatadas pela [**função RasAdminPortGetInfo**](rasadminportgetinfo.md) na estrutura [**RAS PORT \_ \_ STATISTICS.**](ras-port-statistics-str.md) Os contadores são redefinidos para zero e começam a se acumular.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS. Especifique o nome com \\ \\ os caracteres " " à frente, no formato: \\ \\ *servername*.

</dd> <dt>

*lpszPort* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta no servidor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno poderá ser o código de erro a seguir.



| Valor                                                                                                 | Significado                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**O \_ DEV \_ DE ERRO NÃO \_ EXISTE**</dt> </dl> | A porta especificada é inválida.<br/> |



 

Não há informações de erro estendidas para essa função; não chame [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentários

A **função RasAdminPortClearStatistics** limpa as estatísticas no servidor, não localmente dentro do aplicativo que faz a chamada. Isso significa que as estatísticas também são redefinidas para qualquer outro aplicativo que está monitorando a porta especificada.

Se a porta *lpszPort* faz parte de uma conexão multilink, **RasAdminPortClearStatistics** redefine as estatísticas para a porta especificada, a função também redefine as estatísticas cumulativas para a conexão multilink. No entanto, a função não efetiva as estatísticas individuais para outras portas que fazem parte da conexão multilink.

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

[**ESTATÍSTICAS \_ DE \_ PORTA RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

