---
title: Propriedades e métodos
description: Como qualquer objeto OLE, um controle fornece grande parte de sua funcionalidade por meio de um conjunto de interfaces de entrada com propriedades e métodos.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005185"
---
# <a name="properties-and-methods"></a>Propriedades e métodos

Como qualquer objeto OLE, um controle fornece grande parte de sua funcionalidade por meio de um conjunto de interfaces de entrada com propriedades e métodos.

Um controle expõe propriedades e métodos por meio da automação OLE para que os contêineres possam acessá-los sob o controle de uma linguagem de programação fornecida pelo contêiner.

Para dar suporte ao acesso às propriedades por meio de uma interface do usuário, um controle fornece páginas de propriedades, suporte para \_ Propriedades OLEIVERB, navegação por propriedade e vinculação de dados por meio de alteração de propriedade notificações.

-   Por meio de páginas de propriedades, um controle pode exibir suas propriedades, independentemente de seu contêiner, se necessário.
-   Ao dar suporte \_ a Propriedades OLEIVERB, o item Propriedades é exibido no menu do contêiner. Em seguida, o usuário final pode selecionar o item de **Propriedades** para exibir as páginas de propriedades do controle e modificar as propriedades.
-   A navegação por Propriedade dá suporte a um contêiner que pode exibir as propriedades do controle como parte de uma folha de propriedades maior que pode incluir propriedades de vários controles no contêiner.
-   Por meio da notificação de alteração de propriedade, um controle pode notificar um cliente de que suas propriedades foram alteradas, permitindo que o cliente execute todas as ações necessárias como resultado.

Para mais informações, consulte os seguintes tópicos:

-   [Propriedades de controle](control-properties.md)
-   [Métodos de controle](control-methods.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> <dt>

[Páginas de propriedades e folhas de propriedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




