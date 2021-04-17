---
description: Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma \_ instância de erro Msvm.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Método GetErrorEx da classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769345"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a>Método GetErrorEx da \_ classe StorageJob Msvm

Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) . No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de **\_ erro Msvm** são retornadas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erros* \[ do fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Se o status operacional do trabalho não for "OK", esse método retornará uma matriz de instâncias [**de \_ erro Msvm**](msvm-error.md) . Caso contrário, se o trabalho for "OK", será retornado **nulo** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

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

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ StorageJob**](msvm-storagejob.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ StorageJob**](msvm-storagejob.md)
</dt> </dl>

 

