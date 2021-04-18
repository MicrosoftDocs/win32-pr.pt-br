---
title: Estrutura de RAS_SERVER_0 (Rassapi. h)
description: A \_ estrutura do servidor RAS \_ 0 é usada pela função RasAdminServerGetInfo para retornar informações sobre as portas configuradas em um servidor RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS da estrutura de RAS_SERVER_0
- RAS de ponteiro de estrutura de PRAS_SERVER_0
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752833"
---
# <a name="ras_server_0-structure"></a>\_Estrutura do servidor RAS \_ 0

\[A estrutura do **\_ servidor RAS \_ 0** não tem suporte a partir do Windows Vista.\]

A estrutura do **\_ servidor RAS \_ 0** é usada pela função [**RasAdminServerGetInfo**](rasadminservergetinfo.md) para retornar informações sobre as portas configuradas em um servidor RAS.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a>Membros

<dl> <dt>

**TotalPorts**
</dt> <dd>

Especifica o número total de portas configuradas no servidor RAS que estão disponíveis para os clientes remotos se conectarem. Por exemplo, se o número total de portas configuradas para discagem em um servidor for de quatro, mas uma das portas estiver em uso no momento para discar, **TotalPorts** será três.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Especifica o número de portas atualmente em uso por clientes remotos.

</dd> <dt>

**RasVersion**
</dt> <dd>

Especifica a versão do servidor RAS. Use essas informações para executar a ação específica da versão. Esse membro é um dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Indica um servidor RAS da versão 1,0 do LAN Manager.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Indica um servidor ou cliente RAS do Windows NT Server 3,51 e anterior.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ atual**</dt> </dl> | Indica um cliente ou servidor RAS do Windows NT 4,0.<br/>                     |



 

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

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





