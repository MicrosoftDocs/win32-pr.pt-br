---
title: RAS_PPP_IPCP_RESULT estrutura (Rassapi.h)
description: A estrutura RAS PPP IPCP RESULT é usada para relatar o resultado de uma operação de projeção de \_ \_ IP \_ (protocolo IP) PPP para uma porta.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- ras RAS_PPP_IPCP_RESULT estrutura de RAS_PPP_IPCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0425289b7ffd686f0d908f9789a2c24606978f37e05dfada5b937b8ce05b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789610"
---
# <a name="ras_ppp_ipcp_result-structure"></a>Estrutura RAS \_ PPP \_ IPCP \_ RESULT

\[A **estrutura RAS PPP \_ \_ IPCP \_ RESULT** não tem suporte desde Windows Vista.\]

A **estrutura RAS PPP \_ \_ IPCP \_ RESULT** é usada para relatar o resultado de uma operação de projeção de IP (protocolo IP) PPP para uma porta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwerror**
</dt> <dd>

Indica os resultados da operação de projeção de IP. Um valor de NO \_ ERROR indica êxito; nesse caso, o **membro wszAddress** é válido. Se a operação de projeção não tiver sido bem-sucedida, **dwError** será um código de erro de Winerror.h ou Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o endereço IP atribuído ao cliente remoto. Essa cadeia de caracteres tem *o formato a***.** _b_* _._ *_c_*_._ * _d_.

</dd> </dl>

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

[**RESULTADO DA \_ \_ PROJEÇÃO RAS \_ PPP**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





