---
description: Define os dados de configuração da máquina inicial de VMs.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Método SetInitialMachineConfigurationData da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646819"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método SetInitialMachineConfigurationData da \_ classe VirtualSystemManagementService Msvm

Define os dados de configuração inicial da máquina VM.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TargetSystem* \[ no\]
</dt> <dd>

Uma referência ao sistema de computador virtual no qual os dados do IMC serão definidos.

</dd> <dt>

*Imcdata* \[ no\]
</dt> <dd>

Os dados do IMC a serem definidos. Os primeiros quatro bytes devem ser o comprimento da matriz na ordem big-endian

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona. Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




