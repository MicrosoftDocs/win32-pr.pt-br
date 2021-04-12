---
title: Estrutura de RAS_PPP_IPCP_RESULT (Rassapi. h)
description: A \_ estrutura de resultado do IPCP PPP de Ras \_ \_ é usada para relatar o resultado de uma operação de projeção de protocolo IP (PPP Internet Protocol) para uma porta.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS da estrutura de RAS_PPP_IPCP_RESULT
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
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499408"
---
# <a name="ras_ppp_ipcp_result-structure"></a>\_Estrutura de \_ resultado do IPCP de Ras PPP \_

\[A estrutura de **\_ resultado do protocolo \_ IPCP \_ PPP** não tem suporte no Windows Vista.\]

A estrutura de **\_ \_ \_ resultado do IPCP PPP de Ras** é usada para relatar o resultado de uma operação de projeção de protocolo IP (PPP Internet Protocol) para uma porta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwError**
</dt> <dd>

Indica os resultados da operação de projeção de IP. Um valor sem \_ erro indica êxito; nesse caso, o membro **wszAddress** é válido. Se a operação de projeção não foi bem-sucedida, **dwError** é um código de erro de Winerror. h ou Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o endereço IP atribuído ao cliente remoto. Essa cadeia de caracteres tem a forma *um ***.** _b_* _._ *_c_*_._ * _d_.

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

 

 





