---
description: Os monitores podem ser configurados usando a interface Monitor de Rede interface do usuário. Os usuários finais podem passar critérios de configuração para o monitor usando um formulário HTML armazenado como um arquivo HTM na sub pasta a seguir do SDK Monitor de Rede instalado.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Monitorar a configuração (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b55765774df3be2722c448a1af264162bcd9cdc51ac958cc555bf820d646b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364694"
---
# <a name="monitor-configuration-network-monitor"></a>Monitorar a configuração (Monitor de Rede)

Os monitores podem ser configurados usando a interface Monitor de Rede interface do usuário. Os usuários finais podem passar critérios de configuração para o monitor usando um formulário HTML armazenado como um arquivo HTM na sub pasta a seguir do SDK Monitor de Rede instalado.

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

Quando um usuário final seleciona o botão Definir Configuração do **Monitor,** o navegador gera uma mensagem **HTML POST,** que inclui os nomes e valores de todos os elementos de formulário HTML.

Quando o MCSVC chama o método [IMonitor::D oConfigure,](imonitor-doconfigure.md) o parâmetro *pConfiguration* aponta para os dados da mensagem POST. O código de exemplo a seguir fornece um exemplo de dados de mensagem POST:

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Esses dados são passados como uma cadeia de caracteres ASCII longa. A cadeia de caracteres é parecida com o tamanho e a aparência de seções como %3A%5C e %0D%0A. Essa semelhança é causada por HTML, o que exige que um método coloque todas as cadeias de caracteres ANSI, DBCS e Unicode possíveis em um formato ASCII. Por exemplo, o **método DoConfigure** insere determinados caracteres, como o e ampersand (&) na frente de cada nome de variável para identificá-lo como um nome de variável. %3A%5C é uma forma codificada do caractere de dois-pontos e %0D%0A indica um par de retorno de carro/linha. O código de exemplo a seguir fornece o código HTML resultante conforme interpretado pelo monitor.

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



