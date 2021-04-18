---
description: Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de parâmetro para métodos e eventos de um serviço de dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Atributos de parâmetro (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793372"
---
# <a name="parameter-attributes"></a>Atributos de parâmetro

Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de parâmetro para métodos e eventos de um serviço de dispositivo. Esses atributos são retornados pelos seguintes métodos:

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| Atributo                                            | VarType         | Descrição                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ valor padrão do atributo de parâmetro WPD \_ \_**        | VT \_ *xxxx*      | O valor padrão do parâmetro.                                                                                                                                                         |
| **\_elementos de \_ enumeração de atributo de parâmetro WPD \_ \_** | **VT \_ desconhecido** | Uma interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém os valores de enumeração para o parâmetro.                                   |
| **\_formulário de \_ atributo de parâmetro WPD \_**                  | **\_UI4 VT**     | A forma de valores de parâmetro válidos permitidos.                                                                                                                                                 |
| **\_ \_ tamanho máximo do atributo de parâmetro WPD \_ \_**             | **\_UI8 VT**     | O tamanho máximo do parâmetro, em bytes.                                                                                                                                               |
| **\_nome do \_ atributo de parâmetro WPD \_**                  | **LPWStr do VT \_**  | Uma cadeia de caracteres que especifica o nome amigável de script de um parâmetro de evento ou método. Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '.                                                 |
| **\_ordem de \_ atributo de parâmetro WPD \_**                 | **\_UI4 VT**     | O índice de ordem de parâmetro com base em zero, para que um valor de Order igual a 0 corresponda ao primeiro parâmetro.                                                                                       |
| **\_ \_ \_ intervalo mínimo de atributos de parâmetro WPD \_**            | VT \_ *xxxx*      | O valor máximo para um parâmetro do formulário intervalo de \_ formulário de atributo de parâmetro de WPD \_ \_ \_ .                                                                                                       |
| **\_ \_ \_ intervalo máximo de atributos de parâmetro WPD \_**            | VT \_ *xxxx*      | O valor mínimo para um parâmetro do formulário intervalo de \_ formulário de atributo de parâmetro de WPD \_ \_ \_ .                                                                                                       |
| **\_etapa do \_ intervalo do atributo de parâmetro WPD \_ \_**           | VT \_ *xxxx*      | O valor de etapa para um parâmetro do formulário \_ intervalo de formulário de atributo de parâmetro WPD \_ \_ \_ .                                                                                                          |
| **\_ \_ expressão regular de atributo de parâmetro WPD \_ \_**   | **LPWStr do VT \_**  | Uma expressão regular que especifica valores aceitáveis para parâmetros da forma \_ \_ \_ \_ \_ expressão regular do formato de atributo de parâmetro de WPD.                                                      |
| **\_tipo de \_ uso de atributo de parâmetro WPD \_ \_**           | **\_UI4 VT**     | Um inteiro que especifica o uso de um parâmetro de método, por exemplo, in/out. Os valores válidos são do tipo de enumeração de [**\_ tipos de \_ uso \_ de parâmetro WPD**](wpd-parameter-usage-types.md) . |
| **\_VarType de \_ atributo de parâmetro WPD \_**               | **\_UI4 VT**     | O VarType do parâmetro.                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




