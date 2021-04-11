---
description: Se você usar a API de script para o WMI, poderá definir privilégios de segurança específicos.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Executando operações privilegiadas usando o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091784"
---
# <a name="executing-privileged-operations-using-vbscript"></a><span data-ttu-id="15af1-103">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="15af1-103">Executing Privileged Operations Using VBScript</span></span>

<span data-ttu-id="15af1-104">Se você usar a API de script para o WMI, poderá definir privilégios de segurança específicos.</span><span class="sxs-lookup"><span data-stu-id="15af1-104">If you use the scripting API for WMI, you can set specific security privileges.</span></span> <span data-ttu-id="15af1-105">Por exemplo, você pode definir os privilégios de segurança para solicitar um desligamento do sistema operacional ou para examinar o log de eventos de segurança.</span><span class="sxs-lookup"><span data-stu-id="15af1-105">For example, you can set the security privileges to request an operating system shutdown, or to examine the security event log.</span></span> <span data-ttu-id="15af1-106">Para obter mais informações, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="15af1-106">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="15af1-107">Você só precisa definir privilégios quando estiver acessando o WMI em seu computador.</span><span class="sxs-lookup"><span data-stu-id="15af1-107">You only need to set privileges when you are accessing WMI on your computer.</span></span> <span data-ttu-id="15af1-108">Quando você está acessando um host remoto, o COM RPC define automaticamente os privilégios.</span><span class="sxs-lookup"><span data-stu-id="15af1-108">When you are accessing a remote host, COM RPC automatically sets the privileges.</span></span> <span data-ttu-id="15af1-109">Para determinar todos os privilégios necessários, consulte a documentação para as classes específicas do WMI que você deseja acessar, como o [**sistema \_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="15af1-109">To determine all the required privileges, consult the documentation for the specific WMI classes that you want to access, such as [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span> <span data-ttu-id="15af1-110">Para obter mais informações, consulte [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="15af1-110">For more information, see [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>

<span data-ttu-id="15af1-111">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="15af1-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="15af1-112">Definindo um privilégio do objeto de segurança \_</span><span class="sxs-lookup"><span data-stu-id="15af1-112">Setting a Privilege from the Security\_ Object</span></span>](/windows)
-   [<span data-ttu-id="15af1-113">Definindo um privilégio como parte de um moniker</span><span class="sxs-lookup"><span data-stu-id="15af1-113">Setting a Privilege as Part of a Moniker</span></span>](#setting-a-privilege-as-part-of-a-moniker)
-   [<span data-ttu-id="15af1-114">Revogando e redefinindo privilégios</span><span class="sxs-lookup"><span data-stu-id="15af1-114">Revoking and Resetting Privileges</span></span>](#revoking-and-resetting-privileges)
-   [<span data-ttu-id="15af1-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15af1-115">Related topics</span></span>](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a><span data-ttu-id="15af1-116">Definindo um privilégio do objeto de segurança \_</span><span class="sxs-lookup"><span data-stu-id="15af1-116">Setting a Privilege from the Security\_ Object</span></span>

<span data-ttu-id="15af1-117">Use o procedimento a seguir para definir privilégios de segurança em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="15af1-117">Use the following procedure to set security privileges in Visual Basic.</span></span>

<span data-ttu-id="15af1-118">**Para definir privilégios em Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="15af1-118">**To set privileges in Visual Basic**</span></span>

1.  <span data-ttu-id="15af1-119">Crie um objeto do tipo [**SWbemLocator**](swbemlocator.md).</span><span class="sxs-lookup"><span data-stu-id="15af1-119">Create an object of type [**SWbemLocator**](swbemlocator.md).</span></span>
2.  <span data-ttu-id="15af1-120">Adicione o novo privilégio ao objeto [**SWbemLocator. Security \_**](swbemlocator-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="15af1-120">Add the new privilege to the [**SWbemLocator.Security\_**](swbemlocator-security-.md) object.</span></span>

    <span data-ttu-id="15af1-121">O objeto de [**segurança \_**](swbemlocator-security-.md) contém uma coleção [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="15af1-121">The [**Security\_**](swbemlocator-security-.md) object contains an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="15af1-122">Os objetos no conjunto são objetos [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="15af1-122">The objects in the set are [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="15af1-123">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="15af1-123">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

3.  <span data-ttu-id="15af1-124">Faça logon no WMI e recupere um objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="15af1-124">Log on to WMI and retrieve an [**SWbemServices**](swbemservices.md) object.</span></span>

    <span data-ttu-id="15af1-125">O objeto [**SWbemServices**](swbemservices.md) herda o privilégio que é definido na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="15af1-125">The [**SWbemServices**](swbemservices.md) object inherits the privilege that is set in the previous step.</span></span>

<span data-ttu-id="15af1-126">Você também pode definir um privilégio usando o método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="15af1-126">You can also set a privilege using the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method.</span></span>

## <a name="setting-a-privilege-as-part-of-a-moniker"></a><span data-ttu-id="15af1-127">Definindo um privilégio como parte de um moniker</span><span class="sxs-lookup"><span data-stu-id="15af1-127">Setting a Privilege as Part of a Moniker</span></span>

<span data-ttu-id="15af1-128">Você pode definir um privilégio como parte de um moniker.</span><span class="sxs-lookup"><span data-stu-id="15af1-128">You can set a privilege as part of a moniker.</span></span>

<span data-ttu-id="15af1-129">O exemplo a seguir mostra como adicionar um privilégio de depuração a um moniker.</span><span class="sxs-lookup"><span data-stu-id="15af1-129">The following example shows you how to add a debug privilege to a moniker.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a><span data-ttu-id="15af1-130">Revogando e redefinindo privilégios</span><span class="sxs-lookup"><span data-stu-id="15af1-130">Revoking and Resetting Privileges</span></span>

<span data-ttu-id="15af1-131">O exemplo a seguir mostra como definir o privilégio **SeDebugPrivilege** e revogar o privilégio **SeRemoteShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="15af1-131">The following example shows you how to set the **SeDebugPrivilege** privilege, and revoke the **SeRemoteShutdownPrivilege** privilege.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a><span data-ttu-id="15af1-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15af1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15af1-133">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="15af1-133">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="15af1-134">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="15af1-134">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> </dl>

 

 
