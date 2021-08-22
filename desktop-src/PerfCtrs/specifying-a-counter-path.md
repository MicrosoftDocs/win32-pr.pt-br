---
description: O sistema usa contadores para coletar dados de desempenho.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Especificar um Caminho do Contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a359762e4d959992bebd338c4b3ee29825c63b4cb081b70722c82fb3376b5d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143799"
---
# <a name="specifying-a-counter-path"></a>Especificar um Caminho do Contador

O sistema usa contadores para coletar dados de desempenho. Cada contador é identificado exclusivamente por meio de seu nome e seu caminho ou local. A sintaxe de um caminho de contador é:

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

O elemento Computer especifica o nome ou o endereço IP do computador do qual você deseja consultar dados de desempenho. O nome do computador será opcional se o contador estiver localizado no computador local.

O elemento PerfObject especifica o objeto de desempenho a ser consultado. Um objeto de desempenho pode ser um componente físico, como processadores, discos e memória, ou um objeto do sistema, como processos e threads. Cada objeto do sistema está relacionado a um elemento funcional no computador e tem um conjunto de contadores padrão atribuídos a ele. Cada computador pode ter um conjunto diferente de objetos de desempenho e contadores instalados nele porque os aplicativos podem instalar seus próprios objetos de desempenho e contadores. Para ver uma lista dos objetos de desempenho e  contadores instalados em seu computador, consulte a caixa de diálogo Adicionar Contadores na ferramenta Desempenho em seu computador. Esses objetos também são listados na caixa de diálogo Procurar PDH (consulte [Contadores de Navegação](browsing-counters.md)). Para ver uma lista de contadores e objetos de desempenho do sistema, consulte [Contadores por objeto](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).

ParentInstance, ObjectInstance e InstanceIndex serão incluídos no caminho se várias instâncias do objeto puderem existir. Por exemplo, processos e threads são vários objetos de instância porque mais de um processo ou thread pode ser executado ao mesmo tempo. Se um objeto puder ter mais de uma instância, o caminho do contador deverá especificar uma instância de objeto.

O formato dos elementos relacionados à instância depende do tipo de objeto. Se o objeto tiver instâncias simples, o formato será apenas o nome da instância entre parênteses. Por exemplo:

``` syntax
(Explorer)
```

Se a instância desse objeto também exigir um nome de instância pai, o nome da instância pai deverá vir antes da instância do objeto e ser separado por um caractere de barra. Por exemplo, os threads pertencem a processos. Se você consultar um objeto de thread, também deverá especificar o processo ao qual ele pertence, conforme mostrado no exemplo a seguir:

``` syntax
(Explorer/0)
```

Se o objeto tiver várias instâncias que têm a mesma cadeia de caracteres de nome, elas poderão ser indexadas sequencialmente especificando o índice de instância prefixado por um sinal de peso. Os índices de instância são baseados em 0. Se você quiser consultar a primeira instância, não inclua \# 0– basta especificar o nome da instância. Para especificar a segunda instância, use \# 1; para especificar a terceira instância, use \# 2 e assim por diante. Por exemplo:

``` syntax
(Explorer/0#1)
```

O elemento Counter especifica o contador de desempenho que você deseja consultar para o objeto de desempenho determinado.

O PDH usa os seguintes caracteres especiais em um caminho de contador. Os provedores não devem usar esses caracteres em seus nomes. Se um provedor usar esses caracteres especiais, o PDH não poderá analisar o caminho completo do contador para obter os nomes do contador e das instâncias.



| Caractere | Descrição                                                |
|-----------|------------------------------------------------------------|
| \\        | Separador genérico para computador, objeto e contador.       |
| (         | Início do nome da instância.                                |
| )         | Fim do nome da instância.                                   |
| /         | Separa a instância e a instância pai.                    |
| \#n       | Identifica uma ocorrência específica de uma instância de mesmo nome. |
| \*        | Caractere curinga.                                        |



 

Os exemplos a seguir mostram os possíveis formatos para caminhos de contador:

-   \\\\contador \\ de objeto de computador (índice pai/instância) \# \\
-   \\\\contador \\ de objeto de computador (pai/instância) \\
-   \\\\contador \\ computer object(instance \# index) \\
-   \\\\contador \\ de objeto de computador \\ (instância)
-   \\\\contador \\ de objetos de \\ computador
-   \\contador object(parent/instance \# index) \\
-   \\contador object(parent/instance) \\
-   \\contador object(instance \# index) \\
-   \\contador object(instance) \\
-   \\contador \\ de objetos

## <a name="using-wildcard-characters"></a>Usando caracteres curinga

Os caminhos de contador podem conter um caractere curinga somente para o nome da instância, conforme mostrado no exemplo a seguir.

``` syntax
\Process(*)\% Processor Time
```

Para expandir o curinga em uma lista de caminhos de contador que contêm instâncias encontradas no computador ou no arquivo de log, chame [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).

 

 
