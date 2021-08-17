---
description: O método Invoke da classe CIM \_ DiskSpaceCheck avalia uma verificação específica. Os detalhes de como o método avalia uma verificação específica em um contexto CIM são descritos pela \_ subclasse cim check não abstrata.
ms.assetid: 1f06b0c4-3f39-4a6f-9205-2aa309fb06bb
ms.tgt_platform: multiple
title: Método Invoke da classe CIM_DiskSpaceCheck dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbf8e976861c079fc79e70b3b9009b8948624e57e02870ad50c2630cd42aca7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118009892"
---
# <a name="invoke-method-of-the-cim_diskspacecheck-class"></a>Método Invoke da classe CIM \_ DiskSpaceCheck

O **método Invoke** da classe CIM [**\_ DiskSpaceCheck**](cim-diskspacecheck.md) avalia uma verificação específica. Os detalhes de como o método avalia uma verificação específica em um contexto CIM são descritos pela subclasse cim check não [**\_ abstrata.**](cim-check.md)

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

[CIM \_ DiskSpaceCheck](invoke-method-in-class-cim-diskspacecheck.md)
</dt> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> </dl>

 

