---
description: Exporta uma máquina virtual, ou um instantâneo de uma máquina virtual, para um arquivo.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Método ExportSystemDefinition da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646684"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ExportSystemDefinition da \_ classe VirtualSystemManagementService Msvm

Exporta uma máquina virtual, ou um instantâneo de uma máquina virtual, para um arquivo. A máquina virtual deve estar no estado "desligado" ou "salvo" para ser exportada. A máquina virtual, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a um [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual a ser exportada.

</dd> <dt>

*ExportDirectory* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do diretório no qual a máquina virtual deve ser exportada. Se a propriedade **CreateVmExportSubdirectory** da classe [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) no parâmetro *ExportSettingData* for definida como **true**, esse diretório poderá ser reutilizado para exportar várias máquinas virtuais e esse método colocará cada definição de máquina virtual em um subdiretório separado sob esse caminho.

</dd> <dt>

*ExportSettingData* \[ no\]
</dt> <dd>

Uma instância inserida da classe [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) que representa as configurações da operação de exportação.

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

 

