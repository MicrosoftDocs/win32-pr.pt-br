---
description: A interface IUpdateSearcher define as propriedades a seguir.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propriedades de IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dc3af2635fff4260a44261333b23cbfcf1661793ad613f08bb288db452b93d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130428"
---
# <a name="iupdatesearcher-properties"></a>Propriedades de IUpdateSearcher

A interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define as propriedades a seguir.



| Propriedade                                                                                           | Descrição                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Obtém e define um valor booliana que indica se chamadas futuras para os métodos [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) e [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) resultam em uma atualização automática para o WUA (Agente de Atualização Windows). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifica o aplicativo cliente atual.                                                                                                                                                                                                   |
| [**IncludePotentiallySupersededUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Obtém e define um valor booliana que indica se os resultados da pesquisa incluem atualizações que são superadas por outras atualizações nos resultados da pesquisa.                                                                                          |
| [**Online**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Obtém e define um valor booliana que indica se [**o UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) fica online para pesquisar atualizações.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Obtém e define um site a ser pesquisado quando o site a ser pesquisado não é um site Windows Atualização.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Obtém e define [**um valor ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica o servidor para pesquisar atualizações.                                                                                                                            |




 

 

 



