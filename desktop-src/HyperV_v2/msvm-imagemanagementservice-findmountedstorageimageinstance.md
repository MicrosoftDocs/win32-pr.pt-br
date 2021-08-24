---
description: Localiza um objeto Msvm \_ MountedStorageImage para um determinado caminho de imagem de disco.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Método FindMountedStorageImageInstance da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de205cb729b9ad53674808523cc640b9aaccb2adfaf6fba0b8a06c8a0d8952f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522626"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Método FindMountedStorageImageInstance da classe Msvm \_ ImageManagementService

Localiza um [**objeto Msvm \_ MountedStorageImage para**](msvm-mountedstorageimage.md) um determinado caminho de imagem de disco.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SelectionCriterion* \[ Em\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local de um arquivo de imagem de disco.

</dd> <dt>

*CriterionType* \[ Em\]
</dt> <dd>

O tipo de critério a ser buscado ao localizar a imagem de disco.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Caminho** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Imagem* \[ out\]
</dt> <dd>

Uma referência ao [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) (pode ser nulo se a imagem não estiver montada).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

<dl> <dt>

**Concluído sem erro** (0)
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
</dt> <dt>

**Objeto não encontrado** (32789)
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

 

 




