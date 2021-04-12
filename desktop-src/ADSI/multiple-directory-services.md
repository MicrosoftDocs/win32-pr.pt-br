---
title: Vários serviços de diretório
description: Um desafio de trabalhar em um ambiente de computação distribuído é identificar e localizar recursos como usuários, grupos, filas de impressão e documentos.
ms.assetid: 66929290-b830-4768-a2ae-604d1a9de5c4
ms.tgt_platform: multiple
keywords:
- ADSI de vários serviços de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2e174fc1b07564f1cca6c12093a289a0c865a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291792"
---
# <a name="multiple-directory-services"></a><span data-ttu-id="5c690-104">Vários serviços de diretório</span><span class="sxs-lookup"><span data-stu-id="5c690-104">Multiple Directory Services</span></span>

<span data-ttu-id="5c690-105">Um desafio de trabalhar em um ambiente de computação distribuído é identificar e localizar recursos como usuários, grupos, filas de impressão e documentos.</span><span class="sxs-lookup"><span data-stu-id="5c690-105">One challenge of working within a distributed computing environment is identifying and locating resources such as users, groups, print queues, and documents.</span></span> <span data-ttu-id="5c690-106">Um serviço de diretório é a parte de um ambiente de computação distribuído que fornece uma maneira de localizar e identificar os usuários e os recursos disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="5c690-106">A directory service is the part of a distributed computing environment that provides a way to locate and identify the users and resources available in the system.</span></span> <span data-ttu-id="5c690-107">Um serviço de diretório é como um diretório de telefone.</span><span class="sxs-lookup"><span data-stu-id="5c690-107">A directory service is like a phone directory.</span></span> <span data-ttu-id="5c690-108">Dado um nome para uma pessoa ou um recurso, ele fornece os dados necessários para acessar essa pessoa ou recurso.</span><span class="sxs-lookup"><span data-stu-id="5c690-108">Given a name for a person or a resource, it provides the data necessary to access that person or resource.</span></span> <span data-ttu-id="5c690-109">Você não precisa iniciar com dados de associação para acessar um recurso na rede.</span><span class="sxs-lookup"><span data-stu-id="5c690-109">You do not have to start with binding data to access a resource on the network.</span></span>

<span data-ttu-id="5c690-110">A maioria das empresas já tem muitos diretórios diferentes em vigor.</span><span class="sxs-lookup"><span data-stu-id="5c690-110">Most enterprises already have many different directories in place.</span></span> <span data-ttu-id="5c690-111">Por exemplo, sistemas operacionais de rede, sistemas de correio eletrônico e produtos de "groupware" têm seus próprios diretórios.</span><span class="sxs-lookup"><span data-stu-id="5c690-111">For example, network operating systems, electronic mail systems, and "groupware" products all have their own directories.</span></span> <span data-ttu-id="5c690-112">Muitos problemas surgem quando uma única empresa implanta vários diretórios.</span><span class="sxs-lookup"><span data-stu-id="5c690-112">Many issues arise when a single enterprise deploys multiple directories.</span></span> <span data-ttu-id="5c690-113">Esses problemas incluem usabilidade, consistência de dados, custo de desenvolvimento e custo de suporte, entre outros.</span><span class="sxs-lookup"><span data-stu-id="5c690-113">These issues include usability, data consistency, development cost, and support cost, among others.</span></span>

<span data-ttu-id="5c690-114">Esses problemas são abordados na ADSI, pois há um conjunto único, consistente e aberto de interfaces que podem ser usadas para gerenciar e usar qualquer serviço de diretório que tenha um provedor ADSI.</span><span class="sxs-lookup"><span data-stu-id="5c690-114">These issues are addressed in ADSI, in that there is provided a single, consistent, open set of interfaces that can be used for managing and using any directory service that has an ADSI provider.</span></span>

 

 




