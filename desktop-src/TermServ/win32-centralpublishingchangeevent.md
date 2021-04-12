---
title: Classe Win32_CentralPublishingChangeEvent
description: Um evento que representa uma alteração nas configurações do RDV central.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Classe de Win32_CentralPublishingChangeEvent Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_CentralPublishingChangeEvent classe, descrita
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455381"
---
# <a name="win32_centralpublishingchangeevent-class"></a>\_Classe Win32 CentralPublishingChangeEvent

Um evento que representa uma alteração nas configurações do RDV central.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ CentralPublishingChangeEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ CentralPublishingChangeEvent** tem essas propriedades.

<dl> <dt>

**OperationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de operação correspondente ao evento.

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**Criar** (0)


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

**Modificar** (1)


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

**Excluir** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event). Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Objeto alterado pela operação correspondente ao evento.

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da cimv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

