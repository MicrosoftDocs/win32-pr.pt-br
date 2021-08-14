---
description: O método SetPowerState define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: 3808b75d-229e-44c0-a1bc-aa260590cd36
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_AggregatePSExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a979ad1a61e907bcc1d14b402b72999590909001e5214dca83e5920dceeac1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439816"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepsextent-class"></a>Método SetPowerState da classe CIM \_ AggregatePSExtent

O método **SetPowerState** define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado. Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado, usando um qualificador **ValueMap** no método. As cadeias de caracteres nas quais o conteúdo de **ValueMap** são traduzidos também devem ser especificadas na subclasse como um qualificador de matriz de **valores** . Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).

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

O valor de **ValueMap** que especifica o estado de energia desejado para esse dispositivo lógico.

<dt>

1
</dt> <dd>

Potência total

</dd> <dt>

2
</dt> <dd>

Economia de energia – modo de baixa energia

</dd> <dt>

3
</dt> <dd>

Energia-salvar em espera

</dd> <dt>

4
</dt> <dd>

Salvar outra energia

</dd> <dt>

5
</dt> <dd>

Ciclo de energia

</dd> <dt>

6
</dt> <dd>

Desligar

</dd> </dl> </dd> <dt>

*Tempo* \[ no\]
</dt> <dd>

Quando o estado de energia deve ser definido, seja como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida). Quando o parâmetro *PowerState* é igual a 5, (ciclo de energia), o parâmetro *time* indica quando o dispositivo deve ligar novamente. A desligamento é imediata.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 0 (zero) se for bem-sucedido, 1 (um) se o *PowerState* e a solicitação de *tempo* especificados não forem suportados e outro valor se ocorrer algum outro erro.

## <a name="remarks"></a>Comentários

Este método não está implementado no momento pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_AGGREGATEPSEXTENT CIM](setpowerstate-method-in-class-cim-aggregatepsextent.md)
</dt> <dt>

[**\_AGGREGATEPSEXTENT CIM**](cim-aggregatepsextent.md)
</dt> </dl>

 

 




