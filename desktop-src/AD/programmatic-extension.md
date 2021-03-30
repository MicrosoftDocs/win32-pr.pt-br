---
title: Extensão programática
description: As extensões programáticas têm vários méritos, no entanto, um aplicativo é opaco; o administrador deve confiar na documentação incluída no aplicativo de instalação.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Extensão programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634929"
---
# <a name="programmatic-extension"></a><span data-ttu-id="cbcc3-104">Extensão programática</span><span class="sxs-lookup"><span data-stu-id="cbcc3-104">Programmatic Extension</span></span>

<span data-ttu-id="cbcc3-105">O benefício de um arquivo LDIF é que o administrador pode examinar sua função.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-105">The benefit of an LDIF file is that the administrator can examine its function.</span></span> <span data-ttu-id="cbcc3-106">No entanto, o esquema também pode ser estendido programaticamente.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-106">However, the schema can also be extended programmatically.</span></span> <span data-ttu-id="cbcc3-107">As extensões programáticas têm vários méritos, mas um aplicativo é opaco; o administrador deve confiar na documentação incluída no aplicativo de instalação.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-107">Programmatic extensions have several merits, but an application is opaque; the administrator must trust the documentation included with the setup application.</span></span> <span data-ttu-id="cbcc3-108">O uso de extensões de esquema programático pode ser uma barreira para a implantação de aplicativos que os usam.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-108">Use of programmatic schema extensions may be a barrier to deployment for applications that use them.</span></span> <span data-ttu-id="cbcc3-109">Uma extensão programática é invariável; é um executável do Windows NT.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-109">A programmatic extension is invariant; it is a Windows NT executable.</span></span> <span data-ttu-id="cbcc3-110">O binário não pode ser adulterado, ao contrário de um arquivo LDIF ou. csv, que pode ser editado inadvertidamente ou maliciosamente.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-110">The binary cannot be tampered with, unlike an LDIF or .csv file, which can be edited inadvertently or maliciously.</span></span>

<span data-ttu-id="cbcc3-111">Os benefícios de um arquivo LDIF incluem:</span><span class="sxs-lookup"><span data-stu-id="cbcc3-111">Benefits of an LDIF file include:</span></span>

-   <span data-ttu-id="cbcc3-112">Os aplicativos podem detectar e se recuperar de erros e fornecer comentários do usuário.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-112">Applications can detect and recover from errors and provide user feedback.</span></span>
-   <span data-ttu-id="cbcc3-113">Os aplicativos podem manipular o Unicode sem recorrer à codificação Base64.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-113">Applications can handle Unicode without resorting to Base64 encoding.</span></span>
-   <span data-ttu-id="cbcc3-114">Os aplicativos podem aproveitar Windows Installer APIs de instalação.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-114">Applications can leverage Windows Installer setup APIs.</span></span>
-   <span data-ttu-id="cbcc3-115">Os aplicativos podem ser assinados para estabelecer a autenticidade.</span><span class="sxs-lookup"><span data-stu-id="cbcc3-115">Applications can be signed to establish authenticity.</span></span>

 

 




