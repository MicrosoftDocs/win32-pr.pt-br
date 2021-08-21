---
description: 'Método Msvm_CopyFileToGuestJob:: GetErrorEx – recupera os objetos de erro para o trabalho, caso existam.'
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: 'Método Msvm_CopyFileToGuestJob:: GetErrorEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69dd440df079379d8e4bd9cee6e1cad23e684cb80a11e7e48d39752ccea82426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149809"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a>\_Método Msvm CopyFileToGuestJob:: GetErrorEx

Recupera os objetos de erro para o trabalho, caso existam. Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) . No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de **\_ erro Msvm** são retornadas.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erros* \[ do fora\]
</dt> <dd>

Se o status operacional do trabalho não for 2 (OK), esse método retornará uma ou mais instâncias inseridas da classe [**de \_ erro Msvm**](msvm-error.md) , no formato CIM-XML, que representa os erros encontrados no trabalho. Se o status operacional do trabalho for 2 (OK), será retornado **NULL** .

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

 

 




