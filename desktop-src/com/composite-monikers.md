---
title: Monikers compostos
description: Um dos recursos mais úteis dos monikers é que você pode concatenar ou compor os identificadores de recurso juntos.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad815cdb89dda7f58fe1507d43a07a14d24875309668297e20ec51114dd65d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737018"
---
# <a name="composite-monikers"></a>Monikers compostos

Um dos recursos mais úteis dos monikers é que você pode concatenar ou compor os identificadores de recurso juntos. Um *moniker composto* é um moniker que é uma composição de outros monikers e pode determinar a relação entre as partes. Isso permite que você monte o caminho completo de um objeto de acordo com dois ou mais monikers que são equivalentes a caminhos parciais. Você pode compor monikers da mesma classe (como dois identificadores de arquivo) ou de classes diferentes (como um moniker de arquivo e um moniker de item). Se você escrever sua própria classe de moniker, também poderá compor seus monikers com moniker de arquivo ou item. A vantagem básica de uma composição é que ela fornece um trecho de código para implementar cada moniker possível que seja uma combinação de monikers mais simples. Isso reduz significativamente a necessidade de classes de moniker personalizadas específicas.

Como os monikers de classes diferentes podem ser compostos um com o outro, os monikers fornecem a capacidade de unir vários namespaces. O sistema de arquivos define um namespace comum para objetos armazenados como arquivos, pois todos os aplicativos entendem um nome de caminho do sistema de arquivos. Da mesma forma, um objeto de contêiner também define um namespace privado para os objetos que ele contém porque nenhum contêiner entende os nomes gerados por outro contêiner. Os monikers permitem que esses namespaces sejam associados, pois os moniker do arquivo e os monikers do item podem ser compostos. Um cliente moniker pode pesquisar o namespace de todos os objetos usando um único mecanismo. O cliente simplesmente chama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) no moniker, e o código do moniker manipula o resto. Uma chamada para [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) em uma composição cria um nome usando a concatenação de todos os nomes de exibição de monikers individuais.

Além disso, como você pode escrever sua própria classe de moniker, a composição do moniker permite que você adicione extensões personalizadas ao namespace para objetos.

Às vezes, dois monikers de classes específicas podem ser combinados de forma especial. Por exemplo, um moniker de arquivo que representa um caminho incompleto e outro moniker de arquivo que representa um caminho relativo pode ser combinado para formar um moniker de arquivo único que representa o caminho completo. Por exemplo, o arquivo moniker "c: \\ trabalho \\ artístico" pode ser composto com o moniker do arquivo relativo ".. \\ backup \\myfile.doc "para igual a" c: \\ trabalho de \\ backup \\myfile.doc ". Este é um exemplo de *composição não genérica*.

A *composição genérica*, por outro lado, permite a conexão de quaisquer dois monikers, não importa quais são suas classes. Por exemplo, você pode compor um moniker de item em um moniker de arquivo, embora não, é claro, o contrário.

Como uma composição não genérica depende da classe dos monikers envolvidos, seus detalhes são definidos pela implementação de uma classe de moniker específica. Você pode definir novos tipos de composições não genéricas se escrever uma nova classe de moniker. Por outro lado, as composições genéricas são definidas pelo OLE. Os monikers criados como resultado da composição genérica são chamados de monikers compostos genéricos.

Essas três classes, os monikers de arquivo, os monikers de item e os monikers compostos genéricos, todos trabalham juntos e são as classes mais usadas de monikers.

Os clientes do moniker devem chamar [**IMoniker:: ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) para criar uma composição no moniker com outra. O moniker no qual ele é chamado internamente decide se ele pode fazer uma composição genérica ou não genérica. Se a implementação do moniker determinar que uma composição genérica é utilizável, o OLE fornecerá a função [**CreateGenericComposite**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) para facilitar isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers de arquivo](file-monikers.md)
</dt> <dt>

[Monikers de item](item-monikers.md)
</dt> <dt>

[Monikers de ponteiro](pointer-monikers.md)
</dt> </dl>

 

 




