---
description: Windows Os dispositivos portáteis dão suporte aos seguintes atributos de propriedade.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Atributos de propriedade (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Property
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 85bf37b716349aae164594eeb8085e8c6df9dc5445728bbf7d9222705a9cb8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843559"
---
# <a name="property-attributes-portabledeviceh"></a>Atributos de propriedade (PortableDevice. h)

Windows Os dispositivos portáteis dão suporte aos seguintes atributos de propriedade. Esses atributos são retornados pelos seguintes métodos:

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties:: GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| Atributo                                           | VarType         | Descrição                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **o \_ atributo de propriedade WPD \_ \_ pode \_ excluir**           | **BOOL do VT \_**    | Um valor booliano que especifica se o cliente pode excluir a propriedade. Para excluir uma propriedade, defina seu valor como VT \_ vazio.                                                                                                                                                                                                                                                                   |
| **o \_ atributo de propriedade WPD \_ \_ pode \_ ler**             | **BOOL do VT \_**    | Um valor booliano que especifica se o cliente pode ler a propriedade.                                                                                                                                                                                                                                                                                                                       |
| **o \_ atributo de propriedade WPD \_ \_ pode \_ gravar**            | **BOOL do VT \_**    | Um valor booliano que especifica se o cliente pode modificar a propriedade.                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ valor padrão do atributo de propriedade WPD \_ \_**        | VT \_ *xxxx*      | Um valor que é definido pelo dispositivo que especifica o valor padrão de uma propriedade. Isso se aplica somente a propriedades graváveis.                                                                                                                                                                                                                                                               |
| **\_elementos de \_ enumeração de atributo de propriedade WPD \_ \_** | **VT \_ desconhecido** | Uma interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém uma coleção de valores para uma propriedade cujo atributo de formulário de **\_ \_ atributo \_ de propriedade WPD** é enumeração de formulário de **atributo de \_ propriedade \_ \_ \_ WPD**. O tipo de dados depende da propriedade que está sendo consultada.                                                                              |
| **\_propriedade de \_ FAST de atributo de propriedade WPD \_ \_**        | **BOOL do VT \_**    | Se for true, essa propriedade pertencerá ao grupo de *Propriedades Fast* . Essas são propriedades que podem ser recuperadas rapidamente do dispositivo.                                                                                                                                                                                                                                                        |
| **\_formulário de \_ atributo de propriedade WPD \_**                  | **\_UI4 VT**     | Um valor enumerado [**WpdAttributeForm**](wpdattributeform.md) que especifica a forma dos valores válidos permitidos para essa propriedade.                                                                                                                                                                                                                                                         |
| **\_nome do \_ atributo da propriedade WPD \_**                  | **LPWStr do VT \_**  | Uma cadeia de caracteres que especifica o nome amigável do script da propriedade. Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '.                                                                                                                                                                                                                                                                    |
| **\_ \_ \_ intervalo máximo de atributos de propriedade WPD \_**            | VT \_ *xxxx*      | O valor máximo de uma propriedade cujo atributo de **\_ formulário de \_ atributo \_ de propriedade WPD** é um intervalo de formulário de **atributo de \_ propriedade \_ \_ \_ WPD**. O tipo de dados pode ser qualquer um dos tipos numéricos.                                                                                                                                                                                                               |
| **\_ \_ \_ intervalo \_ mín. do atributo de propriedade WPD**            | VT \_ *xxxx*      | O valor mínimo de uma propriedade cujo atributo de **\_ formulário de \_ atributo \_ de propriedade WPD** é um intervalo de formulário de **atributo de \_ propriedade \_ \_ \_ WPD**. O tipo de dados pode ser qualquer um dos tipos numéricos.                                                                                                                                                                                                               |
| **\_etapa do \_ intervalo do atributo de propriedade WPD \_ \_**           | VT \_ *xxxx*      | O valor de Step de uma propriedade cujo atributo de **\_ formulário de \_ atributo \_ de propriedade WPD** é um intervalo de formulário de **atributo de \_ propriedade \_ \_ \_ WPD**. A etapa especifica por quanto uma propriedade de intervalo deve ser alterada. Por exemplo, uma propriedade com um valor mínimo de 10, um valor máximo de 20, e uma etapa de 5 poderia ter os seguintes valores: **10**, **15**, **20**. O tipo de dados pode ser qualquer um dos tipos numéricos. |
| **\_ \_ expressão regular de atributo de propriedade WPD \_ \_**   | **LPWStr do VT \_**  | Uma cadeia de caracteres de expressão regular que especifica valores aceitáveis para propriedades cujo formulário é uma **\_ \_ \_ \_ \_ expressão regular de formulário de atributo de propriedade WPD**.                                                                                                                                                                                                                                             |
| **\_VarType de \_ atributo de propriedade WPD \_**               | **\_UI4 VT**     | Um inteiro que especifica o VARTYPE da propriedade, por exemplo, **VT \_ bool**.                                                                                                                                                                                                                                                                                                              |
| **\_ \_ tamanho máximo do atributo de propriedade WPD \_ \_**             | **\_UI8 VT**     | Um valor que especifica o tamanho máximo para o valor dessa propriedade, em bytes.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades**](properties-and-attributes.md)
</dt> </dl>

 

 




