---
title: Guia de programação wpd
description: Este guia de programação se concentra em como as tarefas de exemplo são realizadas usando as interfaces WPD e os métodos encontrados nas interfaces.
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13d50942c28cd4937d27a745d61d7a30a01a15
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409859"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="51a63-103">Guia de programação wpd</span><span class="sxs-lookup"><span data-stu-id="51a63-103">WPD programming guide</span></span>

<span data-ttu-id="51a63-104">A origem principal deste guia de programação é um exemplo que acompanha o SDK (Kit de Desenvolvimento de Software) WPD (Dispositivos Portáteis do Windows).</span><span class="sxs-lookup"><span data-stu-id="51a63-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="51a63-105">Este exemplo, chamado WpdApiSample.exe, consiste em sete módulos .cpp.</span><span class="sxs-lookup"><span data-stu-id="51a63-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="51a63-106">Seis desses módulos contêm o código que demonstra 26 tarefas que um aplicativo pode realizar usando a API (interface de programação de aplicativo) WPD.</span><span class="sxs-lookup"><span data-stu-id="51a63-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="51a63-107">As exceções ao acima são os tópicos que descrevem: tarefas de serviço do dispositivo, o menu de contexto e as extensões da folha de propriedades; esses tópicos não foram retirados de WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="51a63-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="51a63-108">As tarefas de serviço do dispositivo são baseadas no exemplo chamado WpdServiceApiSample.</span><span class="sxs-lookup"><span data-stu-id="51a63-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="51a63-109">O menu de contexto e as extensões de folha de propriedades são snippets retirados de aplicativos que não são encaminhados com o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="51a63-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="51a63-110">As seções a seguir se concentram nas tarefas realizadas por esses exemplos e explicam como cada uma é realizada usando as interfaces WPD e vários métodos encontrados nessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="51a63-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51a63-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51a63-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a63-112">**Dispositivos Portáteis do Windows**</span><span class="sxs-lookup"><span data-stu-id="51a63-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
