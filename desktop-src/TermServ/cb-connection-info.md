---
title: Estrutura de CB_CONNECTION_INFO (Cbclient. h)
description: Contém informações sobre uma solicitação de conexão de entrada.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- Estrutura de CB_CONNECTION_INFO Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PCB_CONNECTION_INFO Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd433f668c178973a4e3690ea130d01d75fab79e739610f77ac00619b9e326c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575036"
---
# <a name="cb_connection_info-structure"></a>Estrutura de informações de \_ conexão CB \_

Contém informações sobre uma solicitação de conexão de entrada. Essa estrutura é usada com o método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**UserName**
</dt> <dd>

O nome do usuário que está solicitando uma sessão.

</dd> <dt>

**Domínio**
</dt> <dd>

O nome do domínio do qual o **nome de usuário** é membro.

</dd> <dt>

**InitialProgram**
</dt> <dd>

O caminho totalmente qualificado e o nome de arquivo do programa inicial que é iniciado quando a sessão é iniciada. Defina esse membro como uma cadeia de caracteres vazia se nenhum programa inicial precisar ser iniciado.

</dd> <dt>

**Recurso**
</dt> <dd>

Um valor da enumeração [**do \_ \_ tipo de recurso CB**](cb-resource-type.md) que especifica o tipo de recurso ao qual a conexão de entrada está se conectando. Se o membro **pluginname** for **nulo**, esse membro será usado pelo agente de conexão de área de trabalho remota para determinar qual plug-in invocar para determinar o computador de destino.

</dd> <dt>

**PluginName**
</dt> <dd>

O nome do plug-in a ser invocado para determinar o computador de destino. Se esse parâmetro for **NULL**, o membro de **recurso** será usado para determinar qual plug-in invocar.

</dd> <dt>

**Farmname**
</dt> <dd>

O nome do farm que contém os computadores, um dos quais será o computador de destino em que a conexão será redirecionada.

</dd> <dt>

**dwVendorInfoLength**
</dt> <dd>

Este membro é reservado para uso futuro.

</dd> <dt>

**pVendorSpecificInfo**
</dt> <dd>

Este membro é reservado para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





