---
description: Solicita que o Dispositivo capture suas informações atuais de configuração, configuração e/ou estado em um armazenamento de back-back.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Método SaveProperties da CIM_LogicalDevice classe
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
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>Método SaveProperties da classe \_ LogicalDevice cim

Solicita que o Dispositivo capture suas informações atuais de configuração, configuração e/ou estado em um armazenamento de back-back. A meta seria usar essas informações posteriormente (por meio do método RestoreProperties) para retornar um Dispositivo à sua "condição" atual. Esse método pode não ter suporte de todos os Dispositivos. O método deverá retornar 0 se for bem-sucedido, 1 se a solicitação não tiver suporte e algum outro valor se ocorrer qualquer outro erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador ValueMap no método . As cadeias de caracteres para as quais o conteúdo valueMap é 'convertido' também podem ser especificadas na subclasse como um qualificador de matriz Valores.

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
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




