---
description: O método seturgência define o nível de urgência desejado para um alarme.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Método seturgência da classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920365"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>Método seturgência da \_ classe AlarmDevice do CIM

O método **seturgência** define o nível de urgência desejado para um alarme.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestedUrgency* \[ no\]
</dt> <dd>

A frequência relativa na qual o alarme pisca, vibra ou emite tons audíveis. Os valores a seguir são da propriedade **urgência** no [**CIM \_ AlarmDevice**](cim-alarmdevice.md).

<dt>

0
</dt> <dd>

Desconhecido.

</dd> <dt>

1
</dt> <dd>

Outros.

</dd> <dt>

2
</dt> <dd>

Não há suporte.

</dd> <dt>

3
</dt> <dd>

Informativa.

</dd> <dt>

4
</dt> <dd>

Não crítico.

</dd> <dt>

5
</dt> <dd>

Crítica.

</dd> <dt>

6
</dt> <dd>

Irrecuperável.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) em êxito, 1 (um) se o nível de urgência solicitado não for suportado e qualquer outro número para indicar um erro.

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

[\_ALARMDEVICE CIM](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> </dl>

 

