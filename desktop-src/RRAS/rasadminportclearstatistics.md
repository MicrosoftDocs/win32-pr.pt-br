---
title: Função RasAdminPortClearStatistics (Rassapi. h)
description: A função RasAdminPortClearStatistics redefine os contadores que representam as várias estatísticas relatadas pela função RasAdminPortGetInfo na \_ estrutura de estatísticas de porta de Ras \_ . Os contadores são redefinidos para zero e começam a acumular.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- Função RasAdminPortClearStatistics RAS
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
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750105"
---
# <a name="rasadminportclearstatistics-function"></a>Função RasAdminPortClearStatistics

\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0. Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]

A função **RasAdminPortClearStatistics** redefine os contadores que representam as várias estatísticas relatadas pela função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) na estrutura de [**\_ \_ Estatísticas de porta de Ras**](ras-port-statistics-str.md) . Os contadores são redefinidos para zero e começam a acumular.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS. Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.

</dd> <dt>

*lpszPort* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta no servidor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.



| Valor                                                                                                 | Significado                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_desenvolvimento de \_ erro \_ inexistente**</dt> </dl> | A porta especificada é inválida.<br/> |



 

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

A função **RasAdminPortClearStatistics** limpa as estatísticas no servidor, não localmente no aplicativo que faz a chamada. Isso significa que as estatísticas também são redefinidas para qualquer outro aplicativo que esteja monitorando a porta especificada.

Se a porta *lpszPort* fizer parte de uma conexão Multilink, o **RasAdminPortClearStatistics** redefinirá as estatísticas para a porta especificada, a função também redefinirá as estatísticas cumulativas para a conexão de vínculos múltiplos. No entanto, a função não afeta as estatísticas individuais para outras portas que fazem parte da conexão de vínculos múltiplos.

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

[**\_Estatísticas de porta RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

