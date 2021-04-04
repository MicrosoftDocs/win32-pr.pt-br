---
description: Esse método é usado para localizar a reserva real com o parâmetro de entrada sendo o número de processadores de máquina virtual para os quais a reserva é calculada.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Método CalculatePossibleReserve da classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662196"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Método CalculatePossibleReserve da \_ classe ProcessorPool Msvm

Esse método é usado para localizar a reserva real com o parâmetro de entrada sendo o número de processadores de máquina virtual para os quais a reserva é calculada. Esse método é necessário porque a reserva de recursos do processador é altamente dependente do número de processadores que devem ser agendados em paralelo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProcessorCount* \[ no\]
</dt> <dd>

Tipo: **UInt16**

O número de processadores de máquina virtual para os quais a reserva é calculada. O valor máximo dessa propriedade é a contagem de processadores lógicos para o computador host.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

A quantidade de recursos de CPU que podem ser reservados para uma máquina virtual.

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ ProcessorPool**](msvm-processorpool.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

