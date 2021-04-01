---
description: Os provedores de componentes compartilhados devem considerar tornar seu componente disponível como um assembly lado a lado se um ou mais dos casos a seguir forem verdadeiros.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Você deve fornecer um componente compartilhado como um assembly lado a lado?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829771"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>Você deve fornecer um componente compartilhado como um assembly lado a lado?

Os provedores de componentes compartilhados devem considerar tornar seu componente disponível como um assembly lado a lado se um ou mais dos seguintes itens forem verdadeiros:

-   O componente expõe uma interface de programação de aplicativo avançada que é usada por muitos aplicativos. Por exemplo, um componente como o MSHTML, que permite que aplicativos C e C++ acessem o modelo de objeto HTML dinâmico (DHTML).
-   O componente já está sendo compartilhado por vários aplicativos. Por exemplo, um componente como o COMCTL32, que fornece aos aplicativos acesso aos controles comuns.
-   O componente é um novo componente.
-   O componente é um componente de modo de usuário e não um driver de dispositivo.

Nem todo componente é um candidato adequado para um assembly lado a lado. Um componente não é um candidato adequado para um assembly lado a lado se qualquer uma das seguintes opções for verdadeira:

-   O componente manipula a comunicação entre aplicativos. Por exemplo, partes de OLE32 não fariam um bom assembly lado a lado porque você não desejaria ter duas versões diferentes das partes que coordenam a comunicação entre os aplicativos executados no seu sistema.
-   O componente gerencia um dispositivo físico ou virtual para o sistema. Por exemplo, um driver de dispositivo para um spooler de impressão.

Em alguns casos, pode ser possível para o desenvolvedor do componente recriar um componente existente a fim de torná-lo adequado para publicação como um assembly lado a lado. Para obter mais informações, consulte [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md).

 

 



