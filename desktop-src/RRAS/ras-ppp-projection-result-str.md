---
title: RAS_PPP_PROJECTION_RESULT estrutura (Rassapi.h)
description: A estrutura RAS \_ PPP PROJECTION RESULT é usada para relatar os resultados das várias operações de \_ \_ projeção PPP para uma porta.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- ras RAS_PPP_PROJECTION_RESULT estrutura de RAS_PPP_PROJECTION_RESULT
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
# <a name="ras_ppp_projection_result-structure"></a>Estrutura DE \_ RESULTADOS \_ DA \_ PROJEÇÃO DE RAS PPP

\[A **estrutura RAS PPP PROJECTION \_ \_ \_ RESULT** não tem suporte desde Windows Vista.\]

A **estrutura RAS PPP PROJECTION \_ \_ \_ RESULT** é usada para relatar os resultados das várias operações de projeção PPP para uma porta.

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

Uma [**estrutura RAS PPP \_ \_ NBFCP \_ RESULT**](ras-ppp-nbfcp-result-str.md) que relata o resultado de uma operação de projeção ppp NetBEUI Framer (NBF).

</dd> <dt>

**Ip**
</dt> <dd>

Uma [**estrutura RAS PPP \_ \_ IPCP \_ RESULT**](ras-ppp-ipcp-result-str.md) que relata o resultado de uma operação de projeção do PROTOCOLO IP.

</dd> <dt>

**Ipx**
</dt> <dd>

Uma [**estrutura RAS PPP \_ \_ IPXCP \_ RESULT**](ras-ppp-ipxcp-result-str.md) que relata o resultado de uma operação de projeção do IPX (Pacote de Exchange) PPP.

</dd> <dt>

**at**
</dt> <dd>

Uma [**estrutura RAS PPP \_ \_ ATCP \_ RESULT.**](ras-ppp-atcp-result-str.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura relata os resultados da projeção para protocolos NetBEUI, TCP/IP e IPX. Cada estrutura PPP tem um **membro dwError** que indica se as outras informações na estrutura são válidas. Se **dwError** for NO \_ ERROR, as outras informações serão válidas. Se **dwError** for um dos códigos de erro em Winerror.h ou Raserror.h, as outras informações não serão válidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do RAS (Serviço de Acesso Remoto)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração de servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PORTA RAS \_ \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RESULTADO \_ DO RAS PPP \_ \_ ATCP**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**RESULTADO \_ DE \_ IPCP RAS \_ PPP**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ IPXCP \_ RESULT**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ NBFCP \_ RESULT**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





