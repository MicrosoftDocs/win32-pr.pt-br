---
description: Define os elementos ServiceId, Types, PnPXHardwareId e PnPXCompatibleId para os serviços definidos pelo host de serviço.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento hospedado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d281b5e058f8716c12c655ebcdb9a17bdfa4fb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994883"
---
# <a name="hosted-element"></a>elemento hospedado

Define os elementos [**ServiceId**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)e [**PnPXCompatibleId**](pnpxcompatibleid.md) para os serviços definidos pelo host de serviço.

## <a name="usage"></a>Uso

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                 | Descrição                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [**PnPXCompatibleId**](pnpxcompatibleid.md)<br/> | Especifica o identificador compatível com PnP-X do serviço.<br/> <br/> |
| [**PnPXHardwareId**](pnpxhardwareid.md)<br/>     | Especifica o identificador de hardware PnP-X do serviço.<br/> <br/>   |
| [**ServiceID**](serviceid.md)<br/>               | Define um identificador de serviço para o host de serviço.<br/> <br/>        |
| [**Tipos**](types.md)<br/>                       | Define uma lista de nomes qualificados XSD.<br/> <br/>                    |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                         | Descrição                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Os metadados de hospedagem para o dispositivo a ser implementado.<br/> <br/> |



## <a name="remarks"></a>Comentários

Cada serviço fornecido por um host de serviço deve ter suas próprias informações de elemento **hospedado** para garantir que o serviço seja publicado corretamente em respostas a solicitações de metadados.

Os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) são opcionais, mas quando usados, eles devem ser usados juntos. Se um estiver presente, o outro também deverá estar presente.

Se um elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) estiver presente, pelo menos um elemento **hospedado** deverá conter ambos os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) . Da mesma forma, se os elementos **PnPXHardwareId** e **PnPXCompatibleId** estiverem presentes em um elemento **hospedado** , pelo menos um elemento **PnPXDeviceCategory** deverá estar presente dentro do elemento [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




