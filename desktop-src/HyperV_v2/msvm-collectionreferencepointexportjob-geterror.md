---
description: Recupera um erro.
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: Método GetError da classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011638"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Método GetError da \_ classe Msvm CollectionReferencePointExportJob

Recupera um erro.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erro* \[ do fora\]
</dt> <dd>

Em caso de sucesso, contém uma descrição do erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

0 em caso de êxito; caso contrário, um erro.

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
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




