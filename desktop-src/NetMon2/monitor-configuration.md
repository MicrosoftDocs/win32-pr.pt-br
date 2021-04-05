---
description: Os monitores podem ser configurados usando a interface do usuário do Monitor de Rede. Os usuários finais podem passar critérios de configuração para o monitor usando um formulário HTML armazenado como um arquivo HTM na subpasta a seguir do SDK do Monitor de Rede instalado.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Configuração do monitor (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89125450fc71bba21250a66f5c5458317138899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920998"
---
# <a name="monitor-configuration-network-monitor"></a><span data-ttu-id="3be75-104">Configuração do monitor (Monitor de Rede)</span><span class="sxs-lookup"><span data-stu-id="3be75-104">Monitor Configuration (Network Monitor)</span></span>

<span data-ttu-id="3be75-105">Os monitores podem ser configurados usando a interface do usuário do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="3be75-105">Monitors can be configured using the Network Monitor UI.</span></span> <span data-ttu-id="3be75-106">Os usuários finais podem passar critérios de configuração para o monitor usando um formulário HTML armazenado como um arquivo HTM na subpasta a seguir do SDK do Monitor de Rede instalado.</span><span class="sxs-lookup"><span data-stu-id="3be75-106">End-users can pass configuration criteria to your monitor using an HTML form stored as an HTM file in the following sub folder of your installed Network Monitor SDK.</span></span>

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

<span data-ttu-id="3be75-107">Quando um usuário final seleciona o botão **definir configuração de monitor** , o navegador gera uma mensagem de **postagem** HTML, que inclui os nomes e valores de todos os elementos de formulário HTML.</span><span class="sxs-lookup"><span data-stu-id="3be75-107">When an end user selects the **Set Monitor Configuration** button, the browser generates an HTML **POST** message, which includes the names and values for all the HTML form elements.</span></span>

<span data-ttu-id="3be75-108">Quando o MCSVC chama o método [Imonitor::D oconfigure](imonitor-doconfigure.md) , o parâmetro *pConfiguration* aponta para os dados da mensagem post.</span><span class="sxs-lookup"><span data-stu-id="3be75-108">When the MCSVC calls the [IMonitor::DoConfigure](imonitor-doconfigure.md) method, the *pConfiguration* parameter points to the data from the POST message.</span></span> <span data-ttu-id="3be75-109">O código de exemplo a seguir fornece um exemplo de dados da mensagem POST:</span><span class="sxs-lookup"><span data-stu-id="3be75-109">The following example code provides an example of POST message data:</span></span>

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Esses dados são passados como uma cadeia de caracteres ASCII longa. A cadeia de caracteres parece peculiar, tanto para seu comprimento quanto para a aparência de seções como% 3A% 5C e% 0D% 0A. Essa peculiaridade é causada por HTML, o que exige que um método Coloque todas as cadeias de caracteres ANSI, DBCS e Unicode possíveis em um formato ASCII. Por exemplo, o método **doconfigure** insere determinados caracteres, como o e comercial (&) na frente de cada nome de variável para identificá-lo como um nome de variável. O% 3A% 5C é uma forma codificada do caractere de dois-pontos e% 0D% 0A indica um par de retorno de carro/avanço de linha. <span data-ttu-id="3be75-115">O código de exemplo a seguir fornece o código HTML resultante como interpretado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="3be75-115">The following example code provides the resulting HTML code as interpreted by the monitor.</span></span>

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



