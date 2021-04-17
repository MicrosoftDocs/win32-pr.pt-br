---
description: NOUSEROVERRIDE de localidade \_
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748993"
---
# <a name="locale_nouseroverride"></a><span data-ttu-id="db40d-103">NOUSEROVERRIDE de localidade \_</span><span class="sxs-lookup"><span data-stu-id="db40d-103">LOCALE\_NOUSEROVERRIDE</span></span>

> [!Caution]  
> <span data-ttu-id="db40d-104">Como \_ a localidade NOUSEROVERRIDE desabilita as preferências do usuário, seu uso é altamente desencorajado.</span><span class="sxs-lookup"><span data-stu-id="db40d-104">Since LOCALE\_NOUSEROVERRIDE disables user preferences, its use is strongly discouraged.</span></span> <span data-ttu-id="db40d-105">Essa constante não garante a estabilidade dos dados, pois as [localidades personalizadas](custom-locales.md), as atualizações de serviço, as diferentes versões do sistema operacional e outros cenários podem alterar os dados de maneiras inesperadas.</span><span class="sxs-lookup"><span data-stu-id="db40d-105">This constant does not guarantee data stability since [custom locales](custom-locales.md), service updates, different operating system versions, and other scenarios can change data in unexpected ways.</span></span> <span data-ttu-id="db40d-106">Para obter mais informações, consulte [usando dados de localidade persistente](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="db40d-106">For more information, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

<span data-ttu-id="db40d-107">Nenhuma substituição do usuário.</span><span class="sxs-lookup"><span data-stu-id="db40d-107">No user override.</span></span> <span data-ttu-id="db40d-108">Em várias funções, por exemplo, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), essa constante faz com que a função ignore qualquer substituição de usuário e use o valor padrão do sistema para qualquer outra constante especificada na chamada de função.</span><span class="sxs-lookup"><span data-stu-id="db40d-108">In several functions, for example, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), this constant causes the function to bypass any user override and use the system default value for any other constant specified in the function call.</span></span> <span data-ttu-id="db40d-109">As informações são recuperadas do banco de dados de localidade, mesmo se o identificador indicar a localidade atual e o usuário tiver alterado alguns dos valores usando o painel de controle ou se um aplicativo tiver alterado esses valores usando [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="db40d-109">The information is retrieved from the locale database, even if the identifier indicates the current locale and the user has changed some of the values using the Control Panel, or if an application has changed these values by using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="db40d-110">Se essa constante não for especificada, quaisquer valores que o usuário tiver configurado no painel de controle ou que um aplicativo tenha configurado usando [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) têm precedência sobre as configurações de banco de dados para a localidade padrão do sistema atual.</span><span class="sxs-lookup"><span data-stu-id="db40d-110">If this constant is not specified, any values that the user has configured from the Control Panel or that an application has configured using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) take precedence over the database settings for the current system default locale.</span></span>

 

 



