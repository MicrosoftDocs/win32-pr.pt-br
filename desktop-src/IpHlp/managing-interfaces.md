---
description: O auxiliar de IP estende sua capacidade de gerenciar interfaces de rede. Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador. Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gerenciando interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169407"
---
# <a name="managing-interfaces"></a>Gerenciando interfaces

O auxiliar de IP estende sua capacidade de gerenciar interfaces de rede. Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador. Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.

Use as funções descritas nos parágrafos a seguir para gerenciar interfaces no computador local.

A função [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) retorna o número de interfaces no computador local.

A função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) retorna uma tabela que contém os nomes e os índices correspondentes para as interfaces no computador local. Para obter exemplos de código envolvendo **GetInterfaceInfo** , consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

A função [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) usa um índice de interface e retorna um índice de interface compatível com versões anteriores, ou seja, um que usa apenas os 24 bits inferiores. Esse tipo de índice, às vezes, é chamado de índice de interface "amigável".

A função [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) retorna uma [**estrutura \_ IFROW MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) que contém informações sobre uma interface específica no computador local. Essa função requer que o chamador forneça o índice da interface.

A função [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) retorna uma tabela de [**entradas \_ IFROW de MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , uma para cada interface no computador.

Use a função [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) para modificar a configuração de uma interface específica.

 

 
