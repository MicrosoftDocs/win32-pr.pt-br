---
description: Entenda os conceitos comuns quando você deseja estender Windows Explorer, que é uma das muitas opções de extensibilidade na interface do usuário Windows Shell.
title: Conceitos do Common Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bd0c641e1e265b50180aa6ce4e98eeafbf3f6dc86f4f499dee5267161842e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050517"
---
# <a name="common-explorer-concepts"></a>Conceitos do Common Explorer

O *namespace do* Shell organiza o sistema de arquivos e outros objetos gerenciados pelo Shell em uma única hierarquia estruturada por árvore. Conceitualmente, é uma versão maior e mais inclusiva do sistema de arquivos.

-   [Introdução](#introduction)
-   [Identificando objetos de namespace](#identifying-namespace-objects)
    -   [Item IDs](#item-ids)
    -   [Listas de IDs de Item](#item-id-lists)
    -   [Pidls](#pidls)
    -   [Alocando PIDLs](#allocating-pidls)

## <a name="introduction"></a>Introdução

Uma das principais responsabilidades do Shell é gerenciar e fornecer acesso à ampla variedade de objetos que compõe o sistema. Os mais diversos e familiares desses objetos são as pastas e arquivos que residem em unidades de disco do computador. No entanto, o Shell também gerencia vários sistemas não arquivos ou *objetos* virtuais. Alguns exemplos incluem:

-   Impressoras de rede
-   Outros computadores em rede
-   Painel de Controle aplicativos
-   O Lixeira

Alguns objetos virtuais não envolvem armazenamento físico. O objeto de impressora, por exemplo, contém uma coleção de links para impressoras em rede. Outros objetos virtuais, como o Lixeira, podem conter dados armazenados em uma unidade de disco, mas precisam ser tratados de maneira diferente dos arquivos normais. Por exemplo, um objeto virtual pode ser usado para representar dados armazenados em um banco de dados. Em termos de namespace, os vários itens no banco de dados podem aparecer no Windows Explorer como objetos separados, mesmo que todos eles sejam armazenados em um único arquivo de disco.

Objetos virtuais podem até mesmo estar localizados em computadores remotos. Por exemplo, para facilitar o roaming, os arquivos de documento de um usuário podem ser armazenados em um servidor. Para dar aos usuários acesso aos arquivos de vários computadores desktop, a pasta Meus Documentos no computador desktop que eles estão usando no momento apontará para o servidor, não para o disco rígido do computador desktop. Seu caminho incluirá uma unidade de rede mapeada ou um nome de caminho UNC.

Assim como o sistema de arquivos, o namespace inclui dois tipos básicos de objeto: pastas e arquivos. Objetos de pasta são *os nós* da árvore; eles são contêineres para objetos de arquivo e outras pastas. Objetos de arquivo são *as folhas* da árvore; eles são arquivos de disco normais ou objetos virtuais, como links de impressora. As pastas que não fazem parte do sistema de arquivos às vezes são *conhecidas* como pastas virtuais .

Assim como as pastas do sistema de arquivos, a coleção de pastas virtuais geralmente varia de sistema para sistema. Há três classes de pastas virtuais:

-   Pastas virtuais padrão, como o Lixeira, que são encontradas em todos os sistemas.
-   Pastas virtuais opcionais que têm nomes padrão e funcionalidade, mas podem não estar presentes em todos os sistemas.
-   Pastas não padrão instaladas pelo usuário.

Ao contrário das pastas do sistema de arquivos, os usuários não podem criar novas pastas virtuais por conta própria. Eles só podem instalar aqueles criados por desenvolvedores que não são da Microsoft. O número de pastas virtuais normalmente é muito menor do que o número de pastas do sistema de arquivos. Para ver uma discussão sobre como implementar pastas virtuais, consulte [Extensões de namespace](nse-works.md).

Você pode ver uma representação visual de como o namespace é estruturado na Barra do Explorer do Windows Explorer. Por exemplo, a captura de tela a seguir Windows Explorer mostra um namespace relativamente simples.

![captura de tela mostrando uma exibição do namespace do shell](images/prog1.png)

A raiz final da hierarquia de namespace é a área de trabalho. Imediatamente abaixo da raiz estão várias pastas virtuais, como Meu Computador e Lixeira.

Os sistemas de arquivos das várias unidades de disco podem ser vistos como subconjunto da hierarquia de namespace maior. As raízes desses sistemas de arquivos são subpastas da pasta Meu Computador dados. Meu Computador também inclui as raízes de todas as unidades de rede mapeadas. Outros nós na árvore, como Meus Documentos, são pastas virtuais.

## <a name="identifying-namespace-objects"></a>Identificando objetos de namespace

Antes de usar um objeto de namespace, você deve primeiro ter uma maneira de identificá-lo. Um objeto no sistema de arquivos pode ter um nome como MyFile.htm. Como pode haver outros arquivos com esse nome em outro lugar no sistema, identificar exclusivamente um arquivo ou pasta requer um caminho totalmente qualificado, como "C: \\ MyDocs \\MyFile.htm". Esse caminho é basicamente uma lista ordenada de todas as pastas em um caminho da raiz do sistema de arquivos, C: \\ , terminando com o arquivo .

No contexto do namespace, os caminhos ainda são muito úteis para identificar objetos localizados na parte do sistema de arquivos do namespace. No entanto, eles não podem ser usados para objetos virtuais. Em vez disso, o Shell fornece um meio alternativo de identificação que pode ser usado com qualquer objeto de namespace.

### <a name="item-ids"></a>Item IDs

Em uma pasta, cada objeto tem uma *ID de item*, que é o equivalente funcional de um nome de arquivo ou pasta. A ID do item é, na [**verdade, uma estrutura DEMID:**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid)


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



O **membro abID** é o identificador do objeto. O comprimento de **abID** não está definido e seu valor é determinado pela pasta que contém o objeto . Como não há nenhuma definição padrão de como os **valores abID** são atribuídos por pastas, eles são significativos apenas para o objeto de pasta associado. Os aplicativos devem simplesmente tratá-los como um token que identifica um objeto em uma pasta específica. Como o comprimento de **abID** varia, o **membro cb** mantém o tamanho da estrutura [**DEMID,**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) em bytes.

Como as IDs de item não são úteis para fins de exibição, a pasta que contém o objeto normalmente atribui a ele um nome de exibição. Esse é o nome usado pelo Windows Explorer quando ele exibe o conteúdo de uma pasta. Para obter mais informações sobre como os nomes de exibição são tratados, consulte [Obter informações de uma pasta](folder-info.md).

### <a name="item-id-lists"></a>Listas de IDs de Item

A ID do item raramente é usada por si só. Normalmente, ele faz parte de uma lista de IDs de item, que serve para a mesma finalidade que um caminho do sistema de arquivos. No entanto, em vez da cadeia de caracteres usada para caminhos, uma lista de IDs de item é uma [**estrutura ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Essa estrutura é uma sequência ordenada de uma ou mais IDs de item, terminadas por um NULL de dois **byte.** Cada ID de item na lista de IDs de item corresponde a um objeto de namespace. Sua ordem define um caminho no namespace, assim como um caminho do sistema de arquivos.

A ilustração a seguir mostra uma representação esquematizada da [**estrutura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) que corresponde a C: \\ MyDocs \\MyFile.htm. O nome de exibição de cada ID de item é mostrado acima dela. As larguras variáveis dos membros **abID** são arbitrárias; eles ilustram o fato de que o tamanho desse membro pode variar.

![uma ilustração ilustrativa de um pidl](images/shell2.png)

### <a name="pidls"></a>Pidls

Para a API do Shell, os objetos de namespace geralmente são identificados por um ponteiro para sua estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) ou ponteiro para uma PIDL (lista de identificadores de item). Para sua conveniência, o termo PIDL geralmente se referirá nesta documentação à própria estrutura em vez do ponteiro para ele.

O PIDL mostrado na ilustração anterior é conhecido como um PIDL *completo* *ou* absoluto. Um PIDL completo começa na área de trabalho e contém as IDs de item de todas as pastas intermediárias no caminho. Ele termina com a ID de item do objeto seguida por um NULL de dois byte **de terminação.** Um PIDL completo é semelhante a um caminho totalmente qualificado e identifica exclusivamente o objeto no namespace shell.

As PIDLs completas são usadas com pouca pouca segurança. Muitas funções e métodos esperam um *PIDL relativo.* A raiz de um PIDL relativo é uma pasta, não a área de trabalho. Assim como com caminhos relativos, a série de IDs de item que compõe a estrutura define um caminho no namespace entre dois objetos. Embora eles não identifiquem exclusivamente o objeto, geralmente são menores que um PIDL completo e suficientes para muitas finalidades.

As PIDLs relativas mais usadas, *PIDLs* de nível único, são relativas à pasta pai do objeto. Eles contêm apenas a ID do item do objeto e um **NULL de terminação.** As PIDLs de vários níveis também são usadas para muitas finalidades. Eles contêm duas ou mais IDs de item e normalmente definem um caminho de uma pasta pai para um objeto por meio de uma série de uma ou mais subpastas. Observe que um PIDL de nível único ainda pode ser um PIDL totalmente qualificado. Em particular, os objetos da área de trabalho são filhos da área de trabalho, portanto, suas PIDLs totalmente qualificadas contêm apenas uma ID de item.

Conforme discutido em [Obter a ID](folder-id.md)de uma pasta, a API do Shell fornece várias maneiras de recuperar o PIDL de um objeto. Depois de usá-lo, você geralmente apenas o usa para identificar o objeto quando chama outras funções e métodos da API do Shell. Nesse contexto, o conteúdo interno de um PIDL é opaco e irrelevante. Para os fins desta discussão, pense em PIDLs como tokens que representam objetos de namespace específicos e concentre-se em como usá-los para tarefas comuns.

### <a name="allocating-pidls"></a>Alocando PIDLs

Embora as PIDLs tenham alguma similaridade com caminhos, usá-los requer uma abordagem um pouco diferente. A principal diferença está em como alocar e desalocar memória para eles.

Assim como a cadeia de caracteres usada para um caminho, a memória deve ser alocada para um PIDL. Se um aplicativo criar um PIDL, ele deverá alocar memória suficiente para a [**estrutura ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Para a maioria dos casos discutidos aqui, o Shell cria o PIDL e lida com a alocação de memória. Independentemente do que alocou o PIDL, o aplicativo geralmente é responsável por desalocar o PIDL quando ele não é mais necessário.

Use a [**função CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar o PIDL e a [**função CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar.

 

 
