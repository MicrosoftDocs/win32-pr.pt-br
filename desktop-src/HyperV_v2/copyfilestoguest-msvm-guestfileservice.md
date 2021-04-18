---
description: Copia arquivos do host Hyper-V para a máquina virtual.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Método Msvm_GuestFileService:: CopyFilesToGuest'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783304"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>\_Método Msvm GuestFileService:: CopyFilesToGuest

Copia arquivos do host Hyper-V para a máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CopyFileToGuestSettings* \[ no\]
</dt> <dd>

Uma matriz de instâncias da classe [**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) que representa um trabalho de operação de serviço de arquivo convidado.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona. Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.

> [!Note]  
> Esse parâmetro foi adicionado no Windows 10.

 

</dd> <dt>

*ParentPools* \[ out, opcional\]
</dt> <dd>

Uma matriz opcional de referências do [**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) que são usadas para monitorar o progresso da operação. **CopyFilesToGuest** usará *ParentPools* se não puder ser executado de forma síncrona. Se a operação for executada de forma assíncrona, o valor de retorno será 4096.

> [!Note]  
> Esse parâmetro foi removido no Windows 10.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Em caso de sucesso, retorna 0; caso contrário, retorna um valor de erro.

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
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ GuestFileService**](msvm-guestfileservice.md)
</dt> </dl>

 

 




