---
description: O Auxiliar de IP estende suas habilidades para gerenciar interfaces de rede. Há uma correspondência um-para-um entre as interfaces e adaptadores em um determinado computador. Uma interface é uma abstração no nível de IP, enquanto um adaptador é uma abstração no nível do datalink.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gerenciando interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb46ecba6f1c5780960f6d8e363db9ec04d0cc3611da1caf023ec95bf5a99a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146689"
---
# <a name="managing-interfaces"></a>Gerenciando interfaces

O Auxiliar de IP estende suas habilidades para gerenciar interfaces de rede. Há uma correspondência um-para-um entre as interfaces e adaptadores em um determinado computador. Uma interface é uma abstração no nível de IP, enquanto um adaptador é uma abstração no nível do datalink.

Use as funções descritas nos parágrafos a seguir para gerenciar interfaces no computador local.

A [**função GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) retorna o número de interfaces no computador local.

A [**função GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) retorna uma tabela que contém os nomes e os índices correspondentes para as interfaces no computador local. Para obter exemplos de código **que envolvem GetInterfaceInfo,** consulte [Gerenciando interfaces usando GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

A [**função GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) usa um índice de interface e retorna um índice de interface compatível com versões anteriores, ou seja, um que usa apenas os 24 bits inferiores. Às vezes, esse tipo de índice é chamado de índice de interface "amigável".

A [**função GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) retorna uma estrutura [**\_ IFROW MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) que contém informações sobre uma interface específica no computador local. Essa função requer que o chamador fornece o índice da interface.

A [**função GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) retorna uma tabela de entradas [**\_ IFROW MIB,**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) uma para cada interface no computador.

Use a [**função SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) para modificar a configuração de uma interface específica.

 

 
