---
description: Representa um trabalho de operação do serviço de arquivo convidado.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Msvm_CopyFileToGuestJob classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 33fe43612425c96a5374603e6bb3a3cb6a3a56083113cc7628075ccf75c71056
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531735"
---
# <a name="msvm_copyfiletoguestjob-class"></a>Classe Msvm \_ CopyFileToGuestJob

Representa um trabalho de operação do serviço de arquivo convidado. Essa classe deriva de [**Msvm \_ GuestFileService.**](msvm-guestfileservice.md)

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ CopyFileToGuestJob** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Msvm \_ CopyFileToGuestJob** tem esses métodos.



| Método                                                                   | Descrição                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CopyFilesToGuest**](copyfilestoguest-msvm-guestfileservice.md)       | Copia arquivos do host Hyper-V para a máquina virtual.<br/> |
| [**Geterror**](geterror-msvm-copyfiletoguestjob.md)                     | Recupera o objeto de erro para o trabalho.<br/>                    |
| [**GetErrorEx**](geterrorex-msvm-copyfiletoguestjob.md)                 | Recupera os objetos de erro para o trabalho.<br/>                   |
| [**RequestStateChange**](requeststatechange-msvm-copyfiletoguestjob.md) | Altera o estado do trabalho.<br/>                              |
| **Startservice**                                                         | Não há suporte para o método.<br/>                              |
| **StopService**                                                          | Não há suporte para o método.<br/>                              |



 

### <a name="properties"></a>Propriedades

A **classe Msvm \_ CopyFileToGuestJob** tem essas propriedades.

<dl> <dt>

**Cancelável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o trabalho pode ser cancelado. O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja bem-sucedida. Se **TRUE**, o trabalho poderá ser cancelado; caso contrário, **FALSE.**

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual curta do objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CopyFileToGuestSettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Definir dados usados para copiar um arquivo.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usada com outras propriedades de chave da classe , essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Trabalho CIM \_**](cim-job.md).**ErrorCode**")
</dt> </dl>

Uma descrição resumida do erro, se presente. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador exclusivo para o serviço que também fornece uma indicação da funcionalidade gerenciada. Para obter mais informações sobre a funcionalidade, consulte a propriedade **Description do** objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, o serviço foi iniciado.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.

Os valores incluem o seguinte:

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**"Automático"**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**"Manual"**
</dt> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Status atual do objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

Os valores incluem o seguinte:

<dl><span id="OK"></span><span id="ok"></span><dt>

**"OK"**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**"Erro"**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**"Degradado"**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**"Desconhecido"**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Pred Fail"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**"Iniciando"**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**"Parando"**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**"Serviço"**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**"Stressed"**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"NonRecover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Sem contato"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Perda de comunicação"**
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da classe de criação do sistema de escopo.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do sistema que hospeda o serviço.

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

GUID do sistema virtual afetado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> <dt>

[**Msvm \_ GuestFileService**](msvm-guestfileservice.md)
</dt> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

