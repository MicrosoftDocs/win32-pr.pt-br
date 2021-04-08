---
description: Um objeto de desempenho é uma entidade para a qual os dados de desempenho estão disponíveis.
ms.assetid: 97b9c9ec-e758-4928-b3fa-90d220bca5fb
title: Design de objeto e contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9556882f5dd6c323697d9d41fa80727895550a5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921743"
---
# <a name="object-and-counter-design"></a>Design de objeto e contador

Um objeto de desempenho é uma entidade para a qual os dados de desempenho estão disponíveis. Os contadores de desempenho definem o tipo de dados que está disponível para um objeto de desempenho. Um aplicativo pode fornecer informações para vários objetos de desempenho. Os objetos de desempenho podem conter contadores de instância única ou vários contadores de instância. Um único objeto de instância retorna um único conjunto de valores de contador.

Um objeto de várias instâncias retorna uma instância do objeto para cada ocorrência do objeto que o aplicativo controla. Por exemplo, um aplicativo SCSI poderia definir um objeto de unidade com dois contadores, como bytes lidos e bytes gravados. Quando o consumidor consulta o objeto, a DLL de desempenho retorna uma instância do objeto para cada unidade que o aplicativo controla.

Depois de decidir se o objeto dá suporte a uma única instância ou a várias instâncias, você precisa decidir sobre o tipo de contadores que deseja que o objeto forneça. Por exemplo, você pode fornecer valores de contador que são exibidos como valores brutos, como taxas ou como porcentagens.

Para obter uma lista de tipos de contadores predefinidos que você deve escolher, consulte a seção tipos de contadores do [Kit de implantação do Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)). Dependendo do tipo de contador, você pode simplesmente fornecer os dados brutos, ou você também pode ter que fornecer informações de tempo e frequência e dados de contador adicionais usados pelo consumidor para calcular um valor de exibição.

O método usado para coletar os dados pode ser tão simples quanto incrementar um contador cada vez que uma rotina específica no aplicativo é chamada ou pode envolver cálculos demorados. Os contadores e temporizadores devem ser incrementados e nunca ser limpos. Os contadores podem encapsular, desde que eles não sejam quebrados duas vezes entre serem amostrados pelo consumidor. Seu aplicativo pode coletar e armazenar dados durante sua execução normal, desde que não afete seu desempenho.

Para alguns tipos de dados, pode ser mais eficiente ou apropriado coletar os dados sob demanda. Nessa situação, a DLL de desempenho deve se comunicar com o aplicativo de que os dados foram solicitados. Para dados que são caros de coletar (em termos de tempo de processador ou uso de memória), considere coletar dados somente quando o consumidor solicitar dados **dispendiosos** . Isso permite que um consumidor solicite dados rotineiramente para todos os contadores que não são caros. Os dados podem ser solicitados somente quando necessário. A ferramenta de desempenho não coleta dados **caros** .

 

 
