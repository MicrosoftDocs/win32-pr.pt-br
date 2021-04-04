---
title: InprocServer
description: Especifica o caminho para a DLL do servidor em processo.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916259"
---
# <a name="inprocserver"></a><span data-ttu-id="5d1d4-104">InprocServer</span><span class="sxs-lookup"><span data-stu-id="5d1d4-104">InprocServer</span></span>

<span data-ttu-id="5d1d4-105">Especifica o caminho para a DLL do servidor em processo.</span><span class="sxs-lookup"><span data-stu-id="5d1d4-105">Specifies the path to the in-process server DLL.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5d1d4-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="5d1d4-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a><span data-ttu-id="5d1d4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d1d4-107">Remarks</span></span>

<span data-ttu-id="5d1d4-108">A entrada **InprocServer** é relativamente rara para classes insertáveis.</span><span class="sxs-lookup"><span data-stu-id="5d1d4-108">The **InprocServer** entry is relatively rare for insertable classes.</span></span>

<span data-ttu-id="5d1d4-109">Atualmente, os servidores em processo são registrados usando a entrada de registro **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="5d1d4-109">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="5d1d4-110">Os servidores em processo de 32 bits e 64 bits devem usar a entrada [**InprocServer32**](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="5d1d4-110">The 32-bit and 64-bit in-process servers should use the [**InprocServer32**](inprocserver32.md) entry.</span></span> <span data-ttu-id="5d1d4-111">Se um contêiner estiver pesquisando o registro de um servidor em processo, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits tem prioridade com um contêiner de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5d1d4-111">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d1d4-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d1d4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d1d4-113">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="5d1d4-113">**InprocServer32**</span></span>](inprocserver32.md)
</dt> </dl>

 

 




