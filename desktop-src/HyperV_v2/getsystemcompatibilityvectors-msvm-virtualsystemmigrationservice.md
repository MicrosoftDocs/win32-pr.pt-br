---
description: Obtém uma lista de instâncias Msvm CompatibilityVector que podem ser usadas para verificar a \_ VM (máquina virtual) para hospedar a compatibilidade.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: Msvm_VirtualSystemMigrationService::GetSystemCompatibilityVectors
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
ms.openlocfilehash: 19eb9fe54c9a20e635d706eff9b22eb0e78cb8347b27fcdcaff0f419e60a6112
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427656"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>Método Msvm \_ VirtualSystemMigrationService::GetSystemCompatibilityVectors

Obtém uma lista [**de instâncias Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que podem ser usadas para verificar a VM (máquina virtual) para hospedar a compatibilidade.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

Uma referência a uma [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a VM para a que recuperar vetores de compatibilidade. Se esse parâmetro se referir ao sistema de computador de hospedagem, os dados retornados no parâmetro *CompatibilityVectors* poderão ser usados para determinar se qualquer uma das VMs no sistema de computador de hospedagem pode ser migrada rapidamente para outro sistema de computador de hospedagem.

</dd> <dt>

*CompatibilityVectors* \[ out\]
</dt> <dd>

Uma matriz de [**instâncias Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que contêm as informações de compatibilidade para as VMs ou o sistema de computador de hospedagem.

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
</dt> </dl>

## <a name="remarks"></a>Comentários

**GetSystemCompatibilityVectors** obtém informações de compatibilidade para uma VM (máquina virtual) (quando executado em um sistema de computadores VM) ou um host (quando executado em um sistema de computador host). As informações de compatibilidade permanecem opaca para o cliente, enquanto as informações fornece uma maneira de comparar as informações de compatibilidade do host com as da VM.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\\\Virtualização \\ raiz \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




