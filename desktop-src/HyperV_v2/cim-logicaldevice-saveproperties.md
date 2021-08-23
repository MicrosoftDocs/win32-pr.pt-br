---
description: Solicita que o dispositivo Capture sua configuração atual, a configuração e/ou as informações de estado em um repositório de backup.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Método SaveProperties da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e5910ea87a6321872b009003bf18d26910b53627dba6c51647f2896dde2e686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648158"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>Método SaveProperties da classe CIM \_ LogicalDevice

Solicita que o dispositivo Capture sua configuração atual, a configuração e/ou as informações de estado em um repositório de backup. O objetivo seria usar essas informações mais tarde (por meio do método restoreproperties) para retornar um dispositivo para sua presente "Condition". Esse método pode não ter suporte de todos os dispositivos. O método deve retornar 0 se for bem-sucedido, 1 se a solicitação não tiver suporte e algum outro valor se ocorrer algum outro erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método. As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

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

 

 




