---
description: A infraestrutura de pares não garante a ordem de recebimento e processamento de registros.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Dependências de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770268"
---
# <a name="record-dependencies"></a><span data-ttu-id="acff7-103">Dependências de registro</span><span class="sxs-lookup"><span data-stu-id="acff7-103">Record Dependencies</span></span>

<span data-ttu-id="acff7-104">A infraestrutura de pares não garante a ordem de recebimento e processamento de registros.</span><span class="sxs-lookup"><span data-stu-id="acff7-104">The Peer Infrastructure does not guarantee the order for receiving and processing records.</span></span> <span data-ttu-id="acff7-105">Se seu aplicativo tiver dependências de registro, o que significa que o processamento ou a validação de um registro depende de outro registro, o aplicativo deverá ser capaz de lidar com situações em que os registros possam ser recebidos em uma ordem arbitrária e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="acff7-105">If your application has record dependencies, which means that the processing or validation of one record relies on another record, then your application must be able to handle situations when records might be received in an arbitrary and unpredictable order.</span></span> <span data-ttu-id="acff7-106">Por exemplo, um aplicativo de chat pode ter dois tipos de registros: um registro que contém informações sobre um usuário específico e um registro que contém uma mensagem de chat que se refere ao registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="acff7-106">For example, a chat application may have two types of records: a record that contains information about a specific user, and a record that contains a chat message that refers to the user record.</span></span>

<span data-ttu-id="acff7-107">Um aplicativo deve ser capaz de lidar com a situação quando um registro de mensagem de chat é recebido antes do registro de usuário para a mensagem de chat.</span><span class="sxs-lookup"><span data-stu-id="acff7-107">An application must be able to handle the situation when a chat message record is received before the user record for the chat message.</span></span> <span data-ttu-id="acff7-108">Uma maneira de lidar com a situação é aguardar o registro do usuário usando uma **lista de espera**, ou um cache e um temporizador.</span><span class="sxs-lookup"><span data-stu-id="acff7-108">One way to handle the situation is to wait for the user record by using a **stand-by list**, or a cache and timer.</span></span> <span data-ttu-id="acff7-109">O aplicativo pode examinar periodicamente cada registro na lista ou no cache e, em seguida, manipular a situação quando o registro de usuário necessário é recebido.</span><span class="sxs-lookup"><span data-stu-id="acff7-109">The application can periodically examine each record in the list or cache, and then handle the situation when the required user record is received.</span></span>

<span data-ttu-id="acff7-110">Para lidar com dependências de registro, um aplicativo bem projetado consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="acff7-110">To handle record dependencies, a well-designed application consists of the following:</span></span>

-   <span data-ttu-id="acff7-111">Sempre verifica dependências de registro antes de executar uma ação.</span><span class="sxs-lookup"><span data-stu-id="acff7-111">Always checks for record dependencies before performing an action.</span></span>
-   <span data-ttu-id="acff7-112">Prevê condições que podem ocorrer quando registros são recebidos em uma ordem inesperada e, em seguida, manipula a situação.</span><span class="sxs-lookup"><span data-stu-id="acff7-112">Anticipates conditions that might occur when records are received in an unexpected order, and then handles the situation.</span></span>

 

 



