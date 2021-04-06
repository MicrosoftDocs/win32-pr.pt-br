---
title: Limite de tempo do servidor com IDirectorySearch
description: Para evitar o uso de todo o tempo de CPU e impedir que outras operações sejam executadas, especifique o limite de tempo de pesquisa para um valor pequeno e, em seguida, execute novamente o aplicativo mais tarde se ele falhar ao gerar o relatório.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Limite de tempo do servidor com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, limite de tempo do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915884"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Limite de tempo do servidor com IDirectorySearch

Ao solicitar uma pesquisa em um servidor ocupado, talvez você queira solicitar que o servidor restrinja a pesquisa a um limite de tempo especificado. Por exemplo, você deseja executar um aplicativo para gerar um relatório semanal em um servidor que está sendo executado perto de sua capacidade. Para evitar o uso de todo o tempo de CPU e impedir que outras operações sejam executadas, especifique o limite de tempo de pesquisa para um valor pequeno e, em seguida, execute novamente o aplicativo mais tarde se ele falhar ao gerar o relatório.

Alguns servidores podem impor seu próprio limite de tempo administrativo. Nesses casos, se você especificar um valor de limite de tempo de pesquisa maior que o limite de tempo administrativo, o servidor irá ignorar sua especificação e usar seu valor de limite de tempo interno.

O padrão para o limite de tempo do servidor é sem limite. Para definir um limite de tempo de servidor, defina uma opção de pesquisa de limite de tempo de SEARCHPREF de anúncios com um valor **\_ inteiro de ADSTYPE** que contenha o limite de tempo de servidor, em segundos, na matriz de [**\_ \_ informações de SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . **\_ \_ \_** Essa operação é mostrada no exemplo de código a seguir. Um limite de tempo de servidor igual A zero indica que não há limite de tempo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




