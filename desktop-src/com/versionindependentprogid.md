---
title: VersionIndependentProgID
description: Associa um ProgID a um CLSID. Esse valor é usado para determinar a versão mais recente de um aplicativo de objeto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006165"
---
# <a name="versionindependentprogid"></a><span data-ttu-id="709ee-105">VersionIndependentProgID</span><span class="sxs-lookup"><span data-stu-id="709ee-105">VersionIndependentProgID</span></span>

<span data-ttu-id="709ee-106">Associa um ProgID a um CLSID.</span><span class="sxs-lookup"><span data-stu-id="709ee-106">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="709ee-107">Esse valor é usado para determinar a versão mais recente de um aplicativo de objeto.</span><span class="sxs-lookup"><span data-stu-id="709ee-107">This value is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="709ee-108">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="709ee-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a><span data-ttu-id="709ee-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="709ee-109">Remarks</span></span>

<span data-ttu-id="709ee-110">Este é um valor de **\_ sz de reg** que especifica a versão mais recente do aplicativo de objeto.</span><span class="sxs-lookup"><span data-stu-id="709ee-110">This is a **REG\_SZ** value that specifies the latest version of the object application.</span></span>

<span data-ttu-id="709ee-111">O ProgID independente de versão é armazenado e mantido exclusivamente pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="709ee-111">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="709ee-112">Ao receber o ProgID independente de versão, a função [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retorna o CLSID da versão atual.</span><span class="sxs-lookup"><span data-stu-id="709ee-112">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="709ee-113">Você pode usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para converter entre essas duas representações.</span><span class="sxs-lookup"><span data-stu-id="709ee-113">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

 

 




