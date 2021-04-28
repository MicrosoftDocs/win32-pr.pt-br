---
description: Método GetError da classe Msvm_StorageJob – recupera o erro.
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Método GetError da classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 00434ef529b7f26755f52833ff6f37310c7dc210
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109594"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a>Método GetError da \_ classe Msvm StorageJob

Recupera o erro.

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

O erro recuperado.

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
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Msvm \_ StorageJob**](msvm-storagejob.md)
</dt> </dl>

 

 




