---
title: Publicando serviços COM+
description: Os serviços baseados em COM fornecem um proxy de aplicativo na forma de um pacote MSI (instalador de Windows).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publicando serviços COM+
- Active Directory, usando, publicando um serviço, serviços COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91801bbfcbf8efa34ac0b79477dd9d859fc2ed34a8d40bcf0bd829f82cfd571a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025424"
---
# <a name="publishing-com-services"></a>Publicando serviços COM+

Os serviços baseados em COM fornecem um proxy de aplicativo na forma de um pacote MSI (instalador de Windows). Esse .msi arquivo contém o nome do servidor a ser usado e outros elementos necessários, como proxy/stubs e bibliotecas de tipos necessárias para marshalling. O snap-in serviços de componentes gera automaticamente esses proxies de aplicativos para aplicativos COM+ Server.

Os proxies do aplicativo são publicados em objetos de política no Active Directory usando o editor Política de Grupo. Nenhuma intervenção especial é necessária no aplicativo cliente. A conta de computador/usuário no computador cliente deve estar em uma UO configurada para usar o objeto de política no qual os proxies do aplicativo são publicados. O binder COM localiza automaticamente o servidor por meio do diretório quando o cliente estabelece uma instância dos objetos em questão.

 

 




