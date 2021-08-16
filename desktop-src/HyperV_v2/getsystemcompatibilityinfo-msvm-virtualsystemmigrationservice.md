---
description: Gera um blob opaco de dados que contém informações de compatibilidade para o sistema especificado.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Método GetSystemCompatibilityInfo da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4866b54bb6f5d5b90d4221b81e8a847e910e4486edc55eb4f932684397072504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392810"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método GetSystemCompatibilityInfo da \_ classe VirtualSystemMigrationService Msvm

Gera um blob opaco de dados que contém informações de compatibilidade para o sistema especificado. Esse método é usado em conjunto com o método [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) para determinar se uma migração rápida ou dinâmica de uma máquina virtual para outro sistema de computador host é possível sem realmente tentar a migração.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a uma classe de [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que representa a máquina virtual para a qual recuperar informações de compatibilidade. Se esse parâmetro se referir ao sistema de computador de hospedagem, os dados retornados no parâmetro *CompatibilityInfo* poderão ser usados para determinar se alguma das máquinas virtuais no sistema do computador de hospedagem pode ser migrada rapidamente para outro sistema de computador de hospedagem.

</dd> <dt>

*CompatibilityInfo* \[ fora\]
</dt> <dd>

Um blob de dados opaco que pode ser passado para o método [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) em outro sistema de computador host para confirmar a compatibilidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




