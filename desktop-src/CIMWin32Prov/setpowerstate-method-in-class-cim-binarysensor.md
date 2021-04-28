---
description: Método SetPowerState da classe CIM_BinarySensor-o método SetPowerState define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.
ms.assetid: bf5bdc90-9735-47b8-87d5-8f2482e603ed
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_BinarySensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd18c9f5761cac208f8682bbc3c8f189cf0aefe0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089504"
---
# <a name="setpowerstate-method-of-the-cim_binarysensor-class"></a>Método SetPowerState da classe CIM \_ BinarySensor

O método **SetPowerState** define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.

Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método. As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** . Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PowerState* \[ no\]
</dt> <dd>

Um valor de **ValueMap** que especifica o estado de energia desejado para o dispositivo lógico.

<dt>

1
</dt> <dd>

Potência total.

</dd> <dt>

2
</dt> <dd>

Economia de energia no modo de baixa energia.

</dd> <dt>

3
</dt> <dd>

Power Save em espera.

</dd> <dt>

4
</dt> <dd>

Economia de energia diferente.

</dd> <dt>

5
</dt> <dd>

Ciclo de energia.

</dd> <dt>

6
</dt> <dd>

Desligar.

</dd> </dl> </dd> <dt>

*Tempo* \[ no\]
</dt> <dd>

Especifica quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida). Quando o parâmetro *PowerState* é igual a 5 ("ciclo de energia"), o parâmetro *time* indica quando o dispositivo deve ligar novamente. A desligamento é imediata.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.

## <a name="remarks"></a>Comentários

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[\_BINARYSENSOR CIM](setpowerstate-method-in-class-cim-binarysensor.md)
</dt> <dt>

[**\_BINARYSENSOR CIM**](cim-binarysensor.md)
</dt> </dl>

 

 




