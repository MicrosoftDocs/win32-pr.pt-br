---
description: O namespace do Shell organiza o sistema de arquivos e outros objetos gerenciados pelo shell em uma única hierarquia estruturada em árvore. Conceitualmente, é uma versão maior e mais inclusiva do sistema de arquivos.
title: Conceitos comuns do Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5ea7d154ef0455576d91f99eb53dccd93c25339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567220"
---
# <a name="common-explorer-concepts"></a>Conceitos comuns do Explorer

O *namespace* do Shell organiza o sistema de arquivos e outros objetos gerenciados pelo shell em uma única hierarquia estruturada em árvore. Conceitualmente, é uma versão maior e mais inclusiva do sistema de arquivos.

-   [Introdução](#introduction)
-   [Identificando objetos de namespace](#identifying-namespace-objects)
    -   [IDs de item](#item-ids)
    -   [Listas de IDs de itens](#item-id-lists)
    -   [PIDLs](#pidls)
    -   [Alocando PIDLs](#allocating-pidls)

## <a name="introduction"></a>Introdução

Uma das principais responsabilidades do Shell é gerenciar e fornecer acesso à ampla variedade de objetos que compõem o sistema. Os mais numerosos e familiares desses objetos são as pastas e os arquivos que residem nas unidades de disco do computador. No entanto, o Shell gerencia um número de objetos não-arquivo, ou também de objeto *virtual* . Alguns exemplos incluem:

-   Impressoras de rede
-   Outros computadores em rede
-   Aplicativos do painel de controle
-   A lixeira

Alguns objetos virtuais não envolvem o armazenamento físico. O objeto Printer, por exemplo, contém uma coleção de links para impressoras em rede. Outros objetos virtuais, como a lixeira, podem conter dados armazenados em uma unidade de disco, mas precisam ser tratados de forma diferente dos arquivos normais. Por exemplo, um objeto virtual pode ser usado para representar dados armazenados em um banco de dado. Em termos do namespace, os vários itens no banco de dados podem aparecer no Windows Explorer como objetos separados, mesmo que estejam todos armazenados em um único arquivo de disco.

Os objetos virtuais podem até estar localizados em computadores remotos. Por exemplo, para facilitar o roaming, os arquivos de documento de um usuário podem ser armazenados em um servidor. Para conceder aos usuários acesso a seus arquivos de vários computadores desktop, a pasta meus documentos no computador desktop que eles estão usando no momento apontará para o servidor, não para o disco rígido do PC desktop. Seu caminho incluirá uma unidade de rede mapeada ou um nome de caminho UNC.

Assim como o sistema de arquivos, o namespace inclui dois tipos básicos de objeto: pastas e arquivos. Os objetos de pasta são os *nós* da árvore; Eles são contêineres para objetos de arquivo e outras pastas. Os objetos de arquivo são as *folhas* da árvore; Eles são arquivos de disco normais ou objetos virtuais, como links de impressora. As pastas que não fazem parte do sistema de arquivos são, às vezes, chamadas de *pastas virtuais*.

Como as pastas do sistema de arquivos, a coleção de pastas virtuais geralmente varia de sistema para sistema. Há três classes de pastas virtuais:

-   Pastas virtuais padrão, como a lixeira, que são encontradas em todos os sistemas.
-   Pastas virtuais opcionais que têm nomes e funcionalidades padrão, mas podem não estar presentes em todos os sistemas.
-   Pastas não padrão que são instaladas pelo usuário.

Ao contrário das pastas do sistema de arquivos, os usuários não podem criar novas pastas virtuais por conta própria. Eles só podem instalar aqueles criados por desenvolvedores que não sejam da Microsoft. O número de pastas virtuais, portanto, normalmente é muito menor do que o número de pastas do sistema de arquivos. Para obter uma discussão sobre como implementar pastas virtuais, consulte [extensões de namespace](nse-works.md).

Você pode ver uma representação visual de como o namespace é estruturado na barra do Explorer do Windows Explorer. Por exemplo, a captura de tela a seguir do Windows Explorer mostra um namespace relativamente simples.

![captura de tela mostrando uma exibição do namespace do Shell](images/prog1.png)

A raiz final da hierarquia de namespace é a área de trabalho. Imediatamente abaixo da raiz há várias pastas virtuais, como Meu Computador e a lixeira.

Os sistemas de arquivos das várias unidades de disco podem ser vistos como subconjuntos da hierarquia de namespace maior. As raízes desses sistemas de arquivos são subpastas da pasta Meu Computador. O Meu Computador também inclui as raízes de todas as unidades de rede mapeadas. Outros nós na árvore, como meus documentos, são pastas virtuais.

## <a name="identifying-namespace-objects"></a>Identificando objetos de namespace

Antes de usar um objeto de namespace, você deve primeiro ter uma maneira de identificá-lo. Um objeto no sistema de arquivos pode ter um nome como MyFile.htm. Como pode haver outros arquivos com esse nome em outro lugar no sistema, a identificação exclusiva de um arquivo ou pasta requer um caminho totalmente qualificado, como "C: \\ mydocs \\MyFile.htm". Esse caminho é basicamente uma lista ordenada de todas as pastas em um caminho da raiz do sistema de arquivos, C: \\ , terminando com o arquivo.

No contexto do namespace, os caminhos ainda são bastante úteis para identificar objetos localizados na parte do sistema de arquivos do namespace. No entanto, eles não podem ser usados para objetos virtuais. Em vez disso, o Shell fornece um meio alternativo de identificação que pode ser usado com qualquer objeto de namespace.

### <a name="item-ids"></a>IDs de item

Dentro de uma pasta, cada objeto tem uma *ID de item*, que é o equivalente funcional de um nome de arquivo ou pasta. A ID do item é, na verdade, uma estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) :


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



O membro **abID** é o identificador do objeto. O comprimento de **abID** não é definido, e seu valor é determinado pela pasta que contém o objeto. Como não há nenhuma definição padrão para como os valores de **abID** são atribuídos por pastas, eles só são significativos para o objeto de pasta associado. Os aplicativos devem simplesmente tratá-los como um token que identifica um objeto em uma determinada pasta. Como o comprimento de **abID** varia, o membro **CB** mantém o tamanho da estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , em bytes.

Como as IDs de item não são úteis para fins de exibição, a pasta que contém o objeto normalmente atribui a ele um nome de exibição. Esse é o nome usado pelo Windows Explorer quando ele exibe o conteúdo de uma pasta. Para obter mais informações sobre como os nomes de exibição são tratados, consulte [obtendo informações de uma pasta](folder-info.md).

### <a name="item-id-lists"></a>Listas de IDs de itens

A ID do item raramente é usada por si só. Normalmente, ele faz parte de uma lista de ID de item, que tem a mesma finalidade que um caminho do sistema de arquivos. No entanto, em vez da cadeia de caracteres usada para caminhos, uma lista de IDs de itens é uma estrutura de [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Essa estrutura é uma sequência ordenada de uma ou mais IDs de item, terminadas por um **nulo** de dois bytes. Cada ID de item na lista de ID de item corresponde a um objeto de namespace. Sua ordem define um caminho no namespace, muito parecido com um caminho do sistema de arquivos.

A ilustração a seguir mostra uma representação esquemático da estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) que corresponde a C: \\ mydocs \\MyFile.htm. O nome de exibição de cada ID de item é mostrado acima dele. As larguras variadas dos membros **abID** são arbitrárias; eles ilustram o fato de que o tamanho desse membro pode variar.

![uma ilustração esquemático de um PIDL](images/shell2.png)

### <a name="pidls"></a>PIDLs

Para a API do Shell, os objetos de namespace geralmente são identificados por um ponteiro para sua estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) ou ponteiro para uma lista de identificador de item (PIDL). Para sua conveniência, o termo PIDL geralmente se referirá nesta documentação à estrutura em si, e não ao ponteiro para ela.

O PIDL mostrado na ilustração anterior é conhecido como um PIDL *completo*, ou *absoluto*. Um PIDL completo inicia na área de trabalho e contém as IDs de item de todas as pastas intermediárias no caminho. Ele termina com a ID do item do objeto seguido de um **nulo** de dois bytes de terminação. Um PIDL completo é semelhante a um caminho totalmente qualificado e identifica exclusivamente o objeto no namespace do Shell.

As PIDLs completas são usadas com pouca frequência. Muitas funções e métodos esperam um *PIDL relativo*. A raiz de um PIDL relativo é uma pasta, não a área de trabalho. Assim como acontece com caminhos relativos, a série de IDs de item que compõem a estrutura definem um caminho no namespace entre dois objetos. Embora eles não identifiquem exclusivamente o objeto, eles geralmente são menores do que um PIDL completo e suficiente para muitas finalidades.

A PIDLs relativa mais comumente usada, a *PIDLs de nível único*, são relativas à pasta pai do objeto. Eles contêm apenas a ID de item do objeto e um **nulo** de terminação. Os PIDLs de vários níveis também são usados para muitas finalidades. Eles contêm duas ou mais IDs de item e normalmente definem um caminho de uma pasta pai para um objeto por meio de uma série de uma ou mais subpastas. Observe que um PIDL de nível único ainda pode ser um PIDL totalmente qualificado. Em particular, os objetos de área de trabalho são filhos da área de trabalho, portanto, seus PIDLs totalmente qualificados contêm apenas uma ID de item.

Conforme discutido na [obtenção da ID de uma pasta](folder-id.md), a API do Shell fornece várias maneiras de recuperar o PIDL de um objeto. Depois de tê-lo, você costuma apenas usá-lo para identificar o objeto ao chamar outras funções e métodos da API do Shell. Nesse contexto, o conteúdo interno de um PIDL é opaco e irrelevante. Para os fins desta discussão, imagine PIDLs como tokens que representam objetos de namespace específicos e concentre-se em como usá-los para tarefas comuns.

### <a name="allocating-pidls"></a>Alocando PIDLs

Embora PIDLs tenha alguma semelhança com os caminhos, usá-los requer uma abordagem um pouco diferente. A principal diferença é em como alocar e desalocar memória para eles.

Assim como a cadeia de caracteres usada para um caminho, a memória deve ser alocada para um PIDL. Se um aplicativo criar um PIDL, ele deverá alocar memória suficiente para a estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Para a maioria dos casos discutidos aqui, o Shell cria o PIDL e manipula a alocação de memória. Independentemente do que alocou o PIDL, o aplicativo geralmente é responsável por desalocar o PIDL quando ele não é mais necessário.

Use a função [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar o PIDL e a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocá-lo.

 

 
