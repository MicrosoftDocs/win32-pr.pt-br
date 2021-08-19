---
title: Interface IWMDRMNonSilentLicenseAquisition
description: A interface IWMDRMNonSilentLicenseAquisition fornece métodos que permitem a aquisição de licenças, exigindo a intervenção do usuário. Essa interface pode ser obtida com a execução de uma aquisição de licença não silenciosa.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Formato de mídia do Windows da interface IWMDRMNonSilentLicenseAquisition
- Formato de mídia do Windows da interface IWMDRMNonSilentLicenseAquisition, descrito
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c953588cb457e8afb21cca38e9daed08b2387ab9fb7871ecd6b17dae9dca152f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110346"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Interface IWMDRMNonSilentLicenseAquisition

A interface **IWMDRMNonSilentLicenseAquisition** fornece métodos que permitem a aquisição de licenças, exigindo a intervenção do usuário.

Essa interface pode ser obtida com a execução de uma aquisição de licença não silenciosa. Depois de chamar [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , um evento **MEWMDRMLicenseAcquisitionCompleted** será gerado. Chame o método **IMFMediaEvent:: GetValue** do evento para obter um ponteiro para uma interface **IUnknown** que pode ser consultada para um ponteiro para uma instância dessa interface.

## <a name="members"></a>Membros

A interface **IWMDRMNonSilentLicenseAquisition** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNonSilentLicenseAquisition** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMNonSilentLicenseAquisition** tem esses métodos.



| Método                                                                | Descrição                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Getchallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Recupera o desafio de licença que deve ser postado no servidor de licença.<br/> |
| [**GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Recupera a URL para a qual o desafio de licença deve ser lançado.<br/>           |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Aquisição de licença não silenciosa**](non-silent-license-acquisition.md)
</dt> </dl>

 

