---
description: Atualiza o nome do elemento para o objeto \_ CollectionOfMSEs cim especificado.
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Método RenameCollection da classe Msvm_CollectionManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4ddcb83c7f148ee8a3f7a25d050f3924bfd4b665c471fac1dbfd095c70e46be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681926"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a>Método RenameCollection da classe Msvm \_ CollectionManagementService

Atualiza o nome do elemento para o objeto [**\_ CollectionOfMSEs cim**](cim-collectionofmses.md) especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Coleção* \[ Em\]
</dt> <dd>

A coleção a ser renomeda.

</dd> <dt>

*NewName* \[ Em\]
</dt> <dd>

O novo nome a ser usado.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Uma referência ao trabalho (pode ser nula se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 0 se for bem-sucedido ou 4096 se o trabalho for iniciado; caso contrário, retornará um erro.

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

[**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




