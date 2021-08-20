---
description: 'Método Msvm_CopyFileToGuestJob:: GetError – recupera o objeto de erro para o trabalho, se existir um.'
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Método Msvm_CopyFileToGuestJob:: GetError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c5ef377dfd655c21137bbb0c7d34dfcb047054652afe162d75f2400acee045ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149794"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a>\_Método Msvm CopyFileToGuestJob:: GetError

Recupera o objeto de erro para o trabalho, se houver um. Quando o trabalho está em execução ou termina sem erro, esse método não retorna um objeto [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)) . No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma instância de **\_ erro CIM** é retornada.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erro* \[ do fora\]
</dt> <dd>

Se o status operacional do trabalho não for 2 (OK), esse método retornará uma instância inserida da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML. Se o status operacional do trabalho for 2 (OK), **NULL** será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

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
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

