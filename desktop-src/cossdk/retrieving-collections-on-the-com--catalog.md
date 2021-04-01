---
description: Recuperando coleções no catálogo COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recuperando coleções no catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646282"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Recuperando coleções no catálogo COM+

Os dados no catálogo COM+ são armazenados em uma hierarquia de coleções. Na ferramenta administrativa serviços de componentes, muitas dessas coleções aparecem como pastas na árvore de console. As coleções que não aparecem como pastas só podem ser acessadas programaticamente. Coleções servem como contêineres para itens. Os itens em uma determinada coleção são de um tipo consistente; ou seja, todos eles representam o mesmo tipo de elemento e pode haver um número arbitrário de itens em uma coleção. Por exemplo, a coleção de [**aplicativos**](applications.md) contém um item para cada aplicativo com+ que está instalado no computador. Essa coleção aparece na ferramenta administrativa como a pasta **aplicativos com+** .

As coleções ocorrem em uma estrutura hierárquica porque os elementos que elas contêm seguem uma ordem inato de inclusão. Por exemplo, como os componentes são instalados em um aplicativo COM+, a coleção de [**componentes**](components.md) é logicamente incorporadasda na coleção de [**aplicativos**](applications.md) . Mais especificamente, para manter os componentes instalados nesse aplicativo específico, há uma coleção de **componentes** distintos para cada item na coleção de **aplicativos** .

Você deve obter uma coleção no catálogo sempre que desejar recuperar um item e definir propriedades nele. No caso geral, você precisa percorrer várias coleções para obter o elemento desejado. Para obter o procedimento para fazer isso, consulte [navegando na hierarquia da coleção com+](navigating-the-com--collection-hierarchy.md).

Depois de recuperar uma coleção e antes de trabalhar diretamente com os itens que ela contém, você deve preencher a coleção, que busca dados para o conteúdo da coleção do catálogo COM+. Para obter detalhes, consulte [populando coleções com+](populating-com--collections.md).

Além disso, há um recurso que você pode usar que permite consultar dinamicamente para ver quais coleções relacionadas estão disponíveis em uma determinada coleção que você está mantendo. Para obter detalhes, consulte [consultando as coleções relacionadas disponíveis](querying-for-available-related-collections.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
</dt> <dt>

[Manipulando erros de administração COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemplo introdutório usando o catálogo de administração do COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



