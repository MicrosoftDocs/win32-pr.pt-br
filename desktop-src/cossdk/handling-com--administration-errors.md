---
description: Tratando erros de administração COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Tratando erros de administração COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 965276fff68edf45ae27423ee4ed707e4bb7f1476b0237dab270538e0fa0f1be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306704"
---
# <a name="handling-com-administration-errors"></a>Tratando erros de administração COM+

Erros gerados ao usar os objetos COMAdmin são relatados de duas maneiras, da seguinte maneira:

-   Usando códigos de erro específicos para a biblioteca COMAdmin.
-   Usando informações de erro estendidas disponíveis em uma coleção [**Especial errorInfo.**](errorinfo.md)

## <a name="error-codes"></a>Códigos de erro

Você lida com códigos de erro de administração como faria com qualquer mensagem de erro COM. No Microsoft Visual C++, esses códigos são retornados como **valores HRESULT.** No Microsoft Visual Basic, eles são lançados como exceções que você pode capturar. Para programadores C++, os códigos de erro de administração COM+ são definidos em Winerror.h. Para Visual Basic programadores, eles estão disponíveis por meio do Visual Basic IDE.

## <a name="errorinfo-collection"></a>Coleção ErrorInfo

Quando ocorre um erro, sinalizado por algum tipo de código de falha, informações mais detalhadas podem estar disponíveis, dependendo da natureza do erro. Os objetos COMAdmin fornecem informações estendidas em circunstâncias em que a causa precisa da falha é difícil de determinar sem um relatório detalhado, como com várias operações de leitura e gravação.

Por exemplo, quando você usa métodos como [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) em um [**objeto COMAdminCatalogCollection,**](comadmincatalogcollection.md) você pode ler ou escrever dados para cada item na coleção. Podem ocorrer erros complicados e podem ser difíceis de diagnosticar com base em um único código de erro numérico. Portanto, a Biblioteca COMAdmin faz informações de erro estendidas por meio de uma coleção especial.

Quando as informações de erro estendidas estão disponíveis, são colocadas na coleção [**ErrorInfo**](errorinfo.md) relacionada à coleção original que teve o erro. Para recuperar o relatório de erros, obter a coleção **ErrorInfo** relacionada à coleção original e examinar os itens que ela contém. Você pode recuperar a coleção **ErrorInfo** usando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em [**COMAdminCatalogCollection**](comadmincatalogcollection.md), deixando o segundo parâmetro em branco, em que normalmente você especificaria a propriedade Key de um item pai.

Quando você receber um erro, deverá obter e popular imediatamente a coleção [**ErrorInfo**](errorinfo.md) da coleção que falhou, sem executar nenhuma outra operação nessa coleção. Caso contrário, a **coleção ErrorInfo** será redefinida e não detalha essa falha.

Os itens na coleção [**ErrorInfo**](errorinfo.md) expõem as propriedades especiais de relatório de erros MajorRef e MinorRef, que detalham a causa específica do erro. Para obter mais informações, consulte **ErrorInfo**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
</dt> <dt>

[Exemplo introdutório usando o catálogo de administração COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



