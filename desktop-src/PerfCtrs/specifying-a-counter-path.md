---
description: O sistema usa contadores para coletar dados de desempenho.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Especificar um Caminho do Contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750772"
---
# <a name="specifying-a-counter-path"></a>Especificar um Caminho do Contador

O sistema usa contadores para coletar dados de desempenho. Cada contador é identificado exclusivamente por meio de seu nome e seu caminho ou local. A sintaxe de um caminho de contador é:

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

O elemento Computer especifica o nome ou o endereço IP do computador do qual você deseja consultar dados de desempenho. O nome do computador será opcional se o contador estiver localizado no computador local.

O elemento Perfobject especifica o objeto de desempenho a ser consultado. Um objeto de desempenho pode ser um componente físico, como processadores, discos e memória, ou um objeto do sistema, como processos e threads. Cada objeto do sistema está relacionado a um elemento funcional dentro do computador e tem um conjunto de contadores padrão atribuído a ele. Cada computador pode ter um conjunto diferente de objetos de desempenho e contadores instalados nele, pois os aplicativos podem instalar seus próprios objetos e contadores de desempenho. Para obter uma lista dos objetos de desempenho e dos contadores instalados no seu computador, consulte a caixa de diálogo **Adicionar contadores** na ferramenta de desempenho em seu computador. Esses objetos também são listados na caixa de diálogo Procurar PDH (consulte os [contadores de navegação](browsing-counters.md)). Para obter uma lista de objetos e contadores de desempenho do sistema, consulte [contadores por objeto](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).

O ParentInstance, ObjectInstance e InstanceIndex serão incluídos no caminho se várias instâncias do objeto puderem existir. Por exemplo, processos e threads são vários objetos de instância porque mais de um processo ou thread podem ser executados ao mesmo tempo. Se um objeto puder ter mais de uma instância, o caminho do contador deverá especificar uma instância de objeto.

O formato dos elementos relacionados à instância depende do tipo de objeto. Se o objeto tiver instâncias simples, o formato será apenas o nome da instância entre parênteses. Por exemplo:

``` syntax
(Explorer)
```

Se a instância desse objeto também exigir um nome de instância pai, o nome da instância pai deverá vir antes da instância do objeto e ser separado por um caractere de barra invertida. Por exemplo, os threads pertencem a processos. Se você consultar um objeto de thread, também deverá especificar o processo ao qual ele pertence, conforme mostrado no exemplo a seguir:

``` syntax
(Explorer/0)
```

Se o objeto tiver várias instâncias que têm a mesma cadeia de caracteres de nome, elas poderão ser indexadas sequencialmente especificando o índice de instância prefixado por um sinal de libra. Os índices de instância são baseados em 0. Se você quiser consultar a primeira instância, não inclua \# 0 – basta especificar o nome da instância. Para especificar a segunda instância, use \# 1; para especificar a terceira instância, use \# 2; e assim por diante. Por exemplo:

``` syntax
(Explorer/0#1)
```

O elemento Counter Especifica o contador de desempenho que você deseja consultar para o objeto de desempenho fornecido.

A PDH usa os seguintes caracteres especiais em um caminho de contador. Os provedores não devem usar esses caracteres em seus nomes. Se um provedor usar esses caracteres especiais, a PDH não poderá analisar o caminho completo do contador para obter os nomes do contador e das instâncias.



| Caractere | Descrição                                                |
|-----------|------------------------------------------------------------|
| \\        | Separador genérico para computador, objeto e contador.       |
| (         | Início do nome da instância.                                |
| )         | Final do nome da instância.                                   |
| /         | Separa instância e instância pai.                    |
| \#n       | Identifica uma ocorrência específica de uma instância do mesmo nome. |
| \*        | Caractere curinga.                                        |



 

Os exemplos a seguir mostram os possíveis formatos para caminhos de contador:

-   \\\\\\contador de objeto de computador (índice pai/instância \# ) \\
-   \\\\\\contador de objeto de computador (pai/instância) \\
-   \\\\\\contador de objeto de computador (índice de instância \# ) \\
-   \\\\\\contador de objeto (instância) de computador \\
-   \\\\\\contador de objetos de computador \\
-   \\contador de objeto (índice pai/instância \# ) \\
-   \\contador de objeto (pai/instância) \\
-   \\contador de objeto (índice de instância \# ) \\
-   \\contador de objeto (instância) \\
-   \\contador de objeto \\

## <a name="using-wildcard-characters"></a>Usando caracteres curinga

Os caminhos de contador podem conter um caractere curinga somente para o nome da instância, conforme mostrado no exemplo a seguir.

``` syntax
\Process(*)\% Processor Time
```

Para expandir o curinga em uma lista de caminhos de contadores que contêm instâncias encontradas no computador ou no arquivo de log, chame [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).

 

 
