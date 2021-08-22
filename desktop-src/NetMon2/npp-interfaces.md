---
description: Os NPPs (provedores de pacotes de rede) fornecem interfaces COM que são chamadas por aplicativos NPP e Monitor de Rede.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: NPP Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fc38bd5db91354c81f88d9f0fe0a6ad23ce3ccb3ecd4a08c4b6335e25ddd33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676976"
---
# <a name="npp-interfaces"></a>NPP Interfaces

Os NPPs (provedores de pacotes de rede) fornecem interfaces COM que são chamadas por aplicativos NPP e Monitor de Rede. Ao chamar [CreateNPPInterface](createnppinterface.md), lembre-se de que cada NPP é representado como um único objeto COM em processo. Os aplicativos podem insinuar qualquer número de objetos NPP. No entanto, cada objeto instanado deve usar uma das cinco interfaces NPP.

Observe também que diferentes interfaces NPP fornecem dados de rede em vários formulários. Por exemplo, Monitor de Rede usa a interface **IDelaydC** para capturar o tráfego de rede e salvá-lo em um arquivo de captura; enquanto os monitores usam a interface **IRTC** para capturar o tráfego de rede em tempo real. A tabela a seguir descreve Monitor de Rede interfaces NPP.



| Interface                | Descrição                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Captura o tráfego de rede armazenado em um arquivo de captura. Essa interface é usada por aplicativos Monitor de Rede e NPP.                                          |
| [I LTDA](iesp.md)         | Captura o tráfego de rede armazenado em um arquivo de captura e fornece estatísticas aprimoradas em um formato de arquivo ESP especial. Essa interface é usada por aplicativos NPP |
| [IRTC](irtc.md)         | Captura o tráfego de rede em tempo real e dispara eventos quando eles ocorrem. Essa interface é usada por [*monitores e aplicativos*](m.md) NPP.     |
| [IStats](istats.md)     | Recupera estatísticas como dados brutos em vez de quadros. Essa interface é usada por aplicativos NPP, como [*Perfmon*](p.md).                     |



 

 

 



