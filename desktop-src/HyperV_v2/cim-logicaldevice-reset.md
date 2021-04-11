---
description: Solicita uma redefinição do LogicalDevice.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Método Reset da classe CIM_LogicalDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297208"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a>Método Reset da classe CIM_LogicalDevice (gerenciamento do Hyper-V)

Solicita uma redefinição do LogicalDevice. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método. As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




