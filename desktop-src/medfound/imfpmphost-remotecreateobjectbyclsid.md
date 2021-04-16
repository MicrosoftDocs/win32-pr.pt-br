---
description: 'Versão remota do método IMFPMPHost:: CreateObjectByCLSID.'
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: RemoteCreateObjectByCLSID (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759018"
---
# <a name="remotecreateobjectbyclsid"></a><span data-ttu-id="88b90-103">RemoteCreateObjectByCLSID</span><span class="sxs-lookup"><span data-stu-id="88b90-103">RemoteCreateObjectByCLSID</span></span>

<span data-ttu-id="88b90-104">Versão remota do método [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="88b90-104">Remotable version of the [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) method.</span></span>

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a><span data-ttu-id="88b90-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="88b90-105">Remarks</span></span>

<span data-ttu-id="88b90-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="88b90-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="88b90-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="88b90-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="88b90-108">Se [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="88b90-108">If [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b90-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88b90-109">Requirements</span></span>



| <span data-ttu-id="88b90-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="88b90-110">Requirement</span></span> | <span data-ttu-id="88b90-111">Valor</span><span class="sxs-lookup"><span data-stu-id="88b90-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b90-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88b90-112">Minimum supported client</span></span><br/> | <span data-ttu-id="88b90-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88b90-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="88b90-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88b90-114">Minimum supported server</span></span><br/> | <span data-ttu-id="88b90-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88b90-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88b90-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88b90-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="88b90-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88b90-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="88b90-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88b90-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="88b90-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88b90-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="88b90-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="88b90-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b90-121">**IMFPMPHost**</span><span class="sxs-lookup"><span data-stu-id="88b90-121">**IMFPMPHost**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[<span data-ttu-id="88b90-122">Sessão de mídia do PMP</span><span class="sxs-lookup"><span data-stu-id="88b90-122">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="88b90-123">Caminho de mídia protegido</span><span class="sxs-lookup"><span data-stu-id="88b90-123">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 




