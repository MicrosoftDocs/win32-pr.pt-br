---
description: Método Reset da classe CIM_DiskPartition – o método reset solicita uma redefinição do dispositivo lógico. Esse método é herdado do \_ LOGICALDEVICE CIM.
ms.assetid: 874f8eb4-784a-41ab-9c58-9e48486a7f71
ms.tgt_platform: multiple
title: Método Reset da classe CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 088230f2b09089fafaa1fbe4cb67684a873c97d14d612801383222d011e1ecfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119283736"
---
# <a name="reset-method-of-the-cim_diskpartition-class"></a>Método Reset da classe CIM \_ DiskPartition

O método **Reset** solicita uma redefinição do dispositivo lógico. Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará 0 (zero) se a solicitação tiver sido executada com êxito, 1 (uma) se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.

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

[\_DISKPARTITION CIM](reset-method-in-class-cim-diskpartition.md)
</dt> <dt>

[**\_DISKPARTITION CIM**](cim-diskpartition.md)
</dt> </dl>

 

 




