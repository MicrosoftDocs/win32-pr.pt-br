---
description: Recupera uma lista de alterações na região especificada de um disco virtual desde a ID de Controle de Alterações resiliente fornecida ou a ID de instantâneo VHDSet.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Método GetVirtualDiskChanges da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787105"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVirtualDiskChanges da \_ classe imagens Msvm

Recupera uma lista de alterações na região especificada de um disco virtual desde a ID de Controle de Alterações resiliente fornecida ou a ID de instantâneo VHDSet.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* \[ do no\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual.

</dd> <dt>

*Limitid* \[ no\]
</dt> <dd>

Uma ID de Controle de Alterações resiliente ou uma ID de instantâneo de conjunto de VHD que indica a linha de base para alterações no disco virtual.

</dd> <dt>

*TargetSnapshotId* \[ no\]
</dt> <dd>

Uma ID de instantâneo VHDSet que indica o instantâneo a ser comparado com a linha de base ao fazer o deprazo das alterações no disco rígido virtual. Este parâmetro só é válido para arquivos de conjunto VHD.

</dd> <dt>

*ByteOffset* \[ no\]
</dt> <dd>

O deslocamento de byte da região no disco virtual para consulta de alterações.

</dd> <dt>

*ByteLength* \[ no\]
</dt> <dd>

O comprimento de bytes da região no disco virtual para consulta de alterações. Isso deve ser menor que o tamanho do disco virtual.

</dd> <dt>

*ProcessedByteLength* \[ fora\]
</dt> <dd>

O comprimento total de bytes que foi processado. Isso pode ser igual a ByteLength ou menos.

</dd> <dt>

*ChangedByteOffsets* \[ fora\]
</dt> <dd>

A lista de deslocamentos de bytes no disco virtual que indica o início de cada intervalo alterado.

</dd> <dt>

*ChangedByteLengths* \[ fora\]
</dt> <dd>

A lista de comprimentos de bytes dos intervalos alterados no disco virtual.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos seguintes valores:

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

**Arquivo não encontrado** (32779)
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

[**Msvm \_ imagens**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




