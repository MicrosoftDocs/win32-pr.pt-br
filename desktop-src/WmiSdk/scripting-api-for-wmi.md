---
description: A referência de script do WMI contém definições para a API de script do WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de script para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827729"
---
# <a name="scripting-api-for-wmi"></a><span data-ttu-id="0918e-103">API de script para WMI</span><span class="sxs-lookup"><span data-stu-id="0918e-103">Scripting API for WMI</span></span>

<span data-ttu-id="0918e-104">A referência de script do WMI contém definições para a API de script do WMI.</span><span class="sxs-lookup"><span data-stu-id="0918e-104">The WMI scripting reference contains definitions for the WMI Scripting API.</span></span> <span data-ttu-id="0918e-105">Use essa API se estiver escrevendo aplicativos com o Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript) ou qualquer outra linguagem de script que ofereça suporte a tecnologias de script ativas.</span><span class="sxs-lookup"><span data-stu-id="0918e-105">Use this API if writing applications with Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript), or any other scripting language that supports active scripting technologies.</span></span>

> [!Note]  
> <span data-ttu-id="0918e-106">O PowerShell também está disponível para scripts com o WMI.</span><span class="sxs-lookup"><span data-stu-id="0918e-106">PowerShell is also available for scripting with WMI.</span></span> <span data-ttu-id="0918e-107">O cmdlet Get-WMI e os três aceleradores de tipo ( \[ WMI \] , \[ WMIClass \] e \[ WMISEARCHER \] ) habilitam o acesso administrativo básico ao WMI.</span><span class="sxs-lookup"><span data-stu-id="0918e-107">The Get-WMI cmdlet and the three type accelerators (\[wmi\], \[wmiclass\], and \[wmisearcher\]) enable basic administrative access to WMI.</span></span> <span data-ttu-id="0918e-108">Para obter mais informações, consulte [scripts com o Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="0918e-108">For more information, see [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span></span>

 

<span data-ttu-id="0918e-109">Os objetos de script WMI, exceto para [**SWbemDateTime**](swbemdatetime.md) , não são marcados como seguros para scripts em execução em páginas HTML no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0918e-109">WMI scripting objects, except for [**SWbemDateTime**](swbemdatetime.md) are not marked safe for scripting for scripts running on HTML pages in Internet Explorer.</span></span> <span data-ttu-id="0918e-110">Portanto, a menos que o nível de segurança no Internet Explorer seja reduzido, o script falhará.</span><span class="sxs-lookup"><span data-stu-id="0918e-110">Therefore, unless the security level within Internet Explorer is lowered, the script will fail.</span></span> <span data-ttu-id="0918e-111">**SWbemDateTime** é marcado como seguro para inicialização e scripts.</span><span class="sxs-lookup"><span data-stu-id="0918e-111">**SWbemDateTime** is marked safe for initialization and scripting.</span></span> <span data-ttu-id="0918e-112">No entanto, use todos os objetos de script WMI em chamadas **GetObject** e **CreateObject** no código do lado do servidor em páginas do Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="0918e-112">However, use all WMI scripting objects in **GetObject** and **CreateObject** calls on server-side code in Active Server Pages (ASP).</span></span>

-   [<span data-ttu-id="0918e-113">Modelo de objeto de API de script</span><span class="sxs-lookup"><span data-stu-id="0918e-113">Scripting API Object Model</span></span>](scripting-api-object-model.md)
-   [<span data-ttu-id="0918e-114">Convenções de documento para a API de script</span><span class="sxs-lookup"><span data-stu-id="0918e-114">Document Conventions for the Scripting API</span></span>](document-conventions-for-the-scripting-api.md)
-   [<span data-ttu-id="0918e-115">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="0918e-115">Scripting API Objects</span></span>](scripting-api-objects.md)
-   [<span data-ttu-id="0918e-116">Constantes de API de script</span><span class="sxs-lookup"><span data-stu-id="0918e-116">Scripting API Constants</span></span>](scripting-api-constants.md)

## <a name="related-topics"></a><span data-ttu-id="0918e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0918e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0918e-118">Referência de WMI</span><span class="sxs-lookup"><span data-stu-id="0918e-118">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="0918e-119">Códigos de retorno do WMI</span><span class="sxs-lookup"><span data-stu-id="0918e-119">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

 



