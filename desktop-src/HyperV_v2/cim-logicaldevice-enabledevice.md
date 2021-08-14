---
description: O método EnableDevice foi preterido no lugar do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Método EnableDevice da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a01d1b206d0d38f74c5701c8c088506792cb6ca6f997b9e0280adcc61e5a8633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648521"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>Método EnableDevice da classe CIM \_ LogicalDevice

O método EnableDevice foi preterido no lugar do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.

Solicita que o LogicalDevice esteja habilitado ("Enabled" parâmetro de entrada = TRUE) ou Disabled (= FALSE). Se for bem-sucedido, as propriedades StatusInfo/Enabledstate do dispositivo deverão refletir o estado desejado (habilitado/desabilitado). Observe que a função desse método se sobrepõe à propriedade Requestedstate. O requestedstate foi adicionado ao modelo para manter um registro (ou seja, um valor persistente) da última solicitação de estado. Invocar o método EnableDevice deve definir a propriedade Requestedstate corretamente.

O código de retorno deverá ser 0 se a solicitação tiver sido executada com êxito, 1 se a solicitação não tiver suporte e algum outro valor se ocorrer um erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método. As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Habilitado* \[ no\]
</dt> <dd>

Se verdadeiro, habilite o dispositivo, se FALSE desabilitar o dispositivo.

</dd> </dl>

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

 

 




