---
description: Exclui uma entrada de instantâneo vhd dentro de um arquivo de conjunto de VHDs.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Método DeleteVHDSnapshot da classe Msvm_ImageManagementService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 45a15b03b3ca26375ef0a563981cb9405c4397f355735c173e105029959d8282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522656"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a>Método DeleteVHDSnapshot da classe Msvm \_ ImageManagementService

Exclui uma entrada de instantâneo vhd dentro de um arquivo de conjunto de VHDs.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VHDSetPath* \[ Em\]
</dt> <dd>

Cadeia de caracteres que contém o caminho para o arquivo conjunto de VHD que contém o instantâneo em questão.

</dd> <dt>

*SnapshotId* \[ Em\]
</dt> <dd>

Um GUID que representa a ID do instantâneo para a entrada de instantâneo vhd a ser excluída.

</dd> <dt>

*PersistReferenceSnapshot* \[ Em\]
</dt> <dd>

Se um registro de instantâneo somente referência deve ser persistido após a exclusão do instantâneo.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Uma referência ao trabalho (pode ser nula se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

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

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




