---
title: Estrutura de RAS_PPP_PROJECTION_RESULT (Rassapi. h)
description: A \_ estrutura de \_ resultados de projeção de Ras PPP \_ é usada para relatar os resultados das várias operações de projeção de PPP para uma porta.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS da estrutura de RAS_PPP_PROJECTION_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce1bb82b34490f8a1f3734225cbde1e761c575a2019a30db7790bfc7fa3c169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789580"
---
# <a name="ras_ppp_projection_result-structure"></a>\_Estrutura de \_ resultados da projeção do RAS PPP \_

\[a estrutura de **\_ \_ \_ resultados de projeção de RAS PPP** não tem suporte a partir do Windows Vista.\]

A estrutura de **\_ \_ \_ resultados de projeção de Ras PPP** é usada para relatar os resultados das várias operações de projeção de PPP para uma porta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**nbf**
</dt> <dd>

Uma estrutura de [**\_ resultado de \_ NBFCP \_ RAS PPP**](ras-ppp-nbfcp-result-str.md) que relata o resultado de uma operação de projeção NBF (PPP NetBEUI Framer).

</dd> <dt>

**IP**
</dt> <dd>

Uma estrutura de resultado do protocolo [**\_ \_ IPCP \_ de Ras PPP**](ras-ppp-ipcp-result-str.md) que relata o resultado de uma operação de projeção de IP (PPP Internet Protocol).

</dd> <dt>

**IPX**
</dt> <dd>

uma estrutura de [**\_ \_ \_ resultados do protocolo**](ras-ppp-ipxcp-result-str.md) de rede ip do ppp do RAS que relata o resultado de uma operação de projeção IPX (Exchange de pacotes de internet ppp).

</dd> <dt>

**at**
</dt> <dd>

Uma estrutura de [**\_ resultados do protocolo \_ ATCP \_ do RAS**](ras-ppp-atcp-result-str.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura relata os resultados da projeção para protocolos NetBEUI, TCP/IP e IPX. Cada estrutura PPP tem um membro **dwError** que indica se as outras informações na estrutura são válidas. Se **dwError** não for um \_ erro, as outras informações serão válidas. Se **dwError** for um dos códigos de erro em Winerror. h ou Raserror. h, as outras informações não serão válidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração do servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Porta RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**resultado do ATCP do RAS \_ PPP \_ \_**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**resultado do IPCP de RAS \_ PPP \_ \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**resultado de IPXCP do RAS \_ PPP \_ \_**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**\_resultado de \_ NBFCP RAS PPP \_**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





