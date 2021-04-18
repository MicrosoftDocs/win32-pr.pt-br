---
description: Manipulando erros de administração COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Manipulando erros de administração COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780702"
---
# <a name="handling-com-administration-errors"></a>Manipulando erros de administração COM+

Os erros gerados ao usar os objetos COMAdmin são relatados de duas maneiras, da seguinte maneira:

-   Usando códigos de erro específicos para a biblioteca COMAdmin.
-   Usando informações de erro estendidas disponíveis em uma coleção de [**errorInfo**](errorinfo.md) especial.

## <a name="error-codes"></a>Códigos de erro

Você lida com códigos de erro de administração como faria COM qualquer mensagem de erro COM. No Microsoft Visual C++, esses códigos são retornados como valores **HRESULT** . No Microsoft Visual Basic, eles são lançados como exceções que você pode capturar. Para programadores do C++, os códigos de erro da administração COM+ são definidos no Winerror. h. Para os programadores Visual Basic, eles estão disponíveis por meio do IDE do Visual Basic.

## <a name="errorinfo-collection"></a>Coleção ErrorInfo

Quando ocorre um erro, sinalizado por algum tipo de código de falha, informações mais detalhadas podem estar disponíveis, dependendo da natureza do erro. Os objetos COMAdmin fornecem informações estendidas em circunstâncias em que a causa exata da falha é difícil de determinar sem um relatório detalhado, como com várias operações de leitura e gravação.

Por exemplo, quando você usa métodos como [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) em um objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , você pode ler ou gravar dados para cada item na coleção. Podem ocorrer erros complicados e podem ser difíceis de diagnosticar com base em um único código de erro numérico. Portanto, a biblioteca COMAdmin faz informações de erro estendidas por meio de uma coleção especial.

Quando informações de erro estendidas estão disponíveis, elas são colocadas na coleção [**errorInfo**](errorinfo.md) que está relacionada à coleção original que tinha o erro. Para recuperar o relatório de erros, obtenha a coleção **errorInfo** relacionada à coleção original e examine os itens que ela contém. Você pode recuperar a coleção **errorInfo** usando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em [**COMAdminCatalogCollection**](comadmincatalogcollection.md), deixando o segundo parâmetro em branco, em que você normalmente especificaria a propriedade de chave de um item pai.

Quando receber um erro, você deverá obter imediatamente e preencher a coleção [**errorInfo**](errorinfo.md) para a coleção que falhou, sem executar nenhuma outra operação nessa coleção. Caso contrário, a coleção **errorInfo** será redefinida e não detalhará essa falha.

Os itens na coleção [**errorInfo**](errorinfo.md) expõem as propriedades especiais de relatório de erros MajorRef e MinorRef, que detalham a causa específica do erro. Para obter mais informações, consulte **errorInfo**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
</dt> <dt>

[Exemplo introdutório usando o catálogo de administração do COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



