---
title: MachineAccessRestriction
description: Define a política de restrição de todo o computador para acesso ao componente.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- COM valor do registro MachineAccessRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788865"
---
# <a name="machineaccessrestriction"></a><span data-ttu-id="f54c4-104">MachineAccessRestriction</span><span class="sxs-lookup"><span data-stu-id="f54c4-104">MachineAccessRestriction</span></span>

<span data-ttu-id="f54c4-105">Define a política de restrição de todo o computador para acesso ao componente.</span><span class="sxs-lookup"><span data-stu-id="f54c4-105">Sets the computer-wide restriction policy for component access.</span></span>

> [!Caution]  
> <span data-ttu-id="f54c4-106">A alteração desse valor afetará todos os aplicativos de servidor COM e poderá impedi-lo de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="f54c4-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="f54c4-107">Se houver aplicativos de servidor COM que tenham restrições menos rigorosas do que as restrições em todo o computador, reduzir as restrições de computador poderá expor esses aplicativos para acesso indesejado.</span><span class="sxs-lookup"><span data-stu-id="f54c4-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="f54c4-108">Por outro lado, se você aumentar as restrições de todo o computador, alguns aplicativos de servidor COM podem não estar mais acessíveis chamando aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f54c4-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="f54c4-109">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="f54c4-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="f54c4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f54c4-110">Remarks</span></span>

<span data-ttu-id="f54c4-111">Esse é um **valor \_ binário reg** .</span><span class="sxs-lookup"><span data-stu-id="f54c4-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="f54c4-112">As entidades não dadas as permissões aqui não podem obtê-las mesmo se as permissões forem concedidas pelo valor do registro [DefaultAccessPermission](defaultaccesspermission.md) ou pela função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="f54c4-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="f54c4-113">Por padrão, os membros do grupo Everyone podem obter permissões de acesso local e remota, e os usuários anônimos podem obter permissões de acesso local.</span><span class="sxs-lookup"><span data-stu-id="f54c4-113">By default, members of the Everyone group can obtain local and remote access permissions, and anonymous users can obtain local access permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f54c4-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f54c4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f54c4-115">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="f54c4-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




