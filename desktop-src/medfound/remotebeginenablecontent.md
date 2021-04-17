---
description: 'Versão remota do método IMFContentProtectionManager:: BeginEnableContent.'
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: RemoteBeginEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9bc4a445ec07a7e9678a9d0a193311554f855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749526"
---
# <a name="remotebeginenablecontent"></a><span data-ttu-id="71db8-103">RemoteBeginEnableContent</span><span class="sxs-lookup"><span data-stu-id="71db8-103">RemoteBeginEnableContent</span></span>

<span data-ttu-id="71db8-104">Versão remota do método [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="71db8-104">Remotable version of the [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="71db8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="71db8-105">Remarks</span></span>

<span data-ttu-id="71db8-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="71db8-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="71db8-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="71db8-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="71db8-108">Se [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="71db8-108">If [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="71db8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71db8-109">Requirements</span></span>



| <span data-ttu-id="71db8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="71db8-110">Requirement</span></span> | <span data-ttu-id="71db8-111">Valor</span><span class="sxs-lookup"><span data-stu-id="71db8-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71db8-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71db8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="71db8-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71db8-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71db8-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71db8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="71db8-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71db8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71db8-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71db8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="71db8-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71db8-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="71db8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71db8-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="71db8-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71db8-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="71db8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="71db8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71db8-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="71db8-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




