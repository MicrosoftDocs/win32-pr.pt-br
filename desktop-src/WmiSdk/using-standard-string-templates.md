---
description: Vários consumidores, como o consumidor de evento de script ativo ou o consumidor de evento de linha de comando, têm propriedades de cadeia de caracteres com o qualificador de modelo.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Usando modelos de cadeia de caracteres padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c60a28730b890a5e922489a47b5b382b545cd6712d61cb976e96b549039ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049934"
---
# <a name="using-standard-string-templates"></a>Usando modelos de cadeia de caracteres padrão

Vários consumidores, como o consumidor de evento de script ativo ou o consumidor de evento de linha de comando, têm propriedades de cadeia de caracteres com o qualificador de **modelo** . Essas propriedades usam modelos de cadeia de caracteres padrão para construir uma cadeia de caracteres configurada em parte pela instância do consumidor e em parte por um evento. a estrutura de um modelo de cadeia de caracteres padrão é semelhante à especificação de variável de ambiente do Microsoft Windows.

A lista a seguir mostra alguns exemplos da linguagem do modelo:

-   A cadeia de caracteres "texto aqui" sempre produz a cadeia de caracteres "texto aqui".
-   "% CPUUtilization%" sempre produz o valor da propriedade **CPUUtilization** do evento que está sendo entregue. Se a propriedade não for uma cadeia de caracteres, ela será convertida em uma cadeia de caracteres; por exemplo, "90" ou "TRUE".
-   "A utilização da CPU desse processador é% CPUUtilization% no momento" incorpora o valor da propriedade **CPUUtilization** do evento à cadeia de caracteres, produzindo algo como "a utilização da CPU desse processador é 90 no momento".
-   "% TargetInstance. CPUUtilization%" recupera o valor da propriedade **CPUUtilization** na instância inserida da propriedade **TargetInstance** .
-   "%%" produz um único% Sign.
-   Se a propriedade que está sendo recuperada for uma matriz, toda a matriz será produzida no seguinte formato: "(1, 5, 10, 1024)". Se houver apenas um elemento na matriz, os parênteses serão omitidos. Se não houver nenhum elemento na matriz, "()" será produzido.
-   Se uma propriedade for um objeto inserido, a representação MOF do objeto será produzida (semelhante ao método [**IWbemClassObject:: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).
-   Se uma propriedade de uma matriz inserida de objetos for solicitada, ela será tratada como uma propriedade com um valor de matriz. Por exemplo:% MyEvents. TargetInstance. DriverLetter% poderia produzir ' ("C:", "D:") ' se MyEvents for uma matriz de eventos de modificação de instância incorporada.

## <a name="string-literals"></a>Literais de cadeia de caracteres

Qualquer coisa dentro de um par de aspas é considerada uma literal de cadeia de caracteres e não será substituída.

O exemplo a seguir mostra a cadeia de caracteres que o compilador vê para "a utilização da CPU é% CPUUtilization%".

``` syntax
CPU utilization is %CPUUtilization%
```

Essa cadeia de caracteres produz a saída a seguir.

``` syntax
CPU utilization is 90
```

Por outro lado, a cadeia de caracteres "a utilização da CPU é \\ "% CPUUtilization% \\ "" é vista pelo compilador da seguinte maneira.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Essa cadeia de caracteres produz a saída a seguir, sem substituição de variável.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



