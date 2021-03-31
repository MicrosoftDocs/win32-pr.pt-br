---
title: Interface IWMDRMIndividualizationStatus
description: A interface IWMDRMIndividualizationStatus permite a recuperação de informações de status avançadas sobre o progresso da individualização. Essa interface é fornecida com eventos MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Formato de mídia do Windows da interface IWMDRMIndividualizationStatus
- Formato de mídia do Windows da interface IWMDRMIndividualizationStatus, descrito
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917554"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>Interface IWMDRMIndividualizationStatus

A interface **IWMDRMIndividualizationStatus** permite a recuperação de informações de status avançadas sobre o progresso da individualização.

Essa interface é fornecida com eventos MEWMDRMIndividualizationProgress. Muitos desses eventos são gerados entre uma chamada para [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) e a conclusão do processo de individualização, que é sinalizado pela geração de um evento **MEWMDRMIndividualizationCompleted** .

Para recuperar um ponteiro para uma instância da interface **IWMDRMIndividualizationStatus** , você deve primeiro chamar o método **IMFMediaEvent:: GetValue** do evento Progress. O valor que você recupera do evento é um ponteiro para a interface **IUnknown** do objeto que implementa a interface **IWMDRMIndividualizationStatus** .

## <a name="members"></a>Membros

A interface **IWMDRMIndividualizationStatus** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMIndividualizationStatus** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMIndividualizationStatus** tem esses métodos.



| Método                                                       | Descrição                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Recupera informações detalhadas sobre individualização.<br/> |



 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

