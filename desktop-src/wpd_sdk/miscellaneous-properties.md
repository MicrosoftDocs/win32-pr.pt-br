---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades diversas.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Propriedades diversas (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769140"
---
# <a name="miscellaneous-properties"></a>Propriedades diversas

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades diversas.



| Propriedade                                       | VarType         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **a \_ opção de API WPD \_ \_ usa \_ fluxo de dados claros \_ \_** | **BOOL do VT \_**    | Um valor booliano que especifica se o fluxo de dados criado para transferência de dados será claro, ou seja, o DRM não está envolvido. Os clientes podem definir essa opção adicionando-a às propriedades do objeto passado para [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).<br/>                                                                                                                                                   |
| **\_versão do serviço WPD \_**                      | **LPWStr do VT \_**  | Uma cadeia de caracteres que especifica a versão de implementação de um determinado serviço de dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **\_tipos de conteúdo de pasta WPD \_ \_ \_ permitidos**       | **VT \_ desconhecido** | Um valor que especifica os tipos de objeto que podem ser filhos diretos dessa pasta. As pastas filhas podem ter recursos diferentes. Essa propriedade é um [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém \_ valores de CLSID VT que especificam tipos de objeto permitidos.<br/> Para obter uma lista de tipos de objeto definidos por dispositivos portáteis do Windows, consulte [requisitos para objetos](requirements-for-objects.md).<br/>                                         |
| **\_categoria de \_ objeto \_ funcional WPD**          | **CLSID do VT \_**   | Um valor que especifica a categoria funcional do objeto.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **\_perfis de \_ informações de renderização WPD \_**      | **VT \_ desconhecido** | Um [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) que contém várias interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) , cada uma delas contendo as configurações de propriedade para um perfil ao qual o objeto dá suporte.                                                                                                                                                                                                                                            |
| **\_nome de \_ exibição do local de dica de objeto WPD \_ \_ \_** | **LPWStr do VT \_**  | Se um objeto for um local de dica, essa propriedade indicará o nome específico da dica a ser exibido para o usuário em vez do nome do objeto. Os drivers podem especificar dicas de local para vários tipos de objeto. Esses são locais de armazenamento preferenciais para pastas que mantêm um tipo de objeto específico. Um equivalente seria a pasta minhas imagens para arquivos de imagem no Windows. Se essa propriedade não existir, normalmente o [nome do \_ objeto \_ WPD](object-properties.md) será usado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




