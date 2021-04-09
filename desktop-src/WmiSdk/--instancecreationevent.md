---
description: Relata um evento de criação de instância, que é um tipo de evento intrínseco que é gerado quando uma nova instância é adicionada ao namespace.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: Classe __InstanceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171463"
---
# <a name="__instancecreationevent-class"></a>\_\_Classe InstanceCreationEvent

A classe de sistema **\_ \_ InstanceCreationEvent** relata um evento de criação de instância, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que é gerado quando uma nova instância é adicionada ao namespace.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ InstanceCreationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ InstanceCreationEvent** tem essas propriedades.

<dl> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cópia da instância que foi criada. Essa propriedade é herdada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ InstanceCreationEvent** é derivada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Criação de um recurso: \_ \_ InstanceCreationEvent**

Suponha que você esteja interessado em receber uma notificação se o bloco de notas for executado em um determinado computador. Quando o bloco de notas é executado, um processo correspondente é criado. Os processos podem ser gerenciados usando o WMI e são representados pela classe de processo do Win32 \_ . Quando o bloco de notas começa a ser executado, uma instância correspondente da \_ classe de processo Win32 fica disponível por meio do WMI. Se você registrou seu interesse nesse evento (emitindo a consulta de notificação de evento apropriada), a disponibilidade dessa instância resultará na criação de uma instância da classe **\_ \_ InstanceCreationEvent** .

As consultas de notificação que solicitam a notificação da criação de um recurso e usam eventos intrínsecos usam uma sintaxe semelhante à seguinte:

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

Para obter uma discussão maior sobre como usar o **\_ \_ InstanceCreationEvent** como uma maneira de monitorar sistemas de arquivos, consulte [WMI e monitoramento do sistema de arquivos](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) no CodeProject.

## <a name="examples"></a>Exemplos

O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **\_ \_ InstanceCreationEvent** como parte de um script complexo para configurar um registro de evento do WMI permanente.

O exemplo do PowerShell de [eventos permanentes do WMI](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) do PowerShell na galeria do TechNet usa **\_ \_ InstanceCreationEvent** como parte de um script de demonstração para configurar um registro de evento permanente.

O exemplo de teste de [evento de criação de processo](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) do VBScript no TechNet usa **\_ \_ InstanceCreationEvent** para monitorar o primeiro evento de criação de instância do WMI para o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

