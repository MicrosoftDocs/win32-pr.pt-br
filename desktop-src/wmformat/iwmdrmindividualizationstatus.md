---
title: Interface IWMDRMIndividualizationStatus
description: A interface IWMDRMIndividualizationStatus permite a recuperação de informações de status avançadas sobre o progresso da individualização. Essa interface é entregue com eventos MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Formato de mídia da interface IWMDRMIndividualizationStatus
- IWMDRMIndividualizationStatus interface windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6242d2c66b165be8c750d71c61020e9a6acc66f68654d73898fd5000ace3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701465"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>Interface IWMDRMIndividualizationStatus

A interface **IWMDRMIndividualizationStatus** permite a recuperação de informações de status avançadas sobre o progresso da individualização.

Essa interface é entregue com eventos MEWMDRMIndividualizationProgress. Muitos desses eventos são gerados entre uma chamada para [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) e a conclusão do processo de individualização, que é sinalizado pela geração de um evento **MEWMDRMIndividualizationCompleted.**

Para recuperar um ponteiro para uma instância da interface **IWMDRMIndividualizationStatus,** primeiro você deve chamar o método **IMFMediaEvent::GetValue** do evento de progresso. O valor recuperado do evento é um ponteiro para a interface **IUnknown** do objeto que implementa a interface **IWMDRMIndividualizationStatus.**

## <a name="members"></a>Membros

A interface **IWMDRMIndividualizationStatus** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMIndividualizationStatus** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMIndividualizationStatus** tem esses métodos.



| Método                                                       | Descrição                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Recupera informações detalhadas sobre individualização.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

