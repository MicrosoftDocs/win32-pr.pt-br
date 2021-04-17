---
description: Um caminho de objeto de classe descreve o local de uma classe dentro de um namespace.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Descrevendo um caminho de objeto de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782712"
---
# <a name="describing-a-class-object-path"></a><span data-ttu-id="ff308-103">Descrevendo um caminho de objeto de classe</span><span class="sxs-lookup"><span data-stu-id="ff308-103">Describing a Class Object Path</span></span>

<span data-ttu-id="ff308-104">Um caminho de objeto de classe descreve o local de uma classe dentro de um namespace.</span><span class="sxs-lookup"><span data-stu-id="ff308-104">A class object path describes the location of a class within a namespace.</span></span>

<span data-ttu-id="ff308-105">Você pode usar os seguintes métodos para especificar um caminho de objeto:</span><span class="sxs-lookup"><span data-stu-id="ff308-105">You can use the following methods to specify an object path:</span></span>

-   <span data-ttu-id="ff308-106">Um caminho de objeto completo para uma classe acrescenta o nome de classe a um caminho de namespace.</span><span class="sxs-lookup"><span data-stu-id="ff308-106">A full object path to a class appends the class name to a namespace path.</span></span>

    <span data-ttu-id="ff308-107">O exemplo a seguir mostra o local da classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dentro do \\ \\ namespace raiz cimv2 no servidor chamado admin.</span><span class="sxs-lookup"><span data-stu-id="ff308-107">The following example shows the location of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class within the \\root\\cimv2 namespace on the server named Admin.</span></span>

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   <span data-ttu-id="ff308-108">Um caminho de objeto relativo representa uma classe que reside no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="ff308-108">A relative object path represents a class that resides in the current namespace.</span></span> <span data-ttu-id="ff308-109">Um caminho de objeto relativo para uma classe contém apenas o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="ff308-109">A relative object path to a class contains only the class name.</span></span>

    <span data-ttu-id="ff308-110">O exemplo a seguir mostra o caminho relativo para a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="ff308-110">The following example shows the relative path to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

    ``` syntax
    Win32_LogicalDisk
    ```

<span data-ttu-id="ff308-111">Quando você consulta um nome de classe, mas não especifica nenhuma instância, o WMI retorna a definição de classe.</span><span class="sxs-lookup"><span data-stu-id="ff308-111">When you query for a class name but specify no instances, WMI returns the class definition.</span></span> <span data-ttu-id="ff308-112">O procedimento a seguir descreve como recuperar uma definição de classe no VBScript.</span><span class="sxs-lookup"><span data-stu-id="ff308-112">The following procedure describes how to retrieve a class definition in VBScript.</span></span>

<span data-ttu-id="ff308-113">**Para recuperar uma definição de classe no VBScript**</span><span class="sxs-lookup"><span data-stu-id="ff308-113">**To retrieve a class definition in VBScript**</span></span>

-   <span data-ttu-id="ff308-114">Você pode usar a conexão de moniker com uma consulta ou [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="ff308-114">You can use the moniker connection either with a query or [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span></span> <span data-ttu-id="ff308-115">Você também pode usar [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="ff308-115">You can also use [**SWbemServices.Get**](swbemservices-get.md).</span></span>

    <span data-ttu-id="ff308-116">O exemplo a seguir mostra como usar [GetObject](/previous-versions//kdccchxa(v=vs.85)) para obter uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="ff308-116">The following example shows how to use [GetObject](/previous-versions//kdccchxa(v=vs.85)) to get a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    <span data-ttu-id="ff308-117">O exemplo a seguir mostra como consultar uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="ff308-117">The following example shows how to query for a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

<span data-ttu-id="ff308-118">Você pode recuperar uma definição de classe em C++ especificando apenas o nome da classe e nenhum caminho para uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="ff308-118">You can retrieve a class definition in C++ by specifying only the class name and no path to a particular instance.</span></span> <span data-ttu-id="ff308-119">O procedimento a seguir descreve como recuperar uma definição de classe em C++.</span><span class="sxs-lookup"><span data-stu-id="ff308-119">The following procedure describes how to retrieve a class definition in C++.</span></span>

<span data-ttu-id="ff308-120">**Para recuperar uma definição de classe em C++**</span><span class="sxs-lookup"><span data-stu-id="ff308-120">**To retrieve a class definition in C++**</span></span>

-   <span data-ttu-id="ff308-121">Faça uma chamada para as funções [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="ff308-121">Make a call to the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) functions.</span></span>

    <span data-ttu-id="ff308-122">O exemplo a seguir mostra como chamar a função [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="ff308-122">The following example shows how to call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) function.</span></span>

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    <span data-ttu-id="ff308-123">O exemplo de código anterior requer que a seguinte \# instrução include seja compilada corretamente.</span><span class="sxs-lookup"><span data-stu-id="ff308-123">The previous code example requires the following \#include statement to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
