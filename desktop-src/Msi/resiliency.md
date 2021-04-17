---
description: A resiliência é a capacidade de um aplicativo de se recuperar normalmente de situações em que um componente vital está faltando ou foi substituído por uma versão incompatível.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resiliência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757112"
---
# <a name="resiliency"></a><span data-ttu-id="ede19-103">Resiliência</span><span class="sxs-lookup"><span data-stu-id="ede19-103">Resiliency</span></span>

<span data-ttu-id="ede19-104">A resiliência é a capacidade de um aplicativo de se recuperar normalmente de situações em que um componente vital está faltando ou foi substituído por uma versão incompatível.</span><span class="sxs-lookup"><span data-stu-id="ede19-104">Resiliency is the ability of an application to recover gracefully from situations in which a vital component is missing, or has been replaced by an incompatible version.</span></span> <span data-ttu-id="ede19-105">Ao criar um pacote de instalação e usar as [funções do instalador](installer-functions.md), os desenvolvedores podem usar o Windows Installer para produzir aplicativos resilientes capazes de se recuperar dessas situações.</span><span class="sxs-lookup"><span data-stu-id="ede19-105">By authoring an installation package and using the [Installer Functions](installer-functions.md), developers can use the Windows Installer to produce resilient applications capable of recovering from such situations.</span></span>

-   <span data-ttu-id="ede19-106">Use a lista de origem do instalador para aumentar a resiliência de aplicativos que dependem de recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="ede19-106">Use the installer's source list to increase the resiliency of applications that rely on network resources.</span></span> <span data-ttu-id="ede19-107">Para obter mais informações, consulte [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="ede19-107">For more information, see [Source Resiliency](source-resiliency.md).</span></span>
-   <span data-ttu-id="ede19-108">Use a API do instalador para verificar se um recurso, componente, arquivo ou versão de arquivo vital está instalado.</span><span class="sxs-lookup"><span data-stu-id="ede19-108">Use the installer's API to check whether a vital feature, component, file, or file version is installed.</span></span>
-   <span data-ttu-id="ede19-109">Use a API do instalador para verificar o caminho para um componente em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ede19-109">Use the installer's API to check the path to a component at run time.</span></span> <span data-ttu-id="ede19-110">Isso reduz a dependência do aplicativo em caminhos de arquivo estáticos, que normalmente são diferentes entre computadores.</span><span class="sxs-lookup"><span data-stu-id="ede19-110">This reduces your application's dependency on static file paths, which commonly differ between computers.</span></span>
-   <span data-ttu-id="ede19-111">Use o instalador para reinstalar atalhos danificados, entradas de registro e outros componentes sem precisar executar a instalação novamente.</span><span class="sxs-lookup"><span data-stu-id="ede19-111">Use the installer to reinstall damaged shortcuts, registry entries, and other components without having to rerun setup.</span></span>
-   <span data-ttu-id="ede19-112">Aumente a resiliência da instalação do produto, deixando o recurso de reversão do instalador habilitado.</span><span class="sxs-lookup"><span data-stu-id="ede19-112">Increase the resiliency of your product's installation by leaving the rollback capability of the installer enabled.</span></span> <span data-ttu-id="ede19-113">Para obter mais informações, consulte [Rollback Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="ede19-113">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



