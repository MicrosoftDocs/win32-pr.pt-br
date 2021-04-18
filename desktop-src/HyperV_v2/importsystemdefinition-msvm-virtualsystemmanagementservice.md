---
description: Cria um novo sistema de computador planejado com base na definição de máquina virtual especificada.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Método ImportSystemDefinition da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759411"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ImportSystemDefinition da \_ classe VirtualSystemManagementService Msvm

Cria um novo sistema de computador planejado com base na definição de máquina virtual especificada.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SystemDefinitionFile* \[ no\]
</dt> <dd>

O caminho totalmente qualificado para o arquivo de definição do sistema (. xml ou. exp) que representa a máquina virtual que deve ser importada. O arquivo de definição ainda não deve estar em uso pelo sistema host ou pela plataforma de virtualização.

</dd> <dt>

*SnapshotFolder* \[ no\]
</dt> <dd>

O caminho totalmente qualificado para a pasta em que as configurações de instantâneo para esta máquina virtual podem ser encontradas. Essa pasta será pesquisada para localizar todos os instantâneos referenciados pela definição da máquina virtual. Todos os instantâneos referenciados não encontrados nesse local devem ser excluídos usando o método [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) ou importados usando o método [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) antes de concretizar o sistema de computador planejado.

</dd> <dt>

*GenerateNewSystemIdentifier* \[ no\]
</dt> <dd>

Indica se o identificador exclusivo deve ser reutilizado para a máquina virtual. Se esse parâmetro for **true**, um novo identificador do sistema será gerado. Se esse parâmetro for **false**, o identificador do sistema existente será usado.

</dd> <dt>

*ImportedSystem* \[ fora\]
</dt> <dd>

Se a operação for concluída de forma síncrona, uma referência a um objeto [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa a máquina virtual importada.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> <dt>

**Arquivo em uso** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

