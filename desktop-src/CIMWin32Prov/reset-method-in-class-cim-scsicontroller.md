---
description: O método reset da classe CIM \_ SCSIController solicita uma redefinição do dispositivo lógico.
ms.assetid: 44084b46-7ada-47f0-acf4-67a824359da6
ms.tgt_platform: multiple
title: Método Reset da classe CIM_SCSIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33d812a8dd0003c96e9ea52a02f46eeb61c1941
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089612"
---
# <a name="reset-method-of-the-cim_scsicontroller-class"></a>Método Reset da classe CIM \_ SCSIController

O método **Reset** da classe CIM \_ SCSIController solicita uma redefinição do dispositivo lógico. Esse método é herdado [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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

[\_SCSICONTROLLER CIM](reset-method-in-class-cim-scsicontroller.md)
</dt> <dt>

[**\_SCSICONTROLLER CIM**](cim-scsicontroller.md)
</dt> </dl>

 

 




