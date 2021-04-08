---
description: A lista de origem usada mais recentemente (MRU) permanece residente no sistema de usuários.
ms.assetid: 010f8f88-999e-4dde-bffb-ac1a07256d55
title: Sobre a lista de origem do MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062624057e7dd1a083ebf0eb152200fd3a7241b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920842"
---
# <a name="about-the-mru-source-list"></a><span data-ttu-id="8d4b1-103">Sobre a lista de origem do MRU</span><span class="sxs-lookup"><span data-stu-id="8d4b1-103">About the MRU Source List</span></span>

<span data-ttu-id="8d4b1-104">A lista de origem usada mais recentemente (MRU) permanece residente no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d4b1-104">The most recently used (MRU) source list remains resident on the user's system.</span></span> <span data-ttu-id="8d4b1-105">As funções de instalação manipulam internamente a criação de novas listas de origem e sua localização na máquina do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d4b1-105">The setup functions internally handle the creation of new source lists and their location on the user's machine.</span></span> <span data-ttu-id="8d4b1-106">As funções de instalação usam essa lista para armazenar informações sobre caminhos de origem usados em instalações anteriores.</span><span class="sxs-lookup"><span data-stu-id="8d4b1-106">The setup functions use this list to store information about source paths used in previous installations.</span></span>

<span data-ttu-id="8d4b1-107">Você pode usar essas informações ao solicitar ao usuário um caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="8d4b1-107">You can use this information when prompting the user for a source path.</span></span> <span data-ttu-id="8d4b1-108">Por exemplo, você pode criar uma lista suspensa das conexões de rede usadas como caminhos de origem em instalações anteriores.</span><span class="sxs-lookup"><span data-stu-id="8d4b1-108">For example, you could create a drop-down list of the network connections used as source paths in previous installations.</span></span>

<span data-ttu-id="8d4b1-109">Dependendo de suas permissões, você pode criar uma lista de usuários, uma que seja específica a um usuário específico, ou uma lista do sistema, uma que seja a mesma para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="8d4b1-109">Depending on your permissions, you can create a user list, one that is specific to a particular user, or a system list, one that is the same for all users.</span></span> <span data-ttu-id="8d4b1-110">Além das listas de origem do sistema e do usuário, você pode criar uma lista de origem temporária que é descartada quando o aplicativo de instalação é encerrado.</span><span class="sxs-lookup"><span data-stu-id="8d4b1-110">In addition to system and user source lists you can create a temporary source list that is discarded when the setup application exits.</span></span>

 

 



