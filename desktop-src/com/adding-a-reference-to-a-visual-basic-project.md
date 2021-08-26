---
title: Adicionando uma referência a um Visual Basic Project
description: Adicionando uma referência a um Visual Basic Project
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deba6030e57839e0f436239790aaa6f02e2fb29981ce021b0de2d09af2acdff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097066"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Adicionando uma referência a um Visual Basic Project

O procedimento a seguir descreve como adicionar uma referência a um objeto COM a um Visual Basic projeto. Seu aplicativo pode usar as classes desse objeto.

Ao adicionar um objeto como referência, você só pode usar a biblioteca de tipos fornecida pelo controle ou a biblioteca de tipos "brutos". Por outro lado, adicionar um controle como um componente também expõe as Visual Basic e métodos do extensor como se eles fossem parte do controle.

**Para fazer uma Visual Basic referência a um componente**

1.  No menu **Projeto**, clique em **Referências**.
2.  Clique para marcar a caixa de seleção ao lado do componente que você deseja adicionar. Se o componente não estiver listado, localize o arquivo .dll ou .ocx usando **Procurar**.
3.  Clique em **OK**.

O componente agora faz parte do projeto. Seu aplicativo pode criar instâncias de classe usando a **palavra-chave** New.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando um componente a um Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Traduzindo para Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




