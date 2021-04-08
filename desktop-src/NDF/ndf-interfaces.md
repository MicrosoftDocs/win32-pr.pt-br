---
title: Interfaces NDF
description: As interfaces a seguir podem ser usadas para estender a funcionalidade das classes auxiliares da Microsoft que são identificadas como extensível.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004791"
---
# <a name="ndf-interfaces"></a>Interfaces NDF

As interfaces a seguir podem ser usadas para estender a funcionalidade das classes auxiliares da Microsoft que são identificadas como extensível. Embora essa funcionalidade não seja necessária para a maioria dos aplicativos, ela pode fornecer diagnósticos e resoluções mais específicos em alguns casos.

> [!Note]  
> Essas interfaces e seus métodos associados são para desenvolvedores que implementam suas próprias classes auxiliares de terceiros que estendem a funcionalidade NDF.

 



| Nome da Interface                                                 | Descrição                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Chamado pelo NDF para a maioria das atividades que ocorrem durante um diagnóstico.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Chamado pelo NDF para capturar e fornecer informações associadas aos diagnósticos e à resolução de problemas relacionados à rede. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Chamado pelo NDF para validar que ele tem as informações necessárias                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Reservado para uso do sistema.                                                                                                 |



 

 

 




