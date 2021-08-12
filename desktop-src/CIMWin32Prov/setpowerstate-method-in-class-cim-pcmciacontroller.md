---
description: O método SetPowerState da classe CIM PCMCIAController define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser \_ colocado nesse estado.
ms.assetid: 30e6936d-f621-4dd1-b25c-8d959ea97cc8
ms.tgt_platform: multiple
title: Método SetPowerState da classe CIM_PCMCIAController classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20547a654f0f010cae315b27c921590e6e504575f33b67bf71972ea08a6e233f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675592"
---
# <a name="setpowerstate-method-of-the-cim_pcmciacontroller-class"></a>Método SetPowerState da classe CIM \_ PCMCIAController

O **método SetPowerState** da classe CIM PCMCIAController define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser \_ colocado nesse estado. Em uma subclasse, o conjunto de códigos de retorno possíveis deve ser especificado usando um qualificador **ValueMap** no método . As cadeias de caracteres para as quais o conteúdo **valueMap** são convertidos também devem ser especificadas na subclasse como um qualificador da matriz **Valores.** Esse método é herdado [**de CIM \_ LogicalDevice.**](cim-logicaldevice.md)

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

Um **valor valueMap** que especifica o estado de energia desejado para este dispositivo lógico.

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

Esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor. Para classes WMI derivadas de [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md), consulte [Classes Win32](win32-provider.md).

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

[CIM \_ PCMCIAController](setpowerstate-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> </dl>

 

 




