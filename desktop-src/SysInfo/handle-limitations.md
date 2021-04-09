---
description: Alguns objetos dão suporte a apenas um identificador de cada vez.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitações de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171471"
---
# <a name="handle-limitations"></a><span data-ttu-id="43772-103">Limitações de identificador</span><span class="sxs-lookup"><span data-stu-id="43772-103">Handle Limitations</span></span>

<span data-ttu-id="43772-104">Alguns objetos dão suporte a apenas um identificador de cada vez.</span><span class="sxs-lookup"><span data-stu-id="43772-104">Some objects support only one handle at a time.</span></span> <span data-ttu-id="43772-105">O sistema fornece o identificador quando um aplicativo cria o objeto e invalida o identificador quando o aplicativo destrói o objeto.</span><span class="sxs-lookup"><span data-stu-id="43772-105">The system provides the handle when an application creates the object and invalidates the handle when the application destroys the object.</span></span> <span data-ttu-id="43772-106">Outros objetos dão suporte a vários identificadores para um único objeto.</span><span class="sxs-lookup"><span data-stu-id="43772-106">Other objects support multiple handles to a single object.</span></span> <span data-ttu-id="43772-107">O sistema operacional remove automaticamente o objeto da memória depois que o último identificador para o objeto é fechado.</span><span class="sxs-lookup"><span data-stu-id="43772-107">The operating system automatically removes the object from memory after the last handle to the object is closed.</span></span>

<span data-ttu-id="43772-108">O número total de identificadores abertos no sistema é limitado apenas pela quantidade de memória disponível.</span><span class="sxs-lookup"><span data-stu-id="43772-108">The total number of open handles in the system is limited only by the amount of memory available.</span></span> <span data-ttu-id="43772-109">Alguns tipos de objeto dão suporte a um número limitado de identificadores por sessão ou por processo.</span><span class="sxs-lookup"><span data-stu-id="43772-109">Some object types support a limited number of handles per session or per process.</span></span>

 

 



