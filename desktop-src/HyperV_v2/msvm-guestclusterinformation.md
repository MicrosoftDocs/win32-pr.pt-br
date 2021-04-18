---
description: Usado no método QueryGuestClusterInformation na \_ classe VssService Msvm para recuperar informações sobre o cluster de convidado do qual a VM faz parte.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Classe Msvm_GuestClusterInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770217"
---
# <a name="msvm_guestclusterinformation-class"></a>\_Classe Msvm GuestClusterInformation

Usado no método [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) na classe [**\_ VssService Msvm**](msvm-vssservice.md) para recuperar informações sobre o cluster de convidado do qual a VM faz parte.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ GuestClusterInformation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ GuestClusterInformation** tem essas propriedades.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O identificador do cluster de failover do qual o sistema operacional convidado da VM faz parte.

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de nós no cluster do qual o sistema operacional convidado da VM faz parte.

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o recurso de disco correspondente no cluster de convidado é compartilhado entre VMs no modo ativo/ativo.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o disco correspondente é um recurso de cluster no cluster de convidado.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o recurso de disco correspondente no cluster de convidado está online.

</dd> <dt>

**Isdele**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o recurso de disco correspondente no cluster de convidado é currenly pertencente a essa VM.

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A contagem de tiques de relógio quando um dos recursos de disco compartilhado foi movido pela última vez.

> [!Note]  
> Essa propriedade foi adicionada no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de caminhos de disco rígido virtual compartilhados conectados à VM.

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de dados de configuração de alocação de recursos (RASD) que representa os discos rígidos virtuais compartilhados conectados à VM.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

