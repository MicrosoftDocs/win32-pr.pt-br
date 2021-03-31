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
# <a name="properties-and-methods"></a><span data-ttu-id="0d589-103">Propriedades e métodos</span><span class="sxs-lookup"><span data-stu-id="0d589-103">Properties and Methods</span></span>

<span data-ttu-id="0d589-104">Como qualquer objeto OLE, um controle fornece grande parte de sua funcionalidade por meio de um conjunto de interfaces de entrada com propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="0d589-104">Like any OLE object, a control provides much of its functionality through a set of incoming interfaces with properties and methods.</span></span>

<span data-ttu-id="0d589-105">Um controle expõe propriedades e métodos por meio da automação OLE para que os contêineres possam acessá-los sob o controle de uma linguagem de programação fornecida pelo contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d589-105">A control exposes properties and methods through OLE automation so that containers can access them under the control of a container-supplied programming language.</span></span>

<span data-ttu-id="0d589-106">Para dar suporte ao acesso às propriedades por meio de uma interface do usuário, um controle fornece páginas de propriedades, suporte para \_ Propriedades OLEIVERB, navegação por propriedade e vinculação de dados por meio de alteração de propriedade notificações.</span><span class="sxs-lookup"><span data-stu-id="0d589-106">To support access to properties through a user interface, a control provides property pages, support for OLEIVERB\_PROPERTIES, per property browsing, and data binding through property change notfications.</span></span>

-   <span data-ttu-id="0d589-107">Por meio de páginas de propriedades, um controle pode exibir suas propriedades, independentemente de seu contêiner, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0d589-107">Through property pages a control can display its properties, independent of its container, if necessary.</span></span>
-   <span data-ttu-id="0d589-108">Ao dar suporte \_ a Propriedades OLEIVERB, o item Propriedades é exibido no menu do contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d589-108">By supporting OLEIVERB\_PROPERTIES, the Properties item is displayed on the container's menu.</span></span> <span data-ttu-id="0d589-109">Em seguida, o usuário final pode selecionar o item de **Propriedades** para exibir as páginas de propriedades do controle e modificar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d589-109">Then, the end user can select the **Properties** item to view the control's property pages and modify the properties.</span></span>
-   <span data-ttu-id="0d589-110">A navegação por Propriedade dá suporte a um contêiner que pode exibir as propriedades do controle como parte de uma folha de propriedades maior que pode incluir propriedades de vários controles no contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d589-110">Per property browsing supports a container that can display the control's properties as part of a larger property sheet that may include properties from several controls in the container.</span></span>
-   <span data-ttu-id="0d589-111">Por meio da notificação de alteração de propriedade, um controle pode notificar um cliente de que suas propriedades foram alteradas, permitindo que o cliente execute todas as ações necessárias como resultado.</span><span class="sxs-lookup"><span data-stu-id="0d589-111">Through property change notification, a control can notify a client that its properties have change, allowing the client to take any necessary actions as a result.</span></span>

<span data-ttu-id="0d589-112">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="0d589-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="0d589-113">Propriedades de controle</span><span class="sxs-lookup"><span data-stu-id="0d589-113">Control Properties</span></span>](control-properties.md)
-   [<span data-ttu-id="0d589-114">Métodos de controle</span><span class="sxs-lookup"><span data-stu-id="0d589-114">Control Methods</span></span>](control-methods.md)

## <a name="related-topics"></a><span data-ttu-id="0d589-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d589-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d589-116">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="0d589-116">ActiveX Controls</span></span>](activex-controls.md)
</dt> <dt>

[<span data-ttu-id="0d589-117">Páginas de propriedades e folhas de propriedades</span><span class="sxs-lookup"><span data-stu-id="0d589-117">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




