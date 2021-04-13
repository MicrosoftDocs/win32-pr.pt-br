---
title: Run-Time vincular a Wtsapi32.dll
description: Seu aplicativo pode usar a API Serviços de Área de Trabalho Remota para vincular dinamicamente ao Wtsapi32.dll em tempo de execução. Para fazer isso, seu aplicativo deve chamar a função LoadLibrary para carregar Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366407"
---
# <a name="run-time-linking-to-wtsapi32dll"></a><span data-ttu-id="83dc6-104">Run-Time vincular a Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="83dc6-104">Run-Time linking to Wtsapi32.dll</span></span>

<span data-ttu-id="83dc6-105">Se o seu aplicativo for executado em um ambiente que não seja um Serviços de Área de Trabalho Remota ambiente, mas você quiser que seu aplicativo forneça funcionalidade adicional quando ele for executado em um ambiente de Serviços de Área de Trabalho Remota, o aplicativo poderá usar a API do Serviços de Área de Trabalho Remota para implementar a funcionalidade adicional e vincular dinamicamente a Wtsapi32.dll em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="83dc6-105">If your application runs in an environment that is not a Remote Desktop Services environment, but you want your application to provide additional functionality when it does run in a Remote Desktop Services environment, the application can use the Remote Desktop Services API to implement the additional functionality, and dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="83dc6-106">Para fazer isso, seu aplicativo deve chamar a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="83dc6-106">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span> <span data-ttu-id="83dc6-107">Se a chamada **LoadLibrary** falhar, seu aplicativo poderá ser executado usando sua funcionalidade básica.</span><span class="sxs-lookup"><span data-stu-id="83dc6-107">If the **LoadLibrary** call fails, your application can run using its basic functionality.</span></span> <span data-ttu-id="83dc6-108">Se **LoadLibrary** for executado com sucesso, seu aplicativo poderá chamar a função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar ponteiros para as funções de serviços de área de trabalho remota que você deseja chamar.</span><span class="sxs-lookup"><span data-stu-id="83dc6-108">If **LoadLibrary** succeeds, your application can call the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve pointers to the Remote Desktop Services functions that you want to call.</span></span>

<span data-ttu-id="83dc6-109">Se seu aplicativo for destinado apenas a um ambiente de Serviços de Área de Trabalho Remota, a vinculação dinâmica não será necessária.</span><span class="sxs-lookup"><span data-stu-id="83dc6-109">If your application is intended only for a Remote Desktop Services environment, dynamic linking is not necessary.</span></span> <span data-ttu-id="83dc6-110">Nesse caso, você pode incluir Wtsapi32. h e vincular com Wtsapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="83dc6-110">In this case, you can include Wtsapi32.h and link with Wtsapi32.lib.</span></span> <span data-ttu-id="83dc6-111">Em seguida, se seu aplicativo for iniciado em um ambiente diferente de Serviços de Área de Trabalho Remota, ele será encerrado porque Wtsapi32.dll não está presente.</span><span class="sxs-lookup"><span data-stu-id="83dc6-111">Then, if your application starts up in an environment other than Remote Desktop Services, it will exit because Wtsapi32.dll is not present.</span></span>

<span data-ttu-id="83dc6-112">Para obter informações sobre como determinar se seu aplicativo está sendo executado em um ambiente de Serviços de Área de Trabalho Remota, consulte [detectando o ambiente de serviços de área de trabalho remota](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="83dc6-112">For information about determining whether your application is running in a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83dc6-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83dc6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83dc6-114">Diretrizes gerais de programação</span><span class="sxs-lookup"><span data-stu-id="83dc6-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> </dl>

 

 