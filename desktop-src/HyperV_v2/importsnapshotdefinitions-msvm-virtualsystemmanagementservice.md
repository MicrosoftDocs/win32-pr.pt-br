---
description: Pesquisa na pasta especificada os arquivos de definição de instantâneo associados ao sistema de computador planejado especificado e cria um novo instantâneo no sistema de computador planejado para cada arquivo de definição associado nesse local.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Método ImportSnapshotDefinitions da classe Msvm_VirtualSystemManagementService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cfa20eb845546f58201bdc167cfbe38bd4a3bd0ad327a04e009db4504ce0966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694586"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ImportSnapshotDefinitions da classe Msvm \_ VirtualSystemManagementService

Pesquisa na pasta especificada os arquivos de definição de instantâneo associados ao sistema de computador planejado especificado e cria um novo instantâneo no sistema de computador planejado para cada arquivo de definição associado nesse local.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PlannedSystem* \[ Em\]
</dt> <dd>

Uma referência a [**um objeto Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa a máquina virtual planejada que referencia os instantâneos a serem importados.

</dd> <dt>

*SnapshotFolder* \[ Em\]
</dt> <dd>

O caminho totalmente qualificado para a pasta em que as configurações de instantâneo para essa máquina virtual podem ser encontradas.

</dd> <dt>

*ImportedSnapshots* \[ out\]
</dt> <dd>

Se a operação for concluída de forma síncrona, uma matriz de referências às instâncias [**do Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representam os instantâneos que foram importados com êxito.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

**O status é desconhecido** (32771)
</dt> <dt>

**Tempoout** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

**O sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

**O sistema não está disponível** (32777)
</dt> <dt>

**Memória sem memória** (32778)
</dt> <dt>

**Arquivo em uso** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

