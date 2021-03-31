---
description: Permite que os limites sejam definidos no uso do processo de host de recursos do sistema.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: Classe __ProviderHostQuotaConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169811"
---
# <a name="__providerhostquotaconfiguration-class"></a>\_\_Classe ProviderHostQuotaConfiguration

A classe de sistema **\_ \_ ProviderHostQuotaConfiguration** é uma classe de configuração para processos de provedor de host. Essa classe reside no namespace raiz e permite que os limites sejam definidos no uso do processo de host dos recursos do sistema.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ProviderHostQuotaConfiguration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ProviderHostQuotaConfiguration** tem essas propriedades.

<dl> <dt>

**HandlesPerHost**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Número de identificadores de objeto de kernel que cada host pode ter.

</dd> <dt>

**MemoryAllHosts**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Quantidade combinada de memória privada em bytes que pode ser mantida por todos os hosts.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MemoryPerHost**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Quantidade de memória privada que pode ser mantida por cada host.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ProcessLimitAllHosts**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Número total de processos de host que podem ser executados simultaneamente.

</dd> <dt>

**ThreadsPerHost**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Número de threads pertencentes a um host.

</dd> </dl>

## <a name="remarks"></a>Comentários

As propriedades que representam os limites podem ser alteradas, mas como a classe é singleton, todos os hosts do provedor compartilham os mesmos limites.

Os parâmetros a seguir são usados ao configurar os limites de objeto de trabalho para o objeto de trabalho do host:

-   **MemoryAllHosts**
-   **MemoryPerHost**
-   **ProcessLimitAllHosts**
-   **ThreadsPerHost**

O processo de host pesquisa o uso do identificador e sai do processo se a cota de **HandlesPerHost** for violada. As alterações nesses valores entrarão em vigor depois que o computador for reiniciado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

