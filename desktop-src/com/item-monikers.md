---
title: Monikers de item
description: Outra classe de moniker implementada por OLE é o moniker do item, que pode ser usado para identificar um objeto contido em outro objeto.
ms.assetid: ddcf3669-4ad0-4a4e-80a6-eb78058cff09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b692502ba44519a2c51a661ef62a51e133ac04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788974"
---
# <a name="item-monikers"></a>Monikers de item

Outra classe de moniker implementada por OLE é o *moniker do item*, que pode ser usado para identificar um objeto contido em outro objeto. Um tipo de objeto contido é um objeto OLE inserido em um documento composto. Um documento composto poderia identificar os objetos inseridos que ele contém, atribuindo a cada um nome arbitrário, como "embedobj1", "embedobj2" e assim por diante. Outro tipo de objeto contido é uma seleção de usuário em um documento, como um intervalo de células em uma planilha ou um intervalo de caracteres em um documento de texto. Um objeto que consiste em uma seleção é chamado de *pseudo-objeto* porque não é tratado como um objeto distinto até que um usuário marque a seleção. Uma planilha pode identificar um intervalo de células usando um nome como "1A: 7F", enquanto um documento de processamento de texto pode identificar um intervalo de caracteres usando o nome de um indicador.

Um moniker de item é útil principalmente quando concatenado, ou *composto*, com outro moniker, um que identifica o contêiner. Um moniker de item geralmente é criado e, em seguida, composto em (por exemplo) um moniker de arquivo para criar o equivalente de um caminho completo para o objeto. Por exemplo, você pode compor o arquivo moniker "c: \\ work \\report.doc" (que identifica o objeto de contêiner) com o item moniker "embedobj1" (que identifica um objeto dentro do contêiner) para formar o moniker "c: \\ Work \\report.doc\\ embedobj1", que identifica exclusivamente um objeto específico dentro de um determinado arquivo. Você também pode concatenar os monikers de item adicionais para identificar objetos profundamente aninhados. Por exemplo, se "embedobj1" for o nome de um objeto de planilha, para identificar um determinado intervalo de células nesse objeto de planilha, você poderá acrescentar outro moniker de item para criar um moniker que seria o equivalente de "c: \\ work \\report.doc\\ Embedobj1 \\ 1a: 7F".

Quando combinado com um moniker de arquivo, um moniker de item forma um caminho completo. Os monikers de item, portanto, estendem a noção de nomes de caminho além do sistema de arquivos, definindo nomes de caminho para identificar objetos individuais, não apenas arquivos.

Há uma diferença significativa entre um moniker de item e um moniker de arquivo. O caminho contido em um moniker de arquivo é significativo para qualquer pessoa que entenda o sistema de arquivos, enquanto o caminho parcial contido em um moniker de item é significativo apenas para um contêiner específico. Todos sabem o que "c: \\ work \\report.doc" refere-se a, mas apenas um objeto de contêiner específico sabe o que "1a: 7F" refere-se a. Um contêiner não pode interpretar um moniker de item criado por outro aplicativo; o único contêiner que sabe qual objeto é referenciado por um moniker de item é o contêiner que atribuiu o moniker de item ao objeto em primeiro lugar. Por esse motivo, a origem do objeto nomeado pela combinação de um arquivo e um moniker de item não deve apenas implementar [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)para facilitar a vinculação do moniker do arquivo, mas também [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) para facilitar a resolução do nome do moniker do item no objeto apropriado, no contexto de um arquivo.

A vantagem dos monikers é que alguém que usa um moniker para localizar um objeto não precisa entender o nome contido no moniker do item, desde que o moniker do item faça parte de uma composição. Em geral, não faz sentido que um moniker de item exista por conta própria. Em vez disso, você comporia um moniker de item em um moniker de arquivo. Em seguida, você chamaria [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) na composição, que associa os monikers individuais dentro dela, interpretando os nomes.

Para criar um objeto de moniker de item e retornar seu ponteiro para o provedor de moniker, o OLE fornece a função auxiliar [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker). Essa função cria um objeto moniker do item e retorna seu ponteiro para o provedor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers compostos](composite-monikers.md)
</dt> <dt>

[Monikers de arquivo](file-monikers.md)
</dt> <dt>

[Monikers de ponteiro](pointer-monikers.md)
</dt> </dl>

 

 




