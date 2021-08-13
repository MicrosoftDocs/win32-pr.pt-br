---
description: O método SetPowerState da classe CIM HeatPipe define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser \_ colocado nesse estado.
ms.assetid: 10932c75-1fbe-422e-9333-d805ad695147
ms.tgt_platform: multiple
title: Método SetPowerState da CIM_HeatPipe classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HeatPipe.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19b5a5a244c54485887cccd85c2fb242ebb742b2e77c8dd8d66adb6bb058decc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675692"
---
# <a name="setpowerstate-method-of-the-cim_heatpipe-class"></a>Método SetPowerState da classe \_ HeatPipe cim

O **método SetPowerState** da classe CIM HeatPipe define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser \_ colocado nesse estado. Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método . As cadeias de caracteres para as quais o conteúdo **valueMap** são convertidos também devem ser especificadas na subclasse como um qualificador de matriz **Valores.** Esse método é herdado [**de CIM \_ LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PowerState* \[ Em\]
</dt> <dd>

Um **valor ValueMap** que especifica o estado de energia desejado para o dispositivo lógico.

<dt>

1
</dt> <dd>

Energia total.

</dd> <dt>

2
</dt> <dd>

Economia de energia no modo de baixa energia.

</dd> <dt>

3
</dt> <dd>

Economia de energia em espera.

</dd> <dt>

4
</dt> <dd>

Power save other.

</dd> <dt>

5
</dt> <dd>

Ciclo de energia.

</dd> <dt>

6
</dt> <dd>

Desligar.

</dd> </dl> </dd> <dt>

*Hora* \[ Em\]
</dt> <dd>

Especifica quando o estado de energia deve ser definido, como um valor de data/hora regular ou como um valor de intervalo (em que o intervalo começa quando a invocação do método é recebida). Quando o *parâmetro PowerState* é igual a 5 ("Power Cycle"), o parâmetro *Time* indica quando o dispositivo deve ser conectado novamente. A desligar é imediata.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 0 (zero) se for bem-sucedido, 1  (um) se a solicitação *PowerState* e Hora especificadas não tiver suporte e outro valor se qualquer outro erro ocorrer.

## <a name="remarks"></a>Comentários

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[CIM \_ HeatPipe](setpowerstate-method-in-class-cim-heatpipe.md)
</dt> <dt>

[**CIM \_ HeatPipe**](cim-heatpipe.md)
</dt> </dl>

 

 




