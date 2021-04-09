---
title: Propriedade WSMan. Error (WSManDisp. h)
description: Obtém informações de erro adicionais, em um fluxo XML, para a chamada anterior para um método WSMan se Gerenciamento Remoto do Windows serviço não pôde criar um objeto de sessão, um objeto ConnectionOptions ou um objeto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de propriedade de erro
- Propriedade de erro Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, Propriedade Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085597"
---
# <a name="wsmanerror-property"></a><span data-ttu-id="30c6d-106">Propriedade WSMan. Error</span><span class="sxs-lookup"><span data-stu-id="30c6d-106">WSMan.Error property</span></span>

<span data-ttu-id="30c6d-107">Obtém informações de erro adicionais, em um fluxo XML, para a chamada anterior para um método [**WSMan**](wsman.md) se gerenciamento remoto do Windows serviço não pôde criar um objeto de [**sessão**](session.md) , um objeto [**ConnectionOptions**](connectionoptions.md) ou um objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="30c6d-107">Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.</span></span>

<span data-ttu-id="30c6d-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="30c6d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c6d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30c6d-109">Syntax</span></span>


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="30c6d-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="30c6d-110">Property value</span></span>

<span data-ttu-id="30c6d-111">A representação XML das informações de erro.</span><span class="sxs-lookup"><span data-stu-id="30c6d-111">The XML representation of the error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c6d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30c6d-112">Requirements</span></span>



| <span data-ttu-id="30c6d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="30c6d-113">Requirement</span></span> | <span data-ttu-id="30c6d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="30c6d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30c6d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30c6d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="30c6d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30c6d-116">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="30c6d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30c6d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="30c6d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30c6d-118">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="30c6d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30c6d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c6d-120"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c6d-120"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="30c6d-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="30c6d-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30c6d-122"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30c6d-122"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="30c6d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30c6d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="30c6d-124"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30c6d-124"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30c6d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="30c6d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c6d-126"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c6d-126"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30c6d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="30c6d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c6d-128">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="30c6d-128">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





