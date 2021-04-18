---
description: Os NPPs (provedores de pacotes de rede) fornecem interfaces COM que são chamadas por aplicativos NPP e Monitor de Rede.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfaces NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753136"
---
# <a name="npp-interfaces"></a>Interfaces NPP

Os NPPs (provedores de pacotes de rede) fornecem interfaces COM que são chamadas por aplicativos NPP e Monitor de Rede. Ao chamar [CreateNPPInterface](createnppinterface.md), lembre-se de que cada NPP é representado como um único objeto com em processo. Os aplicativos podem criar uma instância de qualquer número de objetos NPP. No entanto, cada objeto instanciado deve usar um — e apenas um — das cinco interfaces NPP.

Observe também que diferentes interfaces NPP fornecem dados de rede em várias formas. Por exemplo, Monitor de Rede usa a interface **IDelaydC** para capturar o tráfego de rede e salvá-lo em um arquivo de captura; enquanto os monitores usam a interface **IRTC** para capturar o tráfego de rede em tempo real. A tabela a seguir descreve Monitor de Rede interfaces NPP.



| Interface                | Descrição                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Captura o tráfego de rede armazenado em um arquivo de captura. Essa interface é usada pelos aplicativos Monitor de Rede e NPP.                                          |
| [IESP](iesp.md)         | Captura o tráfego de rede armazenado em um arquivo de captura e fornece estatísticas avançadas em um formato de arquivo ESP especial. Essa interface é usada por aplicativos NPP |
| [IRTC](irtc.md)         | Captura o tráfego de rede em tempo real e dispara eventos quando eles ocorrem. Essa interface é usada por [*monitores*](m.md) e aplicativos NPP.     |
| [IStats](istats.md)     | Recupera estatísticas como dados brutos em vez de quadros. Essa interface é usada por aplicativos NPP, como [*Perfmon*](p.md).                     |



 

 

 



