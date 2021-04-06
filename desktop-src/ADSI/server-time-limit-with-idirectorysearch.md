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
# <a name="server-time-limit-with-idirectorysearch"></a><span data-ttu-id="1a594-105">Limite de tempo do servidor com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="1a594-105">Server Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="1a594-106">Ao solicitar uma pesquisa em um servidor ocupado, talvez você queira solicitar que o servidor restrinja a pesquisa a um limite de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="1a594-106">When you request a search on a busy server, you may want to request that the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="1a594-107">Por exemplo, você deseja executar um aplicativo para gerar um relatório semanal em um servidor que está sendo executado perto de sua capacidade.</span><span class="sxs-lookup"><span data-stu-id="1a594-107">For example, you want to run an application to generate a weekly report on a server that is running near its capacity.</span></span> <span data-ttu-id="1a594-108">Para evitar o uso de todo o tempo de CPU e impedir que outras operações sejam executadas, especifique o limite de tempo de pesquisa para um valor pequeno e, em seguida, execute novamente o aplicativo mais tarde se ele falhar ao gerar o relatório.</span><span class="sxs-lookup"><span data-stu-id="1a594-108">To avoid using all the CPU time and preventing other operations from running, specify the search time limit to a small value and then rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="1a594-109">Alguns servidores podem impor seu próprio limite de tempo administrativo.</span><span class="sxs-lookup"><span data-stu-id="1a594-109">Some servers might impose their own administrative time limit.</span></span> <span data-ttu-id="1a594-110">Nesses casos, se você especificar um valor de limite de tempo de pesquisa maior que o limite de tempo administrativo, o servidor irá ignorar sua especificação e usar seu valor de limite de tempo interno.</span><span class="sxs-lookup"><span data-stu-id="1a594-110">In these cases, if you specify a search time limit value greater than the administrative time limit, the server will ignore your specification and use its internal time limit value instead.</span></span>

<span data-ttu-id="1a594-111">O padrão para o limite de tempo do servidor é sem limite.</span><span class="sxs-lookup"><span data-stu-id="1a594-111">The default for the server time limit is no limit.</span></span> <span data-ttu-id="1a594-112">Para definir um limite de tempo de servidor, defina uma opção de pesquisa de limite de tempo de SEARCHPREF de anúncios com um valor **\_ inteiro de ADSTYPE** que contenha o limite de tempo de servidor, em segundos, na matriz de [**\_ \_ informações de SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1a594-112">To set a server time limit, set an **ADS\_SEARCHPREF\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the server time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="1a594-113">Essa operação é mostrada no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a594-113">This operation is shown in the following code example.</span></span> <span data-ttu-id="1a594-114">Um limite de tempo de servidor igual A zero indica que não há limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="1a594-114">A server time limit of zero indicates no time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




