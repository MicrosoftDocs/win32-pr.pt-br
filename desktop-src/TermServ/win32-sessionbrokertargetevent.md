---
title: Win32_SessionBrokerTargetEvent classe
description: Representa uma alteração em um destino do agente de sessão.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent classe Serviços de Área de Trabalho Remota
- Win32_SessionBrokerTargetEvent classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92fcd6cb93e3ac7abaa5fef33e1557008eb29b46940fae6d5165809d9252fa16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769966"
---
# <a name="win32_sessionbrokertargetevent-class"></a>Classe \_ SessionBrokerTargetEvent do Win32

Representa uma alteração em um destino do agente de sessão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Membros

A **classe \_ SessionBrokerTargetEvent do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SessionBrokerTargetEvent do Win32** tem essas propriedades.

<dl> <dt>

**Changetype**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a alteração que ocorreu. Esse pode ser um dos valores a seguir.

<dt>

1 (0x1)
</dt> <dd>

O tipo de alteração não é especificado.

</dd> <dt>

2 (0x2)
</dt> <dd>

O endereço IP externo foi alterado.

</dd> <dt>

4 (0x4)
</dt> <dd>

O endereço IP interno foi alterado.

</dd> <dt>

8 (0x8)
</dt> <dd>

O destino foi unido.

</dd> <dt>

16 (0x10)
</dt> <dd>

O destino foi removido.

</dd> <dt>

32 (0x20)
</dt> <dd>

O estado do destino foi alterado.

</dd> <dt>

64 (0x40)
</dt> <dd>

O destino está ocioso.

</dd> </dl>

</dd> <dt>

**Ambiente**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do ambiente. No caso de um destino de VM (máquina virtual), esse pode ser o nome do host da VM.

**Windows Server 2008 R2:** Essa propriedade não está disponível antes Windows Server 2012

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do farm ao que o destino pertence.

**Windows Server 2008 R2:** Essa propriedade não está disponível antes Windows Server 2012

</dd> <dt>

**Guid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O GUID do destino.

**Windows Server 2008 R2:** Essa propriedade não está disponível antes Windows Server 2012

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do plug-in.

**Windows Server 2008 R2:** Essa propriedade não está disponível antes Windows Server 2012

</dd> <dt>

**DESCRITOR \_ DE SEGURANÇA**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Essa propriedade é herdada do [**\_ \_ Evento**](/windows/desktop/WmiSdk/--event). Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [Constantes de segurança WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**Targetname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do destino.

**Windows Server 2008 R2:** Essa propriedade não está disponível antes Windows Server 2012

</dd> <dt>

**TEMPO \_ CRIADO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Esse é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (Tempos Universais Coordenados). Essa propriedade é herdada do [**\_ \_ Evento**](/windows/desktop/WmiSdk/--event).

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

