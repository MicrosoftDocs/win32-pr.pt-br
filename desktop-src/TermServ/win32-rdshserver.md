---
title: Classe Win32_RDSHServer
description: Gerencia um servidor de Host da Sessão da Área de Trabalho Remota (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDSHServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDSHServer classe, descrita
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
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295792"
---
# <a name="win32_rdshserver-class"></a>\_Classe Win32 RDSHServer

Gerencia um servidor de Host da Sessão da Área de Trabalho Remota (RDSH).

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

A classe **Win32 \_ RDSHServer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDSHServer** tem esses métodos.



| Método                                                                          | Descrição                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getint32property**](getint32property-win32-rdshserver.md)                   | Recupera um valor da propriedade Integer de um objeto **\_ RDSHServer do Win32** .<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | Recupera uma lista de servidores que estão aguardando para serem iniciados.<br/>                                                                                                                           |
| [**Getstringproperty**](getstringproperty-win32-rdshserver.md)                 | Recupera um valor de propriedade da cadeia de caracteres de um objeto **\_ RDSHServer do Win32** .<br/>                                                                                                   |
| [**Setint32property**](setint32property-win32-rdshserver.md)                   | Atualiza um valor da propriedade Integer de um objeto **\_ RDSHServer do Win32** .<br/>                                                                                                   |
| [**Setstringproperty**](setstringproperty-win32-rdshserver.md)                 | Atualiza um valor de propriedade de cadeia de caracteres de um objeto **Win32 \_ RDSHServer** .<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | Compara o estado atual com o termo especificado; Se as duas corresponderem, o estado será definido como um novo valor. Independentemente da correspondência, o estado atual também é retornado.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ RDSHServer** tem essas propriedades.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém e define o alias para a coleção de RDSH à qual o servidor de RDSH está atribuído.

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define o nome do RDCB (agente de Conexão de Área de Trabalho Remota) que gerencia o acesso do usuário ao servidor de RDSH.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém e define o nome do servidor de RDSH.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Descreve o estado do servidor. Qualquer valor diferente de **destino \_ em execução** (3) é reservado e deve considerar um estado inválido.

Os valores possíveis são.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**Destino \_ DESCONHECIDO** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**Destino \_ EM execução** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**Destino \_ INVÁLIDO** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**Destino \_ A partir** de (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**Destino \_ PARAndo** (10)


</dt> <dd></dd> </dl>

**Windows server 2012 R2 e Windows server 2012:** Essa propriedade não está disponível antes do Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

