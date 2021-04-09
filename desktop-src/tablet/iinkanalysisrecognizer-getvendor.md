---
description: Recupera o nome do fornecedor do IInkAnalysisRecognizer.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'Método IInkAnalysisRecognizer:: getvendor (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090533"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a><span data-ttu-id="f1d84-103">Método IInkAnalysisRecognizer:: getvendor</span><span class="sxs-lookup"><span data-stu-id="f1d84-103">IInkAnalysisRecognizer::GetVendor method</span></span>

<span data-ttu-id="f1d84-104">Recupera o nome do fornecedor do [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="f1d84-104">Retrieves the vendor name of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1d84-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1d84-105">Syntax</span></span>


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a><span data-ttu-id="f1d84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1d84-107">*pbstrVendor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f1d84-107">*pbstrVendor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1d84-108">O nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="f1d84-108">The name of the vendor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1d84-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1d84-109">Return value</span></span>

<span data-ttu-id="f1d84-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f1d84-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1d84-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1d84-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f1d84-112">Para evitar um vazamento de memória, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) no \* *pbstrVendor* quando você não precisar mais usar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1d84-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrVendor* when you no longer need to use the string.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1d84-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1d84-113">Requirements</span></span>



| <span data-ttu-id="f1d84-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1d84-114">Requirement</span></span> | <span data-ttu-id="f1d84-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f1d84-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d84-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d84-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d84-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f1d84-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f1d84-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d84-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d84-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f1d84-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f1d84-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1d84-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d84-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d84-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f1d84-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f1d84-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1d84-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1d84-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f1d84-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1d84-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d84-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="f1d84-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="f1d84-126">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="f1d84-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

