---
title: RAS_SERVER_0 estrutura (Rassapi.h)
description: A estrutura RAS SERVER 0 é usada \_ pela função RasAdminServerGetInfo para retornar informações sobre as portas \_ configuradas em um servidor RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- ras RAS_SERVER_0 estrutura de RAS_SERVER_0
- PRAS_SERVER_0 RAS do ponteiro de estrutura
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
ms.openlocfilehash: dbb7a135fd6f8d1d77b59d1085460d51ad5357e47ca1a050e3d1ba6fd89461c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789380"
---
# <a name="ras_server_0-structure"></a>Estrutura RAS \_ SERVER \_ 0

\[A **estrutura RAS SERVER \_ \_ 0** não é suportada desde Windows Vista.\]

A **estrutura RAS SERVER \_ \_ 0** é usada pela [**função RasAdminServerGetInfo**](rasadminservergetinfo.md) para retornar informações sobre as portas configuradas em um servidor RAS.

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

Especifica o número total de portas configuradas no servidor RAS que estão disponíveis para os clientes remotos se conectarem. Por exemplo, se o número total de portas configuradas para discagem em um servidor for quatro, mas uma das portas estiver em uso no momento para discar, **TotalPorts** será três.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Especifica o número de portas atualmente em uso por clientes remotos.

</dd> <dt>

**RasVersion**
</dt> <dd>

Especifica a versão do servidor RAS. Use essas informações para tomar uma ação específica da versão. Esse membro é um dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Indica um servidor RAS versão 1.0 do LAN Manager.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Indica um Windows NT Server 3.51 e o cliente RAS anterior.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ CURRENT**</dt> </dl> | Indica um Windows NT ou cliente RAS 4.0.<br/>                     |



 

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

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





