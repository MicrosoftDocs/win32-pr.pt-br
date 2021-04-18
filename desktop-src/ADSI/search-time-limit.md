---
title: Limite de tempo de pesquisa
description: Quando você solicita uma pesquisa em um servidor que está sob uma carga de trabalho pesada, convém instruir o servidor para restringir a pesquisa a um limite de tempo especificado.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- ADSI do limite de tempo de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756315"
---
# <a name="search-time-limit"></a>Limite de tempo de pesquisa

Quando você solicita uma pesquisa em um servidor que está sob uma carga de trabalho pesada, convém instruir o servidor para restringir a pesquisa a um limite de tempo especificado. Por exemplo, para executar um aplicativo para gerar um relatório semanal em um servidor que esteja executando quase a capacidade e para evitar maximizar o tempo de CPU e impedir que outros trabalhos sejam executados, você pode definir o tempo de pesquisa para um valor pequeno e executar novamente o aplicativo mais tarde se ele falhar ao gerar o relatório.

Alguns servidores podem impor seu próprio limite de tempo administrativo. Nesses casos, se você especificar um valor de limite de tempo de pesquisa maior que o limite de tempo administrativo, o servidor ignorará sua especificação e usará seu limite de tempo administrativo interno em vez disso.

Para obter mais informações sobre como usar a opção de limite de tempo de pesquisa com uma interface de pesquisa específica, consulte:

-   [Limite de tempo do servidor com IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




