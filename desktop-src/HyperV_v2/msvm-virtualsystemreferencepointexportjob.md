---
description: Essa classe representa um trabalho de operação de exportação do ponto de referência do sistema virtual.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506327"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a>\_Classe Msvm VirtualSystemReferencePointExportJob

Essa classe representa um trabalho de operação de exportação do ponto de referência do sistema virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemReferencePointExportJob** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Msvm \_ VirtualSystemReferencePointExportJob** tem esses métodos.



| Método                                                                                     | Descrição                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetError**](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | Recupera o erro.<br/>                    |
| [**GetErrorEx**](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | Recupera informações de erro adicionais.<br/> |
| [**RequestStateChange**](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | Solicita uma alteração de estado.<br/>                |



 

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemReferencePointExportJob** tem essas propriedades.

<dl> <dt>

**BaseReferencePointId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

GUID do ponto de referência que é usado como base na operação de exportação.

</dd> <dt>

**Cancelável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o trabalho pode ser cancelado. O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")
</dt> </dl>

Contém uma descrição resumida de erro.

</dd> <dt>

**ExportDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O local de exportação.

</dd> <dt>

**ExportedConfigFilePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do arquivo de configuração exportado.

</dd> <dt>

**ExportedDisks**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

IDs de instância de discos virtuais para os quais os arquivos de log foram exportados.

</dd> <dt>

**ExportedGuestStateFilePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do arquivo de estado de convidado exportado.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**ExportedLogFilePaths**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminhos dos arquivos de log que foram exportados.

</dd> <dt>

**ExportedRuntimeFilePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do arquivo de estado de tempo de execução exportado.

</dd> <dt>

**ReferencePointId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

GUID do ponto de referência que é exportado.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

GUID da máquina virtual para a qual os arquivos de log foram exportados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

