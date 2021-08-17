---
title: NDF Interfaces
description: As interfaces a seguir podem ser usadas para estender a funcionalidade das Classes Auxiliares da Microsoft identificadas como extensíveis.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16ff5dde9246798392903f47370e663e26dd6be7f21252f8791bfee267018b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801946"
---
# <a name="ndf-interfaces"></a>NDF Interfaces

As interfaces a seguir podem ser usadas para estender a funcionalidade das Classes Auxiliares da Microsoft identificadas como extensíveis. Embora essa funcionalidade não seja necessária para a maioria dos aplicativos, ela pode fornecer diagnósticos e resoluções mais específicos em alguns casos.

> [!Note]  
> Essas interfaces e seus métodos associados são para desenvolvedores que implementam suas próprias classes auxiliares de terceiros que estendem a funcionalidade NDF.

 



| Nome da Interface                                                 | Descrição                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Chamado pelo NDF para a maioria das atividades que ocorrem durante um diagnóstico.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Chamado pelo NDF para capturar e fornecer informações associadas a diagnósticos e resolução de problemas relacionados à rede. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Chamado pelo NDF para validar se ele tem informações necessárias                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Reservado para uso do sistema.                                                                                                 |



 

 

 




