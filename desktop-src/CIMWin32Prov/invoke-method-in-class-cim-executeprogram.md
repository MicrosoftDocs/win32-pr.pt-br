---
description: O método Invoke da classe CIM \_ ExecuteProgram executa uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da \_ ação CIM.
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bdf9a4edb78bb47c0354991d161339099e4dc49f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370408"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a>Método Invoke da classe CIM \_ ExecuteProgram

O método **Invoke** da classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) executa uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado [**da \_ ação CIM**](cim-action.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

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

[\_EXECUTEPROGRAM CIM](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[**\_EXECUTEPROGRAM CIM**](cim-executeprogram.md)
</dt> </dl>

 

