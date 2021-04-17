---
description: Referência gerenciada para classes de comando WMI do Windows PowerShell
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: Referência gerenciada para classes de comando WMI do Windows PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760995"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a><span data-ttu-id="4b290-103">Referência gerenciada para classes de comando WMI do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b290-103">Managed Reference for WMI Windows PowerShell Command Classes</span></span>

<span data-ttu-id="4b290-104">O Windows PowerShell implementa a funcionalidade de Instrumentação de Gerenciamento do Windows (WMI) por meio de um conjunto de cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4b290-104">Windows PowerShell implements Windows Management Instrumentation (WMI) functionality through a set of cmdlets.</span></span> <span data-ttu-id="4b290-105">Você pode usar esses cmdlets para concluir as tarefas de ponta a ponta que são necessárias para gerenciar computadores locais e remotos.</span><span class="sxs-lookup"><span data-stu-id="4b290-105">You can use these cmdlets to complete the end-to-end tasks that are necessary to manage local and remote computers.</span></span>

<span data-ttu-id="4b290-106">Consulte [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4b290-106">See [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) for more information.</span></span>

## <a name="wmi-powershell-classes"></a><span data-ttu-id="4b290-107">Classes do PowerShell do WMI</span><span class="sxs-lookup"><span data-stu-id="4b290-107">WMI PowerShell Classes</span></span>

<span data-ttu-id="4b290-108">**Namespace**: Microsoft. PowerShell. Commands</span><span class="sxs-lookup"><span data-stu-id="4b290-108">**Namespace**: Microsoft.PowerShell.Commands</span></span>

<span data-ttu-id="4b290-109">**Assembly**: Microsoft. PowerShell. Commands. Management</span><span class="sxs-lookup"><span data-stu-id="4b290-109">**Assembly**: Microsoft.PowerShell.Commands.Management</span></span>

<span data-ttu-id="4b290-110">**Dll**: Microsoft.PowerShell.Commands.Management.dll</span><span class="sxs-lookup"><span data-stu-id="4b290-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span></span>

<span data-ttu-id="4b290-111">Essas classes de comando WMI são implementadas pelo Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4b290-111">These WMI command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="4b290-112">Essas classes são incluídas neste Software Development Kit (SDK) apenas para fins de integridade.</span><span class="sxs-lookup"><span data-stu-id="4b290-112">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="4b290-113">Os membros dessas classes não podem ser usados diretamente, nem devem ser usados para derivar outras classes.</span><span class="sxs-lookup"><span data-stu-id="4b290-113">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="4b290-114">Classe</span><span class="sxs-lookup"><span data-stu-id="4b290-114">Class</span></span>                   | <span data-ttu-id="4b290-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b290-115">Description</span></span>                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b290-116">GetWmiObjectCommand</span><span class="sxs-lookup"><span data-stu-id="4b290-116">GetWmiObjectCommand</span></span>     | <span data-ttu-id="4b290-117">Obtém instâncias de classes WMI ou informações sobre as classes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4b290-117">Gets instances of WMI classes or information about the available classes.</span></span><br/> <span data-ttu-id="4b290-118">Consulte o cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) para obter exemplos e informações detalhadas sobre os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b290-118">See the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/> |
| <span data-ttu-id="4b290-119">InvokeWmiMethod</span><span class="sxs-lookup"><span data-stu-id="4b290-119">InvokeWmiMethod</span></span>         | <span data-ttu-id="4b290-120">Chama os métodos WMI.</span><span class="sxs-lookup"><span data-stu-id="4b290-120">Calls WMI methods.</span></span><br/> <span data-ttu-id="4b290-121">Consulte o cmdlet [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) para obter exemplos e informações detalhadas sobre os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b290-121">See the [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                                     |
| <span data-ttu-id="4b290-122">RegisterWmiEventCommand</span><span class="sxs-lookup"><span data-stu-id="4b290-122">RegisterWmiEventCommand</span></span> | <span data-ttu-id="4b290-123">Assina um evento WMI.</span><span class="sxs-lookup"><span data-stu-id="4b290-123">Subscribes to a WMI event.</span></span><br/> <span data-ttu-id="4b290-124">Consulte o cmdlet [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) para obter exemplos e informações detalhadas sobre os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b290-124">See the [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                            |
| <span data-ttu-id="4b290-125">RemoveWmiObject</span><span class="sxs-lookup"><span data-stu-id="4b290-125">RemoveWmiObject</span></span>         | <span data-ttu-id="4b290-126">Exclui uma instância de uma classe WMI existente.</span><span class="sxs-lookup"><span data-stu-id="4b290-126">Deletes an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="4b290-127">Consulte o cmdlet [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) para obter exemplos e informações detalhadas sobre os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b290-127">See the [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                          |
| <span data-ttu-id="4b290-128">SetWmiInstance</span><span class="sxs-lookup"><span data-stu-id="4b290-128">SetWmiInstance</span></span>          | <span data-ttu-id="4b290-129">Cria ou atualiza uma instância de uma classe WMI existente.</span><span class="sxs-lookup"><span data-stu-id="4b290-129">Creates or updates an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="4b290-130">Consulte o cmdlet [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) para obter exemplos e informações detalhadas sobre os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b290-130">See the [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                |



 

 

