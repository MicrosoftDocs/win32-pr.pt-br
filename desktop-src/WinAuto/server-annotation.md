---
title: Anotação do servidor
description: Esta seção fornece informações sobre como usar a anotação do servidor.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9438184cf68d4a0f819afcd7e5497e627a0982e0f9fd9784c8a3460ab5121a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052534"
---
# <a name="server-annotation"></a>Anotação do servidor

Esta seção fornece informações sobre como usar a anotação do servidor.

## <a name="summary"></a>Resumo

Você define uma classe que implementa [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), cria uma instância dela e diz ao sistema que deseja que ela substitua propriedades específicas em elementos específicos da interface do usuário. Quando um cliente solicita uma das propriedades de um dos elementos da interface do usuário, seu objeto é chamado e recebe uma oportunidade de fornecer um valor. Se o objeto retornar um valor, esse valor será passado de volta para o cliente. Se o objeto não retornar um valor, o valor padrão desse elemento de interface do usuário será retornado ao cliente.

## <a name="when-to-use-this-technique"></a>Quando usar essa técnica

Use essa técnica quando quiser substituir as [**propriedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um objeto . Essa técnica é muito mais simples do que as técnicas **de IAccessible** anteriores. Para obter mais informações, [consulte Alternativas à Anotação Dinâmica](alternatives-to-dynamic-annotation.md).

Não é possível usar a anotação de servidor para alterar a estrutura de objeto exposta. Para alterar a estrutura de um objeto, você deve implementar um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.

Para obter mais informações sobre a anotação do servidor, consulte os seguintes tópicos:

-   [Usando anotação de servidor](using-server-annotation.md)
-   [Exemplo de anotação de servidor](server-annotation-sample.md)

 

 




