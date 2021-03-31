---
title: Recuperando um SDO de usuário
description: Recuperando um SDO de usuário
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c1d6320398afb4eed22f72f0c5e12495010323
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917483"
---
# <a name="retrieving-a-user-sdo"></a><span data-ttu-id="ec303-103">Recuperando um SDO de usuário</span><span class="sxs-lookup"><span data-stu-id="ec303-103">Retrieving a User SDO</span></span>

<span data-ttu-id="ec303-104">O código a seguir recupera um SDO (objeto de dados do servidor) para o administrador.</span><span class="sxs-lookup"><span data-stu-id="ec303-104">The following code retrieves a Server Data Object (SDO) for the Administrator.</span></span>


```C++
   HRESULT  hr;
   _bstr_t bstrUserName = L"Administrator";
   CComPtr<IUnknown> pUserUnknown;

   hr = pSdoMachine->GetUserSDO(
      DATA_STORE_LOCAL,
      bstrUserName,
      (IUnknown**) &pUserUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pUserSDO;
   hr = pUserUnknown->QueryInterface(
      __uuidof(ISdo),
      (void**) &pUserSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a><span data-ttu-id="ec303-105">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec303-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec303-106">Anexando a um computador SDO-Enabled</span><span class="sxs-lookup"><span data-stu-id="ec303-106">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="ec303-107">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="ec303-107">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[<span data-ttu-id="ec303-108">**ISdoMachine**</span><span class="sxs-lookup"><span data-stu-id="ec303-108">**ISdoMachine**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[<span data-ttu-id="ec303-109">**ISdoMachine::GetUserSDO**</span><span class="sxs-lookup"><span data-stu-id="ec303-109">**ISdoMachine::GetUserSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)
</dt> <dt>

[<span data-ttu-id="ec303-110">**SysAllocString**</span><span class="sxs-lookup"><span data-stu-id="ec303-110">**SysAllocString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[<span data-ttu-id="ec303-111">**SysFreeString**</span><span class="sxs-lookup"><span data-stu-id="ec303-111">**SysFreeString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> </dl>

 

 