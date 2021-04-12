---
description: A propriedade falha do objeto SWbemRefresher é um valor booliano que indica se o atualizador se reconectará automaticamente a um provedor remoto se a conexão for interrompida.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Propriedade SWbemRefresher. falha (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297913"
---
# <a name="swbemrefresherautoreconnect-property"></a><span data-ttu-id="de9dd-103">Propriedade SWbemRefresher. falha</span><span class="sxs-lookup"><span data-stu-id="de9dd-103">SWbemRefresher.AutoReconnect property</span></span>

<span data-ttu-id="de9dd-104">A propriedade **falha** do objeto [**SWbemRefresher**](swbemrefresher.md) é um valor booliano que indica se o atualizador se reconectará automaticamente a um provedor remoto se a conexão for interrompida.</span><span class="sxs-lookup"><span data-stu-id="de9dd-104">The **AutoReconnect** property of the [**SWbemRefresher**](swbemrefresher.md) object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span>

<span data-ttu-id="de9dd-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="de9dd-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="de9dd-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="de9dd-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de9dd-107">Syntax</span></span>


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a><span data-ttu-id="de9dd-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="de9dd-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="de9dd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="de9dd-109">Remarks</span></span>

<span data-ttu-id="de9dd-110">Modificar essa propriedade afeta apenas os objetos no atualizador que são apoiados por um provedor de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="de9dd-110">Modifying this property affects only objects in the refresher that are backed by a high-performance provider.</span></span> <span data-ttu-id="de9dd-111">Se o provedor não for um provedor de alto desempenho, a definição da propriedade **falha** como **true** não terá efeito porque o objeto [**SWbemRefresher**](swbemrefresher.md) nunca se reconectará.</span><span class="sxs-lookup"><span data-stu-id="de9dd-111">If the provider is not a high-performance provider, then setting the **AutoReconnect** property to **TRUE** has no effect because the [**SWbemRefresher**](swbemrefresher.md) object never reconnects.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9dd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de9dd-112">Requirements</span></span>



| <span data-ttu-id="de9dd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9dd-113">Requirement</span></span> | <span data-ttu-id="de9dd-114">Valor</span><span class="sxs-lookup"><span data-stu-id="de9dd-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de9dd-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de9dd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="de9dd-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de9dd-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de9dd-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de9dd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="de9dd-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de9dd-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de9dd-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de9dd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="de9dd-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de9dd-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de9dd-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de9dd-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="de9dd-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de9dd-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de9dd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="de9dd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de9dd-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de9dd-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="de9dd-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="de9dd-125">CLSID</span></span><br/>                    | <span data-ttu-id="de9dd-126">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="de9dd-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="de9dd-127">IID</span><span class="sxs-lookup"><span data-stu-id="de9dd-127">IID</span></span><br/>                      | <span data-ttu-id="de9dd-128">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="de9dd-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="de9dd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="de9dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9dd-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="de9dd-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




