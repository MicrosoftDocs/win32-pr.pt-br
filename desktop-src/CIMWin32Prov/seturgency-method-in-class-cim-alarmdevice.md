---
description: O método Set Pretendency define o nível de urgência desejado para um alarme.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Método Set Vouency da CIM_AlarmDevice classe
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
ms.openlocfilehash: 9557ad9e65b33e1ed8889ef1fd013b2d9f5426f8e819fe56608cb6846ea8669f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118172630"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>Método SetDelaency da classe CIM \_ AlarmDevice

O **método Set Pretendency** define o nível de urgência desejado para um alarme.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestedAreency* \[ Em\]
</dt> <dd>

Frequência relativa na qual o alarme pisca, vibra ou emite tons audíveis. Os valores a seguir são da **propriedade Urgência** em [**Alarme \_ CIMDevice**](cim-alarmdevice.md).

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

Sem suporte.

</dd> <dt>

3
</dt> <dd>

Informativo.

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

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito, 1 (um) se não há suporte para o nível de urgência solicitado e qualquer outro número para indicar um erro.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[CIM \_ AlarmDevice](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> </dl>

 

