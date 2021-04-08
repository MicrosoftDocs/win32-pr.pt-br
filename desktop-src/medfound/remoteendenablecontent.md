---
description: 'Versão remota do método IMFContentProtectionManager:: EndEnableContent.'
ms.assetid: aa7a2b3a-5982-4fd8-b5de-7439fc374dfa
title: RemoteEndEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bab87bc39e930c08b96e1d312932f061f9dd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827537"
---
# <a name="remoteendenablecontent"></a><span data-ttu-id="6cb38-103">RemoteEndEnableContent</span><span class="sxs-lookup"><span data-stu-id="6cb38-103">RemoteEndEnableContent</span></span>

<span data-ttu-id="6cb38-104">Versão remota do método [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="6cb38-104">Remotable version of the [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) method.</span></span>

``` syntax
[call_as(EndEnableContent)]
HRESULT RemoteEndEnableContent(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="6cb38-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cb38-105">Remarks</span></span>

<span data-ttu-id="6cb38-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="6cb38-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="6cb38-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="6cb38-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="6cb38-108">Se [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="6cb38-108">If [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb38-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb38-109">Requirements</span></span>



| <span data-ttu-id="6cb38-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb38-110">Requirement</span></span> | <span data-ttu-id="6cb38-111">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb38-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb38-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb38-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb38-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cb38-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6cb38-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb38-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb38-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6cb38-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6cb38-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cb38-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cb38-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb38-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="6cb38-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cb38-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cb38-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cb38-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6cb38-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cb38-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb38-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="6cb38-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




