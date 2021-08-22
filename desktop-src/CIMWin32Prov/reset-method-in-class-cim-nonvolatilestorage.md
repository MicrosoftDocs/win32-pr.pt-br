---
description: O método Reset da classe CIM \_ NonVolatileStorage solicita uma redefinição do dispositivo lógico.
ms.assetid: 5fa02e46-4823-4ffa-b4e9-0930fed6fb03
ms.tgt_platform: multiple
title: Método reset da classe CIM_NonVolatileStorage dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e8cd378cbff7e8c723d0e9dc7a99cf4a10ffce8b541ec46a5b8232d6e43937e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418851"
---
# <a name="reset-method-of-the-cim_nonvolatilestorage-class"></a>Método reset da classe CIM \_ NonVolatileStorage

O **método Reset** da classe CIM \_ NonVolatileStorage solicita uma redefinição do dispositivo lógico. Esse método é herdado [**de CIM \_ LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (um) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.

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

[CIM \_ NonVolatileStorage](reset-method-in-class-cim-nonvolatilestorage.md)
</dt> <dt>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> </dl>

 

 




