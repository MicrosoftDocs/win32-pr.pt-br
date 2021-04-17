---
description: 'Versão remota do método IMFMediaTypeHandler:: GetCurrentMediaType.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: RemoteGetCurrentMediaType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105764125"
---
# <a name="remotegetcurrentmediatype"></a><span data-ttu-id="a64bb-103">RemoteGetCurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="a64bb-103">RemoteGetCurrentMediaType</span></span>

<span data-ttu-id="a64bb-104">Versão remota do método [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="a64bb-104">Remotable version of the [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) method.</span></span>

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a><span data-ttu-id="a64bb-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a64bb-105">Remarks</span></span>

<span data-ttu-id="a64bb-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="a64bb-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="a64bb-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="a64bb-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="a64bb-108">Se [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="a64bb-108">If [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

<span data-ttu-id="a64bb-109">Essa interface estará disponível nas seguintes plataformas se os componentes redistribuíveis do SDK do Windows Media Format 11 são instalados:</span><span class="sxs-lookup"><span data-stu-id="a64bb-109">This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:</span></span>

-   <span data-ttu-id="a64bb-110">Windows XP com Service Pack 2 (SP2) e posterior.</span><span class="sxs-lookup"><span data-stu-id="a64bb-110">Windows XP with Service Pack 2 (SP2) and later.</span></span>
-   <span data-ttu-id="a64bb-111">Windows XP Media Center Edition 2005 com KB900325 (Windows XP Media Center Edition 2005) e KB925766 (pacote cumulativo de atualizações de outubro de 2006 para Windows XP Media Center Edition) instalado.</span><span class="sxs-lookup"><span data-stu-id="a64bb-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a64bb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a64bb-112">Requirements</span></span>



| <span data-ttu-id="a64bb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a64bb-113">Requirement</span></span> | <span data-ttu-id="a64bb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a64bb-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64bb-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a64bb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a64bb-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="a64bb-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="a64bb-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a64bb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a64bb-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a64bb-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="a64bb-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a64bb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a64bb-120"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a64bb-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="a64bb-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a64bb-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="a64bb-122"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a64bb-122"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="a64bb-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a64bb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64bb-124">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="a64bb-124">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




