---
description: Obtém uma lista de instâncias do Msvm \_ CompatibilityVector que podem ser usadas para verificar a compatibilidade do host de máquinas virtuais (VM).
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Método Msvm_VirtualSystemMigrationService:: GetSystemCompatibilityVectors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920731"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>\_Método Msvm VirtualSystemMigrationService:: GetSystemCompatibilityVectors

Obtém uma lista de instâncias do [**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que podem ser usadas para verificar a compatibilidade do host de máquinas virtuais (VM).

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a uma classe de [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que representa a VM para a qual os vetores de compatibilidade são recuperados. Se esse parâmetro se referir ao sistema de computador de hospedagem, os dados retornados no parâmetro *CompatibilityVectors* poderão ser usados para determinar se alguma das VMs no sistema de computador de hospedagem pode ser migrada rapidamente para outro sistema de computador de hospedagem.

</dd> <dt>

*CompatibilityVectors* \[ fora\]
</dt> <dd>

Uma matriz de instâncias do [**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que contém as informações de compatibilidade para as VMs ou o sistema de computador de hospedagem.

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

## <a name="remarks"></a>Comentários

**GetSystemCompatibilityVectors** Obtém informações de compatibilidade para uma VM (máquina virtual) (quando executado em um sistema de computador VM) ou um host (quando executado em um sistema de computador host). As informações de compatibilidade permanecem opacas para o cliente, enquanto as informações fornecem uma maneira de comparar as informações de compatibilidade do host com aquela da VM.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




