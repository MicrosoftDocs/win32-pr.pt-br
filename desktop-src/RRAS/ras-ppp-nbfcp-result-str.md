---
title: RAS_PPP_NBFCP_RESULT estrutura (Rassapi.h)
description: A estrutura RAS PPP NBFCP RESULT é usada para relatar o resultado de uma operação de projeção \_ \_ de PPP \_ NetBEUI Framer (NBF) para uma porta.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- ras RAS_PPP_NBFCP_RESULT estrutura de RAS_PPP_NBFCP_RESULT
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
ms.openlocfilehash: e415e6aea75dcf78d19d776e4df0a6edf704db473eacf0c8ddbb366ffbf65947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789590"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>Estrutura RAS \_ PPP \_ NBFCP \_ RESULT

\[A **estrutura RAS PPP \_ \_ NBFCP \_ RESULT** não tem suporte desde Windows Vista.\]

A **estrutura RAS PPP \_ \_ NBFCP \_ RESULT** é usada para relatar o resultado de uma operação de projeção de PPP NetBEUI Framer (NBF) para uma porta.

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

**Dwerror**
</dt> <dd>

Indica os resultados da operação de projeção NBF. Um valor de NO \_ ERROR indica êxito; nesse caso, o membro **wszWksta** contém o nome do computador remoto. Se a operação de projeção não tiver sido bem-sucedida, **dwError** será um código de erro de Winerror.h ou Raserror.h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Ignore esse membro no servidor; ele é relevante apenas no cliente.

</dd> <dt>

**Szname**
</dt> <dd>

Ignore esse membro no servidor; ele é relevante apenas no cliente.

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

 

 





