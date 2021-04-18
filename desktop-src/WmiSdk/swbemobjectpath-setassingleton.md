---
description: O método SetAsSingleton do objeto SWbemObjectPath força o caminho para endereçar uma instância WMI singleton de uma classe. Uma classe singleton é uma classe que nunca pode ter mais de uma instância.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Método SWbemObjectPath. SetAsSingleton (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780696"
---
# <a name="swbemobjectpathsetassingleton-method"></a><span data-ttu-id="2ec39-104">Método SWbemObjectPath. SetAsSingleton</span><span class="sxs-lookup"><span data-stu-id="2ec39-104">SWbemObjectPath.SetAsSingleton method</span></span>

<span data-ttu-id="2ec39-105">O método **SetAsSingleton** do objeto [**SWbemObjectPath**](swbemobjectpath.md) força o caminho para endereçar uma instância WMI singleton de uma classe.</span><span class="sxs-lookup"><span data-stu-id="2ec39-105">The **SetAsSingleton** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a singleton WMI instance of a class.</span></span> <span data-ttu-id="2ec39-106">Uma classe singleton é uma classe que nunca pode ter mais de uma instância.</span><span class="sxs-lookup"><span data-stu-id="2ec39-106">A singleton class is a class that can never have more than one instance.</span></span>

<span data-ttu-id="2ec39-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2ec39-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span> <span data-ttu-id="2ec39-108">SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="2ec39-108">SWbemObjectPath</span></span>

## <a name="syntax"></a><span data-ttu-id="2ec39-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ec39-109">Syntax</span></span>


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a><span data-ttu-id="2ec39-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ec39-110">Parameters</span></span>

<span data-ttu-id="2ec39-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2ec39-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ec39-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ec39-112">Return value</span></span>

<span data-ttu-id="2ec39-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2ec39-113">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ec39-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2ec39-114">Error codes</span></span>

<span data-ttu-id="2ec39-115">Após a conclusão do método **SetAsSingleton** , o objeto **Err** pode conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="2ec39-115">Upon completion of the **SetAsSingleton** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="2ec39-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2ec39-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2ec39-117">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="2ec39-117">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ec39-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ec39-118">Requirements</span></span>



| <span data-ttu-id="2ec39-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ec39-119">Requirement</span></span> | <span data-ttu-id="2ec39-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2ec39-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec39-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ec39-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2ec39-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ec39-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ec39-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ec39-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2ec39-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ec39-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ec39-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ec39-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ec39-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ec39-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ec39-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2ec39-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ec39-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ec39-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2ec39-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2ec39-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ec39-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ec39-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2ec39-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="2ec39-131">CLSID</span></span><br/>                    | <span data-ttu-id="2ec39-132">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="2ec39-132">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="2ec39-133">IID</span><span class="sxs-lookup"><span data-stu-id="2ec39-133">IID</span></span><br/>                      | <span data-ttu-id="2ec39-134">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="2ec39-134">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




