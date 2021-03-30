---
title: Escopo da consulta
description: O escopo de uma consulta é determinado pelo objeto ao qual você está associado.
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- escopo da consulta ADSI
- ADSI de consultas, escopo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac51fc261cb418db0018acd996c248766896a25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634864"
---
# <a name="scope-of-query"></a>Escopo da consulta

O escopo de uma consulta é determinado pelo objeto ao qual você está associado. Se não tiver certeza de onde o objeto está localizado dentro da empresa, você precisará fazer a maior pesquisa possível. No entanto, se você souber que o objeto estará contido em um domínio específico, como o domínio ao qual o usuário está conectado ou dentro de um grupo específico, como o grupo gerentes, defina o escopo da pesquisa para refletir a circunstância. Para obter o melhor desempenho, você deve tentar direcionar o escopo para pesquisar o menor número de objetos possíveis.

Quando não tiver certeza de onde um objeto estará localizado na empresa, você poderá associar ao serviço de catálogo global. O serviço de catálogo global contém uma lista de todos os objetos no diretório e um pequeno subconjunto de atributos de cada objeto. Depois de localizar o objeto no catálogo global, você pode recuperar seu nome distinto do catálogo global e usá-lo para associar ao objeto para executar outras operações.

Depois de decidir a qual objeto associar, você pode restringir ainda mais a consulta a um dos seguintes escopos: uma consulta base, uma consulta de nível único ou uma pesquisa de subárvore, conforme mostrado na ilustração a seguir.

![objetos na raiz de uma pesquisa de uma pesquisa de base, de um nível ou de subárvore](images/netds6.png)

## <a name="base"></a>Base

Uma consulta base limita a pesquisa apenas ao objeto base. O número máximo de objetos retornados é sempre um. Essa pesquisa pode ser usada para verificar a existência de um objeto. Por exemplo, se você tiver um nome diferenciado de um objeto e precisar verificar a existência do objeto com base no caminho, você poderá usar uma pesquisa de nível único. Se a pesquisa falhar, você poderá pressupor que o objeto pode ter sido renomeado ou movido para um local diferente, ou que você tenha dado dados incorretos sobre o objeto. Lembre-se de que você deve armazenar o GUID em vez do nome distinto se desejar revisitar um objeto. Isso permite que o objeto seja renomeado ou movido na hierarquia de diretório sem interromper o link persistente.

## <a name="one-level"></a>Um Nível

Uma pesquisa de nível único é restrita aos filhos imediatos de um objeto base, mas exclui o objeto base em si. Essa configuração pode executar uma pesquisa direcionada para objetos filho imediatos de um objeto pai. Por exemplo, se você tiver um objeto pai chamado P1, e seus filhos imediatos forem: C1, C2, C3, em uma pesquisa de nível único, C1, C2 e C3 devem ser incluídos ao avaliar os critérios, mas P1 não faria parte da pesquisa. Uma pesquisa de nível único pode ser usada para enumerar todos os filhos de um objeto. Na verdade, em alguns provedores ADSI, a enumeração [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) se traduz em uma pesquisa de nível único.

## <a name="subtree"></a>Subárvore

Uma pesquisa de subárvore, também conhecida como uma pesquisa profunda, inclui todos os objetos abaixo do objeto base, excluindo o próprio objeto base. Essa pesquisa pode gerar referências a outros servidores. Essa pesquisa tem o maior escopo e pode retornar um grande conjunto de resultados. Se possível, pesquise pelo menos um atributo indexado e defina as configurações de referências (para obter mais informações, consulte [desempenho e manipulação de grandes conjuntos de resultados](performance-and-handling-large-result-sets.md)) para corresponder aos seus requisitos de pesquisa. Também é recomendável que os resultados de uma pesquisa de subárvore sejam executados de forma assíncrona e paginada para reduzir a sobrecarga do servidor e a eficácia da rede. Uma pesquisa de subárvore normalmente é usada para pesquisar objetos para um determinado escopo. Por exemplo, pesquise todos os usuários com contas que irão expirar em 30 dias ou menos.

 

 




