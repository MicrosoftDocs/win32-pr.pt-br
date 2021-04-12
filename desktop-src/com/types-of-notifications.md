---
title: Tipos de notificações
description: Tipos de notificações
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364273"
---
# <a name="types-of-notifications"></a><span data-ttu-id="3f71e-103">Tipos de notificações</span><span class="sxs-lookup"><span data-stu-id="3f71e-103">Types of Notifications</span></span>

<span data-ttu-id="3f71e-104">As notificações se enquadram em três grupos: documento composto, dados e exibição.</span><span class="sxs-lookup"><span data-stu-id="3f71e-104">Notifications fall into three groups: compound document, data, and view.</span></span> <span data-ttu-id="3f71e-105">Um objeto envia notificações de documento composto em resposta a ser renomeado, salvo, fechado ou, no caso de um link, tendo sua origem de link renomeada.</span><span class="sxs-lookup"><span data-stu-id="3f71e-105">An object sends compound document notifications in response to being renamed, saved, closed or, in the case of a link, having its link source renamed.</span></span> <span data-ttu-id="3f71e-106">Como você deve esperar, os objetos enviam notificações de dados em resposta a alterações em seus dados e enviamos notificações de exibição em resposta às alterações em sua apresentação.</span><span class="sxs-lookup"><span data-stu-id="3f71e-106">As you would expect, objects send data notifications in response to changes in their data and send view notifications in response to changes in their presentation.</span></span> <span data-ttu-id="3f71e-107">Os aplicativos de contêiner devem ser registrados separadamente para cada um desses tipos de notificação, mas todos podem ser tratados por um único coletor de consultoria.</span><span class="sxs-lookup"><span data-stu-id="3f71e-107">Container applications must register separately for each of these notification types, but all can be handled by a single advisory sink.</span></span>

<span data-ttu-id="3f71e-108">Todos os contêineres, o manipulador de objeto e o objeto vinculado são registrados para notificações de documento composto.</span><span class="sxs-lookup"><span data-stu-id="3f71e-108">All containers, the object handler, and the linked object register for compound document notifications.</span></span> <span data-ttu-id="3f71e-109">O contêiner típico também se registra para exibir notificações.</span><span class="sxs-lookup"><span data-stu-id="3f71e-109">The typical container also registers for view notifications.</span></span> <span data-ttu-id="3f71e-110">As notificações de dados geralmente são enviadas para o objeto vinculado e o manipulador de objetos.</span><span class="sxs-lookup"><span data-stu-id="3f71e-110">Data notifications are usually sent to both the linked object and object handler.</span></span> <span data-ttu-id="3f71e-111">Um contêiner de propósito especial, como um que renderiza os dados em si, pode se beneficiar do recebimento de notificações de dados em vez de exibir notificações.</span><span class="sxs-lookup"><span data-stu-id="3f71e-111">A special purpose container, such as one that renders the data itself, might benefit from receiving data notifications instead of view notifications.</span></span> <span data-ttu-id="3f71e-112">Por exemplo, um contêiner de gráfico incorporado com um link para uma tabela pode se registrar para notificações de dados.</span><span class="sxs-lookup"><span data-stu-id="3f71e-112">For example, an embedded chart container with a link to a table can register for data notifications.</span></span> <span data-ttu-id="3f71e-113">Como uma alteração na tabela afeta o gráfico, o recebimento de uma notificação de dados direcionaria o contêiner para obter os novos dados tabulares.</span><span class="sxs-lookup"><span data-stu-id="3f71e-113">Because a change to the table affects the chart, the receipt of a data notification would direct the container to get the new tabular data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f71e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f71e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f71e-115">Notificações</span><span class="sxs-lookup"><span data-stu-id="3f71e-115">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 




