---
title: Interface IWMDRMProvider
description: A interface IWMDRMProvider fornece um método que cria os outros objetos das APIs estendidas do Microsoft Windows Media DRM Client. você pode obter um ponteiro para uma instância dessa interface chamando a função WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Formato de mídia do Windows da interface IWMDRMProvider
- Formato de mídia do Windows da interface IWMDRMProvider, descrito
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641578"
---
# <a name="iwmdrmprovider-interface"></a>Interface IWMDRMProvider

A interface **IWMDRMProvider** fornece um método que cria os outros objetos das APIs estendidas do Microsoft Windows Media DRM Client.

Você pode obter um ponteiro para uma instância dessa interface chamando a função [**WMDRMCreateProvider**](wmdrmcreateprovider.md) . Para obter um ponteiro para uma instância dessa interface que pode criar objetos seguros, você deve chamar a função [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .

## <a name="members"></a>Membros

A interface **IWMDRMProvider** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMProvider** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMProvider** tem esses métodos.



| Método                                              | Descrição                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**CreateObject**](iwmdrmprovider-createobject.md) | Recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.<br/> |



 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

