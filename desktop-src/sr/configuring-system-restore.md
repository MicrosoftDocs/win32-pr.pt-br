---
title: Configurando a restauração do sistema
description: A restauração do sistema usa Instrumentação de Gerenciamento do Windows (WMI) para fornecer uma maneira programável de configurar e usar sua funcionalidade. Ele expõe duas classes, SystemRestore e SystemRestoreConfig, no namespace root \\ padrão.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366253"
---
# <a name="configuring-system-restore"></a><span data-ttu-id="24271-104">Configurando a restauração do sistema</span><span class="sxs-lookup"><span data-stu-id="24271-104">Configuring System Restore</span></span>

<span data-ttu-id="24271-105">A restauração do sistema usa [Instrumentação de gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para fornecer uma maneira programável de configurar e usar sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="24271-105">System Restore uses [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to provide a scriptable way of configuring and using its functionality.</span></span> <span data-ttu-id="24271-106">Ele expõe duas classes, [**SystemRestore**](systemrestore.md) e [**SystemRestoreConfig**](systemrestoreconfig.md), no namespace root \\ padrão.</span><span class="sxs-lookup"><span data-stu-id="24271-106">It exposes two classes, [**SystemRestore**](systemrestore.md) and [**SystemRestoreConfig**](systemrestoreconfig.md), in the root\\default namespace.</span></span>

<span data-ttu-id="24271-107">A classe [**SystemRestore**](systemrestore.md) fornece métodos para as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="24271-107">The [**SystemRestore**](systemrestore.md) class provides methods for the following tasks:</span></span>

-   <span data-ttu-id="24271-108">Desabilitando e habilitando o monitoramento</span><span class="sxs-lookup"><span data-stu-id="24271-108">Disabling and enabling monitoring</span></span>
-   <span data-ttu-id="24271-109">Listando pontos de restauração disponíveis</span><span class="sxs-lookup"><span data-stu-id="24271-109">Listing available restore points</span></span>
-   <span data-ttu-id="24271-110">Iniciando uma restauração no sistema local</span><span class="sxs-lookup"><span data-stu-id="24271-110">Initiating a restore on the local system</span></span>
-   <span data-ttu-id="24271-111">Recuperando o status da última restauração do sistema</span><span class="sxs-lookup"><span data-stu-id="24271-111">Retrieving the status of the last system restore</span></span>

<span data-ttu-id="24271-112">A classe [**SystemRestoreConfig**](systemrestoreconfig.md) fornece propriedades para controlar a frequência da criação do ponto de restauração agendado e a quantidade de espaço em disco consumida pela restauração do sistema em cada unidade.</span><span class="sxs-lookup"><span data-stu-id="24271-112">The [**SystemRestoreConfig**](systemrestoreconfig.md) class provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed by System Restore on each drive.</span></span>

<span data-ttu-id="24271-113">Ambas as classes podem ser acessadas remotamente usando técnicas padrão de WMI.</span><span class="sxs-lookup"><span data-stu-id="24271-113">Both classes can be accessed remotely using standard WMI techniques.</span></span> <span data-ttu-id="24271-114">Para obter uma descrição completa do WMI, consulte [Instrumentação de gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="24271-114">For a complete description of WMI, see [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

 

 