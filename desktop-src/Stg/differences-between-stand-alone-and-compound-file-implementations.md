---
title: Diferenças entre implementações autônomas e de arquivo composto
description: A implementação autônoma das interfaces do conjunto de propriedades e a implementação do arquivo composto diferem de algumas maneiras.
ms.assetid: 650d4759-a58a-47a4-922d-5757e356cf56
keywords:
- IPropertyStorage Strctd STG, implementações
- IPropertyStorage Strctd STG, implementações, diferenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 988f8a9cfdaca0a131bedf98cd8ff10ae8b89525
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822533"
---
# <a name="differences-between-stand-alone-and-compound-file-implementations"></a>Diferenças entre implementações autônomas e de arquivo composto

A implementação autônoma das interfaces do conjunto de propriedades e a implementação do arquivo composto diferem de algumas maneiras. Na implementação de arquivo composto de fluxo, armazenamento, conjunto de propriedades e objetos de armazenamento de propriedades, as várias interfaces são coordenadas entre si porque compartilham uma implementação comum. Na implementação autônoma, as implementações de interface são distintas.

Como resultado, a implementação de arquivo composto lida com problemas de simultaneidade e sincroniza o objeto de conjunto de propriedades com o objeto de armazenamento ou de fluxo. Com a implementação autônoma, o cliente é responsável por lidar com problemas de simultaneidade e sincronização entre o objeto de armazenamento ou de fluxo e o conjunto de propriedades. Um cliente pode atender a esses requisitos seguindo duas regras simples. Primeiro, nunca manipule um conjunto de propriedades usando seu fluxo ou suas interfaces de armazenamento enquanto um objeto de armazenamento de propriedades está aberto nele. Em segundo lugar, sempre chame **Commit** em um objeto de armazenamento de propriedade antes de chamar **CopyTo**, **MoveElementTo** ou **Commit** em um objeto de armazenamento ancestral. Especificamente, os seguintes itens exigem a atenção do cliente:

-   Na implementação de arquivo composto, um único mecanismo fornece proteção de simultaneidade para o objeto de armazenamento e seus objetos de conjunto de propriedades associados. No entanto, na implementação autônoma, a implementação do objeto de armazenamento é separada da implementação do conjunto de propriedades e cada uma fornece seus próprios mecanismos de simultaneidade. Assim, na implementação autônoma, o cliente é responsável por manter a proteção de simultaneidade entre as duas implementações por meio de um mecanismo de exclusão mútua.
-   Na implementação do arquivo composto, as alterações nos conjuntos de propriedades são armazenadas em buffer em um cache de conjunto de propriedades. Em seguida, quando o método [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) é chamado no objeto de armazenamento, a implementação dos arquivos compostos libera automaticamente as alterações do conjunto de propriedades do buffer do conjunto de propriedades antes que o objeto de armazenamento seja confirmado. Portanto, as alterações de conjunto de propriedades são tornadas visíveis como parte da transação que está sendo confirmada.

    Na implementação autônoma, o cliente deve liberar explicitamente o buffer de conjunto de propriedades chamando [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) antes de chamar o método [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) no armazenamento. Como alternativa, o cliente pode usar o novo \_ valor sem buffer PROPSETFLAG na implementação autônoma para gravar diretamente no conjunto de propriedades, em vez de armazenar em cache as alterações no buffer interno do conjunto de propriedades. Se PROPSETFLAG sem \_ buffer for usado, as responsabilidades do cliente serão automaticamente atendidas. A implementação do arquivo composto não oferece suporte ao \_ valor sem buffer PROPSETFLAG. Para obter mais informações, consulte [**constantes PROPSETFLAG**](propsetflag-constants.md).

-   Assim como ocorre com os armazenamentos transacionados, a implementação do arquivo composto atualiza o conjunto de propriedades liberando seu buffer interno antes de executar uma chamada para [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) ou [**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). Assim, as alterações no conjunto de propriedades são refletidas no elemento de armazenamento copiado ou movido.

    Na implementação autônoma, o cliente deve liberar explicitamente o buffer do conjunto de propriedades chamando [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) antes de chamar [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) ou [**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). Como alternativa, o cliente pode usar o novo \_ valor sem buffer PROPSETFLAG para gravar diretamente no conjunto de propriedades em vez de armazenar em cache as alterações no buffer do conjunto de propriedades. Para obter mais informações, consulte [**constantes PROPSETFLAG**](propsetflag-constants.md).

 

 




