---
description: O método Invoke da classe \_ REMOVEDirectoryAction cim toma uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da Ação \_ CIM.
ms.assetid: c6a7edcd-aac1-4364-8de5-a16fe2bab107
ms.tgt_platform: multiple
title: Invocar o método da classe CIM_RemoveDirectoryAction dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fab386bc41458ae4f4dd4593141af7671240a7f386c3fd9dfbb6c0d511071094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064866"
---
# <a name="invoke-method-of-the-cim_removedirectoryaction-class"></a>Invocar o método da classe \_ REMOVEDirectoryAction cim

O **método Invoke** da classe [**\_ REMOVEDirectoryAction cim**](cim-removedirectoryaction.md) toma uma ação específica. Os detalhes de como o método executa a ação são específicos da implementação. Esse método é herdado da [**Ação CIM. \_**](cim-action.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

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

[CIM \_ RemoveDirectoryAction](invoke-method-in-class-cim-removedirectoryaction.md)
</dt> <dt>

[**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md)
</dt> </dl>

 

