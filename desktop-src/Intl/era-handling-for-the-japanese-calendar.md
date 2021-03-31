---
description: Gerenciamento de eras para o calendário japonês
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Gerenciamento de eras para o calendário japonês
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829793"
---
# <a name="era-handling-for-the-japanese-calendar"></a><span data-ttu-id="24475-103">Gerenciamento de eras para o calendário japonês</span><span class="sxs-lookup"><span data-stu-id="24475-103">Era Handling for the Japanese Calendar</span></span>

<span data-ttu-id="24475-104">Muitos calendários têm apagamento, como AD/BC ou CE/A.C..</span><span class="sxs-lookup"><span data-stu-id="24475-104">Many calendars have eras, such as AD/BC or CE/BCE.</span></span> <span data-ttu-id="24475-105">No calendário do japonês, os anos são descritos por nengō, uma combinação do número do ano e do nome da era.</span><span class="sxs-lookup"><span data-stu-id="24475-105">In the Japanese Calendar, years are described by nengō, a combination of the year number and era name.</span></span> <span data-ttu-id="24475-106">Por exemplo, 2009 é Heisei 21.</span><span class="sxs-lookup"><span data-stu-id="24475-106">For example, 2009 is Heisei 21.</span></span> <span data-ttu-id="24475-107">No passado, os nomes de era japoneses mudaram com frequência, mas agora o apagamento em Japonês é alterado apenas em sucessão Imperial.</span><span class="sxs-lookup"><span data-stu-id="24475-107">In the past, Japanese era names changed frequently, but now the Japanese eras change only on imperial succession.</span></span> <span data-ttu-id="24475-108">O Windows e o Microsoft .NET têm suporte historicamente os quatro apagamentos modernos sob esta política: Meiji, Taishō, Shōwa e Heisei.</span><span class="sxs-lookup"><span data-stu-id="24475-108">Windows and Microsoft .NET have historically supported the four modern eras under this policy: Meiji, Taishō, Shōwa and Heisei.</span></span>

<span data-ttu-id="24475-109">Com o Windows 7, o Windows Server 2008 R2 e o .NET Framework 4, a Microsoft reconhece que o apagamento adicional pode ser adicionado no futuro.</span><span class="sxs-lookup"><span data-stu-id="24475-109">With Windows 7, Windows Server 2008 R2, and the .NET Framework 4, Microsoft recognizes that additional eras may be added in the future.</span></span> <span data-ttu-id="24475-110">Nessas versões do Windows, os dados de era são armazenados no registro sob a chave:</span><span class="sxs-lookup"><span data-stu-id="24475-110">On these versions of Windows the era data is stored in the registry under the key:</span></span><dl> <span data-ttu-id="24475-111">HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ NLS \\ calendários \\ Japonês \\ apagar</span><span class="sxs-lookup"><span data-stu-id="24475-111">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Nls\\Calendars\\Japanese\\Eras</span></span>  
</dl>

<span data-ttu-id="24475-112">Se necessário, o apagamento adicional pode ser adicionado a essa chave por meio do processo normal de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="24475-112">If necessary, additional eras can be added to that key through the normal Windows Update process.</span></span> <span data-ttu-id="24475-113">Essa chave pode ser exibida usando o editor do registro (Regedit.exe).</span><span class="sxs-lookup"><span data-stu-id="24475-113">This key can be viewed using the registry editor (Regedit.exe).</span></span> <span data-ttu-id="24475-114">Um exemplo da chave e dos valores fornecidos no Windows 7 é:</span><span class="sxs-lookup"><span data-stu-id="24475-114">An example of the key and values shipped in Windows 7 is:</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

<span data-ttu-id="24475-115">O nome de cada valor de era a data em que a era começa no calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="24475-115">The name of each era value is the date the era begins in the Gregorian calendar.</span></span> <span data-ttu-id="24475-116">O valor contém o nome da era em Japonês, o nome abreviado em Japonês, o nome em inglês e um nome abreviado em inglês:</span><span class="sxs-lookup"><span data-stu-id="24475-116">The value contains the era name in Japanese, the abbreviated name in Japanese, the name in English, and an abbreviated name in English:</span></span><dl> <span data-ttu-id="24475-117">"aaaa MM DD" = "JE \_ aje \_ EE \_ AEE"</span><span class="sxs-lookup"><span data-stu-id="24475-117">"YYYY MM DD"="JE\_AJE\_EE\_AEE"</span></span>  
</dl>where

-   <span data-ttu-id="24475-118">"Aaaa MM DD" é a data do calendário gregoriano do início da era no formato de ano, mês, dia em que o ano é de 4 dígitos, o dia é 2 dígitos e o mês também tem 2 dígitos.</span><span class="sxs-lookup"><span data-stu-id="24475-118">"YYYY MM DD" is the Gregorian date of the start of the era in year, month, day form where year is 4 digits, day is 2 digits and month is also 2 digits.</span></span> <span data-ttu-id="24475-119">Um espaço separa cada parte da data.</span><span class="sxs-lookup"><span data-stu-id="24475-119">A space separates each part of the date.</span></span>
-   <span data-ttu-id="24475-120">"JE" é o nome japonês da era e é seguido por um sublinhado.</span><span class="sxs-lookup"><span data-stu-id="24475-120">"JE" is the Japanese name of the era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="24475-121">"AJE" é o nome abreviado da era, em Japonês, e é seguido por um sublinhado.</span><span class="sxs-lookup"><span data-stu-id="24475-121">"AJE" is the abbreviated name of the era, in Japanese, and is followed by an underscore.</span></span>
-   <span data-ttu-id="24475-122">"EE" é o nome em inglês da era japonesa e é seguido por um sublinhado.</span><span class="sxs-lookup"><span data-stu-id="24475-122">"EE" is the English name of the Japanese era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="24475-123">"AEE" é o nome abreviado em inglês da era japonesa.</span><span class="sxs-lookup"><span data-stu-id="24475-123">"AEE" is the abbreviated English name of the Japanese era.</span></span>

<span data-ttu-id="24475-124">Uma consideração para os desenvolvedores de aplicativos é a possibilidade de que o apagamento adicional seja adicionado por Windows Update ou outros meios.</span><span class="sxs-lookup"><span data-stu-id="24475-124">One consideration for application developers is the possibility that additional eras will be added by Windows Update or other means.</span></span> <span data-ttu-id="24475-125">Nesse caso, o aplicativo pode encontrar mais do que os quatro apagados esperados para o calendário japonês.</span><span class="sxs-lookup"><span data-stu-id="24475-125">In that case the application may encounter more than the expected four eras for the Japanese calendar.</span></span> <span data-ttu-id="24475-126">Para testadores de fins de teste podem adicionar uma era adicional ao registro; no entanto, isso deve ser restrito apenas a computadores de teste, pois ele afeta o comportamento de todo o computador.</span><span class="sxs-lookup"><span data-stu-id="24475-126">For testing purposes testers may add an additional era to the registry; however, that should be restricted to test machines only, as it impacts the behavior of the entire machine.</span></span>

<span data-ttu-id="24475-127">Um exemplo de tal chave que poderia ser usada para o teste a seguir.</span><span class="sxs-lookup"><span data-stu-id="24475-127">An example of such a key that could be used for test follows.</span></span> <span data-ttu-id="24475-128">Essa alteração pode ser feita com o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="24475-128">This change can be made with the registry editor.</span></span> <span data-ttu-id="24475-129">(Este é um exemplo de uso de teste somente e não pretende prever quaisquer adições futuras.)</span><span class="sxs-lookup"><span data-stu-id="24475-129">(This is an example for test use only, and is not intended to predict any future additions.)</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

<span data-ttu-id="24475-130">Observe que isso afeta apenas os computadores que executam o Windows 7 e posterior ou o .NET Framework 4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="24475-130">Note that this only impacts machines running Windows 7 and later or .NET Framework 4 and later.</span></span> <span data-ttu-id="24475-131">Os desenvolvedores de aplicativos são incentivados a testar seus aplicativos com tal teste adicional de apagamento para garantir que seus aplicativos continuem a funcionar se o apagamento adicional for adicionado em alguma data futura.</span><span class="sxs-lookup"><span data-stu-id="24475-131">Application developers are encouraged to test their applications with such additional test eras to ensure that their applications will continue to work if additional eras are added at some future date.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24475-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24475-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24475-133">Recuperando informações de data e hora</span><span class="sxs-lookup"><span data-stu-id="24475-133">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="24475-134">Identificadores de calendário</span><span class="sxs-lookup"><span data-stu-id="24475-134">Calendar Identifiers</span></span>](calendar-identifiers.md)
</dt> </dl>

 

 



