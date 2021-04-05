---
title: Estrutura de RAS_PPP_NBFCP_RESULT (Rassapi. h)
description: A estrutura de resultado do NBFCP do RAS \_ PPP \_ \_ é usada para relatar o resultado de uma operação de projeção NBF (PPP NetBEUI Framer) para uma porta.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS da estrutura de RAS_PPP_NBFCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085662"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>\_Estrutura de \_ resultado de NBFCP RAS PPP \_

\[A estrutura de **resultado do RAS \_ PPP \_ NBFCP \_** não tem suporte no Windows Vista.\]

A estrutura de **\_ resultado do \_ NBFCP \_ do RAS PPP** é usada para relatar o resultado de uma operação de projeção NBF (PPP NetBEUI Framer) para uma porta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwError**
</dt> <dd>

Indica os resultados da operação de projeção NBF. Um valor sem \_ erro indica êxito; nesse caso, o membro **wszWksta** contém o nome do computador remoto. Se a operação de projeção não foi bem-sucedida, **dwError** é um código de erro de Winerror. h ou Raserror. h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Ignorar este membro no servidor; Ele é relevante apenas no cliente.

</dd> <dt>

**szName**
</dt> <dd>

Ignorar este membro no servidor; Ele é relevante apenas no cliente.

</dd> <dt>

**wszWksta**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome NetBIOS da estação de trabalho do cliente RAS.

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

 

 





