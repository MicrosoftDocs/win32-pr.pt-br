---
description: No Windows 7, a WMI implementou a \_ classe Win32 OptionalFeature. Essa classe recupera o status dos recursos opcionais que estão presentes em um computador.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Consultando o status de recursos opcionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661840"
---
# <a name="querying-the-status-of-optional-features"></a><span data-ttu-id="0cbf1-104">Consultando o status de recursos opcionais</span><span class="sxs-lookup"><span data-stu-id="0cbf1-104">Querying the Status of Optional Features</span></span>

<span data-ttu-id="0cbf1-105">No Windows 7, a WMI implementou a classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="0cbf1-105">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="0cbf1-106">Essa classe recupera o status dos recursos opcionais que estão presentes em um computador.</span><span class="sxs-lookup"><span data-stu-id="0cbf1-106">This class retrieves the status of the optional features that are present on a computer.</span></span>

<span data-ttu-id="0cbf1-107">Você pode usar os cmdlets do Windows PowerShell para consultar o status dos recursos opcionais.</span><span class="sxs-lookup"><span data-stu-id="0cbf1-107">You can use Windows PowerShell cmdlets to query the status of optional features.</span></span> <span data-ttu-id="0cbf1-108">Todos os exemplos neste tópico usam o cmdlet Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="0cbf1-108">All of the examples in this topic use the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="0cbf1-109">Para obter mais informações, consulte [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="0cbf1-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

<span data-ttu-id="0cbf1-110">**Para recuperar todas as instâncias de recursos opcionais presentes em um computador**</span><span class="sxs-lookup"><span data-stu-id="0cbf1-110">**To retrieve all instances of optional features present on a computer**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="0cbf1-111">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cbf1-111">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

<span data-ttu-id="0cbf1-112">**Para consultar um recurso opcional especificando o nome do recurso**</span><span class="sxs-lookup"><span data-stu-id="0cbf1-112">**To query for an optional feature by specifying the feature name**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="0cbf1-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cbf1-113">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > <span data-ttu-id="0cbf1-114">A propriedade **Name** diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0cbf1-114">The **name** property is case-sensitive.</span></span>

     

<span data-ttu-id="0cbf1-115">**Para consultar recursos opcionais especificando o estado de instalação**</span><span class="sxs-lookup"><span data-stu-id="0cbf1-115">**To query for optional features by specifying the install state**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="0cbf1-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cbf1-116">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    <span data-ttu-id="0cbf1-117">Para obter mais informações sobre os valores possíveis para a propriedade **InstallState** , consulte [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span><span class="sxs-lookup"><span data-stu-id="0cbf1-117">For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cbf1-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0cbf1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cbf1-119">**\_OptionalFeature Win32**</span><span class="sxs-lookup"><span data-stu-id="0cbf1-119">**Win32\_OptionalFeature**</span></span>](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
