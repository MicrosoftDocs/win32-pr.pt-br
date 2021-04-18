---
title: Protocolo
description: Indica que esta classe OLE 2 é insertável em contêineres de OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Chave do registro de protocolo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793706"
---
# <a name="protocol"></a><span data-ttu-id="5f937-104">Protocolo</span><span class="sxs-lookup"><span data-stu-id="5f937-104">Protocol</span></span>

<span data-ttu-id="5f937-105">Indica que esta classe OLE 2 é insertável em contêineres de OLE 1.</span><span class="sxs-lookup"><span data-stu-id="5f937-105">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5f937-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="5f937-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a><span data-ttu-id="5f937-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f937-107">Remarks</span></span>

<span data-ttu-id="5f937-108">A entrada **StdFileEditing** especifica informações de compatibilidade de OLE 1.</span><span class="sxs-lookup"><span data-stu-id="5f937-108">The **StdFileEditing** entry specifies OLE 1 compatibility information.</span></span> <span data-ttu-id="5f937-109">Ele deve estar presente somente se os objetos dessa classe forem insertáveis em contêineres de OLE 1.</span><span class="sxs-lookup"><span data-stu-id="5f937-109">It should be present only if objects of this class are insertable in OLE 1 containers.</span></span>

<span data-ttu-id="5f937-110">**Servidor** especifica o caminho completo para o aplicativo de servidor OLE 2 e o **verbo** especifica os verbos.</span><span class="sxs-lookup"><span data-stu-id="5f937-110">**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs.</span></span> <span data-ttu-id="5f937-111">O verbo 0 é o verbo primário e os verbos adicionais devem ser numerados consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="5f937-111">Verb 0 is the primary verb and additional verbs must be numbered consecutively.</span></span>

 

 




