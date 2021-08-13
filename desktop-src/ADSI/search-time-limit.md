---
title: Limite de tempo de pesquisa
description: Ao solicitar uma pesquisa em um servidor que está sob uma carga de trabalho pesada, talvez você queira instruir o servidor a restringir a pesquisa a um limite de tempo especificado.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- ADSI de Limite de Tempo de Pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b666b41db67872cd418cca2d4ef2e3d766fbc1a1d1c1a2d9945eec7dfceb2429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690511"
---
# <a name="search-time-limit"></a>Limite de tempo de pesquisa

Ao solicitar uma pesquisa em um servidor que está sob uma carga de trabalho pesada, talvez você queira instruir o servidor a restringir a pesquisa a um limite de tempo especificado. Por exemplo, para executar um aplicativo para gerar um relatório semanal em um servidor que está executando quase a capacidade e evitar maximizar o tempo de CPU e impedir que outros trabalhos executem, você pode definir o tempo de pesquisa como um valor pequeno e executar novamente o aplicativo mais tarde se ele não conseguir gerar o relatório.

Alguns servidores podem impor seu próprio limite de tempo administrativo. Nesses casos, se você especificar um valor de limite de tempo de pesquisa maior que o limite de tempo administrativo, o servidor ignorará sua especificação e usará seu limite de tempo administrativo interno.

Para obter mais informações sobre como usar a opção de limite de tempo de pesquisa com uma interface de pesquisa específica, consulte:

-   [Limite de tempo do servidor com IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Pesquisando com objetos ActiveX dados](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




