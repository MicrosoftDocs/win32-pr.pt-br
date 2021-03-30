---
title: Anti-moniker
description: O OLE fornece uma implementação de um tipo especial de moniker chamado de anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005657"
---
# <a name="anti-monikers"></a>Anti-moniker

O OLE fornece uma implementação de um tipo especial de moniker chamado de *anti-moniker*. Você usa esse moniker na criação de novas classes moniker. Você o usa como o inverso do moniker no qual ele é composto, cancelando efetivamente esse moniker, praticamente da mesma forma que o operador ".." move um nível de diretório para cima em um comando do sistema de arquivos.

É necessário ter um anti-moniker disponível, porque depois que um moniker composto é criado, não é possível excluir partes do moniker se, por exemplo, um objeto se mover. Em vez disso, você usa um anti-moniker para remover uma ou mais entradas de um moniker composto.

Os antimonikers são uma classe moniker explicitamente destinada a uso como inverso. COM define a função [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) nomeada, que retorna um anti-moniker. Geralmente, você usa essa função para implementar o método [**IMoniker:: inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .

Um anti-moniker é apenas um inverso para esses tipos de moniker que são implementados para tratar os permonikers como inversos. Por exemplo, se você quiser remover a última parte de um moniker composto, não deverá criar um anti-moniker e Compose-lo no final da composição. Não é possível ter certeza de que a última parte da composição considera um antimoniker como inverso. Em vez disso, você deve chamar [**IMoniker:: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) no moniker composto, especificando **false** como o primeiro parâmetro. Isso cria um enumerador que retorna os moniker do componente na ordem inversa. Use o enumerador para recuperar a última parte da composição e chame [**inversa**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) nesse moniker. O moniker retornado por **inverso** é o que você precisa para remover a última parte da composição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers compostos](composite-monikers.md)
</dt> <dt>

[Monikers de arquivo](file-monikers.md)
</dt> <dt>

[Monikers de item](item-monikers.md)
</dt> <dt>

[Monikers de ponteiro](pointer-monikers.md)
</dt> </dl>

 

 




