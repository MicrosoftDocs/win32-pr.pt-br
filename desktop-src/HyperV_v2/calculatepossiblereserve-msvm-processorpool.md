---
description: Esse método é usado para encontrar a reserva real com o parâmetro de entrada sendo o número de processadores de máquina virtual para os quais a reserva é calculada.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Método CalculatePossibleReserve da classe Msvm_ProcessorPool dados
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
ms.openlocfilehash: 06cfa01dd89392c05f460462d8bda5898b47d90b6e027fa885bf039f62488cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042066"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Método CalculatePossibleReserve da classe Msvm \_ ProcessorPool

Esse método é usado para encontrar a reserva real com o parâmetro de entrada sendo o número de processadores de máquina virtual para os quais a reserva é calculada. Esse método é necessário porque a reserva de recursos do processador é altamente dependente do número de processadores que devem ser agendados em paralelo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProcessorCount* \[ Em\]
</dt> <dd>

Tipo: **uint16**

O número de processadores de máquina virtual para os quais a reserva é calculada. O valor máximo para essa propriedade é a contagem de processador lógico para o computador host.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

A quantidade de recursos de CPU que podem ser reservados para uma máquina virtual.

## <a name="remarks"></a>Comentários

O acesso à [**classe Msvm \_ ProcessorPool**](msvm-processorpool.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

