---
description: Localiza um \_ objeto Msvm MountedStorageImage para um determinado caminho de imagem de disco.
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
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501916"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Método FindMountedStorageImageInstance da \_ classe imagens Msvm

Localiza um objeto [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) para um determinado caminho de imagem de disco.

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

*SelectionCriterion* \[ no\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local de um arquivo de imagem de disco.

</dd> <dt>

*Critériotype* \[ no\]
</dt> <dd>

O tipo de critério a ser pesquisado ao localizar a imagem do disco.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Caminho** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Imagem* \[ do fora\]
</dt> <dd>

Uma referência ao [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) (pode ser NULL se a imagem não estiver montada).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
</dt> <dt>

**Objeto não encontrado** (32789)
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

 

 




