---
title: Adicionando uma referência a um projeto Visual Basic
description: Adicionando uma referência a um projeto Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292035"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Adicionando uma referência a um projeto Visual Basic

O procedimento a seguir descreve como adicionar uma referência a um objeto COM para um projeto Visual Basic. Em seguida, seu aplicativo pode usar as classes desse objeto.

Quando você adiciona um objeto como uma referência, só pode usar a biblioteca de tipos fornecida pelo controle ou a biblioteca de tipos "RAW". Por outro lado, a adição de um controle como um componente também expõe as propriedades e os métodos do extensor Visual Basic como se eles fossem parte do controle.

**Para fazer uma referência de Visual Basic a um componente**

1.  No menu **Projeto**, clique em **Referências**.
2.  Clique para marcar a caixa de seleção ao lado do componente que você deseja adicionar. Se o componente não estiver listado, localize o arquivo. dll ou. ocx usando **procurar**.
3.  Clique em **OK**.

O componente agora faz parte do projeto. Seu aplicativo pode criar instâncias de classe usando a **nova** palavra-chave.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando um componente a um projeto Visual Basic](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Convertendo para Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




