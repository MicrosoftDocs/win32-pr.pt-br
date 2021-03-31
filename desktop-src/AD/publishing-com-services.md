---
title: Publicando serviços COM+
description: Os serviços baseados em COM fornecem um proxy de aplicativo na forma de um pacote do Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publicando serviços COM+
- Active Directory, usando, publicando um serviço, serviços COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004904"
---
# <a name="publishing-com-services"></a>Publicando serviços COM+

Os serviços baseados em COM fornecem um proxy de aplicativo na forma de um pacote do Windows Installer (MSI). Esse arquivo. msi contém o nome do servidor a ser usado e outros elementos necessários, como proxy/stubs e bibliotecas de tipos necessários para o marshaling. O snap-in Serviços de componentes gera automaticamente esses proxies de aplicativo para aplicativos de servidor COM+.

Os proxies de aplicativo são publicados em objetos de política no Active Directory usando o editor de Política de Grupo. Nenhuma intervenção especial é necessária no aplicativo cliente. A conta de computador/usuário no computador cliente deve estar em uma UO configurada para usar o objeto de política no qual os proxies de aplicativo são publicados. O associador de COM localiza automaticamente o servidor por meio do diretório quando o cliente estabelece uma instância dos objetos preocupados.

 

 




