---
title: Função RasAdminPortGetInfo (Rassapi. h)
description: A função RasAdminPortGetInfo recupera informações sobre uma porta especificada em um servidor especificado.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- Função RasAdminPortGetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785396"
---
# <a name="rasadminportgetinfo-function"></a>Função RasAdminPortGetInfo

\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0. Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]

A função **RasAdminPortGetInfo** recupera informações sobre uma porta especificada em um servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
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

</dd> <dt>

*pRasPort1* \[ fora\]
</dt> <dd>

Ponteiro para a estrutura da [**porta do RAS \_ \_ 1**](ras-port-1-str.md) que a função preenche com informações sobre o estado da porta.

</dd> <dt>

*pRasStats* \[ fora\]
</dt> <dd>

Ponteiro para a estrutura de [**\_ \_ Estatísticas de porta de Ras**](ras-port-statistics-str.md) que a função preenche com estatísticas sobre a porta.

</dd> <dt>

*ppRasParams* \[ fora\]
</dt> <dd>

Ponteiro para uma variável de ponteiro que recebe o endereço de uma matriz de estruturas de [**\_ parâmetros de Ras**](ras-parameters-str.md) . Cada estrutura contém o nome de uma chave específica de mídia, como MAXCONNECTBPS, e seu valor associado. Quando o aplicativo for concluído com essa memória, libere-o chamando a função [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.



| Valor                                                                                                     | Significado                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_desenvolvimento de \_ erro \_ inexistente**</dt> </dl>     | A porta especificada é inválida.<br/>                                        |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl> | Memória insuficiente para alocar um buffer para a matriz *ppRasParams* .<br/> |



 

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

[**parâmetros de RAS \_**](ras-parameters-str.md)
</dt> <dt>

[**\_Porta RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_Estatísticas de porta RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

