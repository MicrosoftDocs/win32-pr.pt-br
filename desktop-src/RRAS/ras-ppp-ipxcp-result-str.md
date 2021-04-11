---
title: Estrutura de RAS_PPP_IPXCP_RESULT (Rassapi. h)
description: A \_ estrutura de resultados do protocolo PPP do RAS \_ \_ é usada para relatar o resultado de uma operação de projeção de intercâmbio de pacotes de rede PPP (IPX) para uma porta.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS da estrutura de RAS_PPP_IPXCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009444"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>Estrutura de resultados do protocolo RAS \_ PPP \_ \_

\[Não há suporte para a estrutura de **\_ \_ \_ resultado do protocolo RAS PPP** no Windows Vista.\]

A estrutura de **\_ \_ \_ resultados do protocolo PPP do RAS** é usada para relatar o resultado de uma operação de projeção de intercâmbio de pacotes de rede PPP (IPX) para uma porta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwError**
</dt> <dd>

Indica os resultados da operação de projeção IPX. Um valor sem \_ erro indica êxito; nesse caso, o membro **wszAddress** é válido. Se a operação de projeção não foi bem-sucedida, **dwError** é um código de erro de Winerror. h ou Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o Endereço IPX atribuído ao cliente remoto. Essa cadeia de caracteres tem o * NET ***.** formulário de _nó_ .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração do servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Porta RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_resultado da \_ projeção do RAS PPP \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





