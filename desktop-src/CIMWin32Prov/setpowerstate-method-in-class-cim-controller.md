---
description: Método SetPowerState da classe CIM_Controller - O método SetPowerState define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.
ms.assetid: 442c6c2c-8e9a-476c-bb57-8b1a6439e97f
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_Controller classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b8956afb9547f949f68007e7e2da7d2dce4f9f46a2e45cb66ea838ad206ad45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439616"
---
# <a name="setpowerstate-method-of-the-cim_controller-class"></a>Método SetPowerState da classe controlador CIM \_

O **método SetPowerState** define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado. Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método . As cadeias de caracteres para as quais o conteúdo **valueMap** são convertidos também devem ser especificadas na subclasse como um qualificador de matriz **Valores.** Esse método é herdado [**de CIM \_ LogicalDevice.**](cim-logicaldevice.md)

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

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor. Para obter mais informações, consulte [Criando provedores WMI](/windows/desktop/WmiSdk/creating-wmi-providers).

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controlador \_ CIM](setpowerstate-method-in-class-cim-controller.md)
</dt> <dt>

[**Controlador \_ CIM**](cim-controller.md)
</dt> </dl>

 

