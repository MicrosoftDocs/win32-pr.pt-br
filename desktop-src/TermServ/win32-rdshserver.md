---
title: Win32_RDSHServer classe
description: Gerencia um servidor Host da Sessão da Área de Trabalho Remota (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer classe Serviços de Área de Trabalho Remota
- Win32_RDSHServer classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066cea4044330ab79122e9346f6f32999202f854245e5508448e40aea3521fe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422596"
---
# <a name="win32_rdshserver-class"></a>Classe Win32 \_ RDSHServer

Gerencia um servidor Host da Sessão da Área de Trabalho Remota (RDSH).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ RDSHServer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ RDSHServer** tem esses métodos.



| Método                                                                          | Descrição                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Recupera um valor da propriedade integer de um **objeto \_ Win32 RDSHServer.**<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | Recupera uma lista de servidores aguardando para iniciar.<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | Recupera um valor de propriedade de cadeia de caracteres de um **\_ objeto Win32 RDSHServer.**<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Atualiza um valor da propriedade integer de um **objeto \_ Win32 RDSHServer.**<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | Atualiza um valor de propriedade de cadeia de caracteres de um **\_ objeto Win32 RDSHServer.**<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | Compara o estado atual com o comparador especificado; se os dois corresponderem, o estado será definido como um novo valor. Independentemente da combinação, o estado atual também é retornado.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ RDSHServer** tem essas propriedades.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém e define o alias para a coleção RDSH à qual o servidor RDSH é atribuído.

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Obtém e define o nome do Conexão de Área de Trabalho Remota Broker (RDCB) que gerencia o acesso do usuário ao servidor RDSH.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém e define o nome do servidor RDSH.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Descreve o estado do servidor. Qualquer valor diferente de **TARGET \_ RUNNING** (3) é reservado e deve ser considerado um estado inválido.

Os valores possíveis são.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**DESTINO \_ UNKNOWN** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**DESTINO \_ EXECUTANDO** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**DESTINO \_ INVÁLIDO** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**DESTINO \_ STARTING** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**DESTINO \_ STOPPING** (10)


</dt> <dd></dd> </dl>

**Windows Server 2012 R2 e Windows Server 2012:** Essa propriedade não está disponível antes Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Raiz \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Área de Trabalho Remota de Serviços de Gerenciamento do Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

