---
title: Propriedades e métodos
description: Como qualquer objeto OLE, um controle fornece grande parte de sua funcionalidade por meio de um conjunto de interfaces de entrada com propriedades e métodos.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52dae30453089f235a4e70d7896569ebefcdff9f7f2419b5fc54af88b8563d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047884"
---
# <a name="properties-and-methods"></a>Propriedades e métodos

Como qualquer objeto OLE, um controle fornece grande parte de sua funcionalidade por meio de um conjunto de interfaces de entrada com propriedades e métodos.

Um controle expõe propriedades e métodos por meio da automação OLE para que os contêineres possam acessá-los sob o controle de uma linguagem de programação fornecida pelo contêiner.

Para dar suporte ao acesso a propriedades por meio de uma interface do usuário, um controle fornece páginas de propriedades, suporte para PROPRIEDADES OLEIVERB, navegação por propriedade e associação de dados por meio de notficações de alteração \_ de propriedade.

-   Por meio de páginas de propriedades, um controle pode exibir suas propriedades, independentemente de seu contêiner, se necessário.
-   Ao dar suporte a PROPRIEDADES OLEIVERB, o \_ item Propriedades é exibido no menu do contêiner. Em seguida, o usuário final pode selecionar o item **Propriedades** para exibir as páginas de propriedades do controle e modificar as propriedades.
-   A navegação por propriedade dá suporte a um contêiner que pode exibir as propriedades do controle como parte de uma folha de propriedades maior que pode incluir propriedades de vários controles no contêiner.
-   Por meio da notificação de alteração de propriedade, um controle pode notificar um cliente de que suas propriedades têm alteração, permitindo que o cliente tome as ações necessárias como resultado.

Para obter mais informações, consulte estes tópicos:

-   [Propriedades do controle](control-properties.md)
-   [Métodos de controle](control-methods.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ActiveX Controles](activex-controls.md)
</dt> <dt>

[Páginas de propriedades e folhas de propriedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




