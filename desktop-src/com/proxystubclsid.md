---
title: ProxyStubClsid
description: Mapeia um IID para um CLSID em DLLs de proxy de 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- COM valor do registro ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005923"
---
# <a name="proxystubclsid"></a><span data-ttu-id="b2d56-104">ProxyStubClsid</span><span class="sxs-lookup"><span data-stu-id="b2d56-104">ProxyStubClsid</span></span>

<span data-ttu-id="b2d56-105">Mapeia um IID para um CLSID em DLLs de proxy de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b2d56-105">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b2d56-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="b2d56-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="b2d56-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2d56-107">Remarks</span></span>

<span data-ttu-id="b2d56-108">Este é um **valor \_ sz de reg** que especifica o CLSID para o IID.</span><span class="sxs-lookup"><span data-stu-id="b2d56-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="b2d56-109">Se você adicionar interfaces, deverá usar essa entrada para registrá-las (sistemas de 16 bits) para que o OLE possa encontrar o código de comunicação remota apropriado para estabelecer a comunicação entre processos.</span><span class="sxs-lookup"><span data-stu-id="b2d56-109">If you add interfaces, you must use this entry to register them (16-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2d56-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2d56-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2d56-111">**Interface**</span><span class="sxs-lookup"><span data-stu-id="b2d56-111">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="b2d56-112">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="b2d56-112">**ProxyStubClsid32**</span></span>](proxystubclsid32.md)
</dt> </dl>

 

 




