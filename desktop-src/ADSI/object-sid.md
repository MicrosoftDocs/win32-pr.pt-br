---
title: SID de objeto (provedor de WinNT)
description: O SID (identificador de segurança do usuário) pode ser recuperado usando o atributo objectSid. O objectSID é retornado como uma matriz variante de caracteres que formam a cadeia de caracteres SID.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, SID de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004866"
---
# <a name="object-sid-winnt-provider"></a><span data-ttu-id="afdff-105">SID de objeto (provedor de WinNT)</span><span class="sxs-lookup"><span data-stu-id="afdff-105">Object SID (WinNT Provider)</span></span>

<span data-ttu-id="afdff-106">O SID (identificador de segurança do usuário) pode ser recuperado usando o atributo **objectSid** .</span><span class="sxs-lookup"><span data-stu-id="afdff-106">The user security identifier (SID) can be retrieved using the **objectSID** attribute.</span></span> <span data-ttu-id="afdff-107">O **objectSid** é retornado como uma matriz **variante** de caracteres que formam a cadeia de caracteres Sid.</span><span class="sxs-lookup"><span data-stu-id="afdff-107">The **objectSID** is returned as a **VARIANT** array of characters that form the SID string.</span></span>

## <a name="example-code"></a><span data-ttu-id="afdff-108">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="afdff-108">Example Code</span></span>


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




