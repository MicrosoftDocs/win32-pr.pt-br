---
title: MachineLaunchRestriction
description: Define a política de restrição de todo o computador para inicialização e ativação de componentes.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- COM valor do registro MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160317"
---
# <a name="machinelaunchrestriction"></a><span data-ttu-id="1924b-104">MachineLaunchRestriction</span><span class="sxs-lookup"><span data-stu-id="1924b-104">MachineLaunchRestriction</span></span>

<span data-ttu-id="1924b-105">Define a política de restrição de todo o computador para inicialização e ativação de componentes.</span><span class="sxs-lookup"><span data-stu-id="1924b-105">Sets the computer-wide restriction policy for component launch and activation.</span></span>

> [!Caution]  
> <span data-ttu-id="1924b-106">A alteração desse valor afetará todos os aplicativos de servidor COM e poderá impedi-lo de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="1924b-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="1924b-107">Se houver aplicativos de servidor COM que tenham restrições menos rigorosas do que as restrições em todo o computador, reduzir as restrições de computador poderá expor esses aplicativos para acesso indesejado.</span><span class="sxs-lookup"><span data-stu-id="1924b-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="1924b-108">Por outro lado, se você aumentar as restrições de todo o computador, alguns aplicativos de servidor COM podem não estar mais acessíveis chamando aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1924b-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="1924b-109">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="1924b-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="1924b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1924b-110">Remarks</span></span>

<span data-ttu-id="1924b-111">Esse é um **valor \_ binário reg** .</span><span class="sxs-lookup"><span data-stu-id="1924b-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="1924b-112">As entidades não dadas as permissões aqui não podem obtê-las mesmo se as permissões forem concedidas pelo valor do registro [DefaultAccessPermission](defaultaccesspermission.md) ou pela função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="1924b-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="1924b-113">Por padrão, os administradores podem obter permissões locais e remotas de inicialização e ativação, e os membros do grupo Everyone podem obter as permissões de ativação local e de inicialização.</span><span class="sxs-lookup"><span data-stu-id="1924b-113">By default, administrators may obtain local and remote launch and activation permissions, and members of the Everyone group may obtain local activation and launch permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1924b-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1924b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1924b-115">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="1924b-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




