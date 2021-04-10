---
title: Anotação do servidor
description: Esta seção fornece informações sobre como usar a anotação do servidor.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005128"
---
# <a name="server-annotation"></a>Anotação do servidor

Esta seção fornece informações sobre como usar a anotação do servidor.

## <a name="summary"></a>Resumo

Você define uma classe que implementa [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), cria uma instância dela e informa ao sistema que você deseja que ela substitua propriedades específicas em elementos específicos da interface do usuário. Quando um cliente solicita uma das propriedades de um dos elementos da interface do usuário, seu objeto é chamado e recebe uma oportunidade de fornecer um valor. Se o objeto retornar um valor, esse valor será passado de volta para o cliente. Se o objeto não retornar um valor, o valor padrão desse elemento de interface do usuário será retornado ao cliente.

## <a name="when-to-use-this-technique"></a>Quando usar essa técnica

Use essa técnica quando desejar substituir as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um objeto. Essa técnica é muito mais simples do que as técnicas de **IAccessible** anteriores. Para obter mais informações, consulte [alternativas à anotação dinâmica](alternatives-to-dynamic-annotation.md).

Você não pode usar a anotação de servidor para alterar a estrutura de objetos expostos. Para alterar a estrutura de um objeto, você deve implementar um ponteiro de interface de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.

Para obter mais informações sobre a anotação do servidor, consulte os seguintes tópicos:

-   [Usando a anotação do servidor](using-server-annotation.md)
-   [Exemplo de anotação do servidor](server-annotation-sample.md)

 

 




