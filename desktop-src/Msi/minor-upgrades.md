---
description: Uma atualização secundária é uma atualização que faz alterações em muitos recursos.
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: Atualizações secundárias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833bb46e2cafe0545f83c0ed0f8ff8aba00f0695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829473"
---
# <a name="minor-upgrades"></a>Atualizações secundárias

Uma atualização secundária é uma atualização que faz alterações em muitos recursos. Nenhuma das alterações pode exigir a alteração do [**ProductCode**](productcode.md). Uma atualização requer uma [atualização importante](major-upgrades.md) para alterar o **ProductCode**. Uma atualização secundária pode ser usada para adicionar novos recursos e componentes, mas não pode reorganizar a árvore de componentes de recursos. As atualizações secundárias fornecem diferenciação de produtos sem realmente definir um produto diferente. Uma atualização pequena típica inclui todas as correções nas pequenas atualizações anteriores combinadas em um patch. Uma atualização secundária também é comumente conhecida como atualização de service pack (SP). Para obter mais informações sobre quais atualizações não exigem a alteração do **ProductCode** , consulte [alterando o código do produto](changing-the-product-code.md).

Uma atualização secundária altera a propriedade [**ProductVersion**](productversion.md) . Alterar a versão do produto do aplicativo significa que as diferentes atualizações têm um pedido. Por exemplo, se um patch existisse para atualizar o v 9,0 para v 9,1 e outro patch existisse para aplicar patches v 9,1 a v 9,2, o instalador poderá impor a ordem correta verificando a versão do produto antes de aplicar o patch. Isso também impede que o patch v 9,1 a v 9,2 seja aplicado a v 9,0. Para patches, essa ordenação é imposta por meio da versão do produto – bits de validação definidos nas transformações incluídas no [pacote de patch](patch-packages.md).

Uma atualização secundária e uma pequena atualização são diferentes, pois uma atualização secundária altera o código do pacote e a versão do produto. Consulte [pequenas atualizações](small-updates.md) para obter diretrizes sobre os tipos de atualizações que podem ser manipuladas por uma pequena atualização ou uma atualização secundária. As atualizações secundárias são enviadas como um pacote de instalação completo do produto ou como um [pacote de patch](patch-packages.md). No entanto, uma atualização secundária não pode usar um rótulo de volume diferente para a nova versão.

Para obter informações sobre como aplicar uma atualização secundária, consulte os seguintes tópicos:

-   [Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md)
-   [Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md)

 

 



