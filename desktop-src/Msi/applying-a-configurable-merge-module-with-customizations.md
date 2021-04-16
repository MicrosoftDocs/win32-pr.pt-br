---
description: Siga as diretrizes gerais para aplicar os módulos de mesclagem descritos em aplicando módulos de mesclagem.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Aplicando um módulo de mesclagem configurável com personalizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750254"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a><span data-ttu-id="8c7fb-103">Aplicando um módulo de mesclagem configurável com personalizações</span><span class="sxs-lookup"><span data-stu-id="8c7fb-103">Applying a Configurable Merge Module with Customizations</span></span>

<span data-ttu-id="8c7fb-104">Siga as diretrizes gerais para aplicar os módulos de mesclagem descritos em [aplicando módulos de mesclagem](applying-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="8c7fb-104">Follow the general guidelines for applying merge modules described in [Applying Merge Modules](applying-merge-modules.md).</span></span> <span data-ttu-id="8c7fb-105">Além disso, os consumidores de módulo de mesclagem devem fazer o seguinte para configurar um módulo de mesclagem no momento da instalação:</span><span class="sxs-lookup"><span data-stu-id="8c7fb-105">In addition, merge module consumers must do the following to configure a merge module at the time of installation:</span></span>

-   <span data-ttu-id="8c7fb-106">Use um módulo de mesclagem que seja criado para ter configurações configuráveis.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-106">Use a merge module that is authored to have configurable settings.</span></span> <span data-ttu-id="8c7fb-107">Para obter mais informações, consulte [criando um módulo de mesclagem que pode ser configurado pelo usuário final](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span><span class="sxs-lookup"><span data-stu-id="8c7fb-107">For more information, see [Creating a Merge Module that Can Be Configured by the End-User](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span></span>
-   <span data-ttu-id="8c7fb-108">Use uma ferramenta de mesclagem e configuração que chama Mergemod.dll versão 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-108">Use a merge and configuration tool that calls Mergemod.dll version 2.0 or later.</span></span> <span data-ttu-id="8c7fb-109">As versões anteriores do Mergmod.dll não podem definir as configurações do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-109">Earlier versions of Mergmod.dll cannot configure merge module settings.</span></span> <span data-ttu-id="8c7fb-110">Os autores devem criar módulos de mesclagem que forneçam valores padrão e sejam compatíveis com versões anteriores do Mergmod.dll.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-110">Authors should create merge modules that provide default values and are compatible with earlier versions of Mergmod.dll.</span></span>
-   <span data-ttu-id="8c7fb-111">Forneça informações de personalização quando solicitado pela ferramenta de cliente de configuração.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-111">Provide customization information when prompted by the configuration client tool.</span></span> <span data-ttu-id="8c7fb-112">Os autores devem criar módulos de mesclagem que usam valores padrão quando um usuário recusa a fornecer informações.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-112">Authors should create merge modules that use default values when a user declines to provide information.</span></span>

 

 



