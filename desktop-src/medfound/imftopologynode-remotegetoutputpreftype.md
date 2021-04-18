---
description: 'Versão remota do método IMFTopologyNode:: GetOutputPrefType.'
ms.assetid: 56fbbf14-0c55-4f98-bcda-7f434cff803c
title: RemoteGetOutputPrefType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46069add8f9d15a2b3742a083a1cf169a46b969f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786256"
---
# <a name="remotegetoutputpreftype"></a><span data-ttu-id="8068e-103">RemoteGetOutputPrefType</span><span class="sxs-lookup"><span data-stu-id="8068e-103">RemoteGetOutputPrefType</span></span>

<span data-ttu-id="8068e-104">Versão remota do método [**IMFTopologyNode:: GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) .</span><span class="sxs-lookup"><span data-stu-id="8068e-104">Remotable version of the [**IMFTopologyNode::GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) method.</span></span>

``` syntax
[call_as(GetOutputPrefType)] 
HRESULT RemoteGetOutputPrefType(
    DWORD dwOutputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="8068e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8068e-105">Remarks</span></span>

<span data-ttu-id="8068e-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="8068e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="8068e-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="8068e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="8068e-108">Se **GetOutputPrefType** for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="8068e-108">If **GetOutputPrefType** is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="8068e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8068e-109">Requirements</span></span>



| <span data-ttu-id="8068e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8068e-110">Requirement</span></span> | <span data-ttu-id="8068e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="8068e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8068e-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8068e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8068e-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8068e-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8068e-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8068e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8068e-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8068e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8068e-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8068e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8068e-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8068e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="8068e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8068e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="8068e-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8068e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="8068e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8068e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8068e-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="8068e-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




