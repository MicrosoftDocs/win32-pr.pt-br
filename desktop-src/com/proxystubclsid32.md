---
title: ProxyStubClsid32
description: Mapeia um IID para um CLSID em DLLs de proxy de 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- COM valor do registro ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294533"
---
# <a name="proxystubclsid32"></a><span data-ttu-id="2a2b1-104">ProxyStubClsid32</span><span class="sxs-lookup"><span data-stu-id="2a2b1-104">ProxyStubClsid32</span></span>

<span data-ttu-id="2a2b1-105">Mapeia um IID para um CLSID em DLLs de proxy de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2a2b1-105">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2a2b1-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="2a2b1-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="2a2b1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a2b1-107">Remarks</span></span>

<span data-ttu-id="2a2b1-108">Este é um **valor \_ sz de reg** que especifica o CLSID para o IID.</span><span class="sxs-lookup"><span data-stu-id="2a2b1-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="2a2b1-109">Essa é uma entrada necessária, pois o mapeamento de IID para CLSID pode ser diferente para interfaces de 16 bits e de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2a2b1-109">This is a required entry since the IID-to-CLSID mapping may be different for 16-bit and 32-bit interfaces.</span></span> <span data-ttu-id="2a2b1-110">O mapeamento de IID para CLSID depende da maneira como os proxies de interface são empacotados em um conjunto de DLLs de proxy.</span><span class="sxs-lookup"><span data-stu-id="2a2b1-110">The IID-to-CLSID mapping depends on the way the interface proxies are packaged into a set of proxy DLLs.</span></span>

<span data-ttu-id="2a2b1-111">Se você adicionar interfaces, deverá usar essa entrada para registrá-las (sistemas de 32 bits) para que o OLE possa encontrar o código de comunicação remota apropriado para estabelecer a comunicação entre processos.</span><span class="sxs-lookup"><span data-stu-id="2a2b1-111">If you add interfaces, you must use this entry to register them (32-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a2b1-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a2b1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a2b1-113">**IMarshal**</span><span class="sxs-lookup"><span data-stu-id="2a2b1-113">**IMarshal**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[<span data-ttu-id="2a2b1-114">**Interface**</span><span class="sxs-lookup"><span data-stu-id="2a2b1-114">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="2a2b1-115">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="2a2b1-115">**ProxyStubClsid**</span></span>](proxystubclsid.md)
</dt> </dl>

 

 