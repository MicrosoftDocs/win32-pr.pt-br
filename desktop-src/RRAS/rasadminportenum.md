---
title: Função RasAdminPortEnum (Rassapi. h)
description: A função RasAdminPortEnum enumera todas as portas no servidor RAS especificado. Para cada porta no servidor, a função retorna a estrutura de \_ porta \_ 0 do RAS que contém informações sobre a porta.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- Função RasAdminPortEnum RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b86cbf78a47a62c8d98799ac18adf987cbe623dc92e703537c54b54bf892a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788868"
---
# <a name="rasadminportenum-function"></a>Função RasAdminPortEnum

\[essa função é fornecida somente para compatibilidade com versões anteriores com o Windows NT Server 4,0. ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]

A função **RasAdminPortEnum** enumera todas as portas no servidor RAS especificado. Para cada porta no servidor, a função retorna a estrutura [**de \_ porta \_ 0 do RAS**](ras-port-0-str.md) que contém informações sobre a porta.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS. Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.

</dd> <dt>

*ppRasPort0* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe um ponteiro para um buffer que contém uma matriz de estruturas de [**\_ porta RAS \_ 0**](ras-port-0-str.md) . Quando o aplicativo for concluído com a memória, libere-o chamando a função [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> <dt>

*pcEntriesRead* \[ fora\]
</dt> <dd>

Ponteiro para uma variável de 16 bits que recebe o número total de estruturas de [**porta do RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) retornadas na matriz *ppRasPort0* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.



| Valor                                                                                             | Significado                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NERR \_ ItemNotFound**</dt> </dl> | Nenhuma porta pode ser enumerada. Isso pode ocorrer porque todas as portas configuradas no servidor estão sendo usadas para a discagem.<br/> |



 

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
</dt> <dt>

[**\_Porta RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

