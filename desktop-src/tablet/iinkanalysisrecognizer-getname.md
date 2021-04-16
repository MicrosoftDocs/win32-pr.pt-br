---
description: Recupera o nome do reconhecedor.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'Método IInkAnalysisRecognizer:: GetName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750401"
---
# <a name="iinkanalysisrecognizergetname-method"></a><span data-ttu-id="b7887-103">Método IInkAnalysisRecognizer:: GetName</span><span class="sxs-lookup"><span data-stu-id="b7887-103">IInkAnalysisRecognizer::GetName method</span></span>

<span data-ttu-id="b7887-104">Recupera o nome do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="b7887-104">Retrieves the name of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7887-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7887-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="b7887-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7887-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7887-107">*pbstrName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b7887-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7887-108">O nome do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="b7887-108">The name of the recognizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7887-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7887-109">Return value</span></span>

<span data-ttu-id="b7887-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b7887-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7887-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7887-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b7887-112">Para evitar um vazamento de memória, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) no \* *pbstrName* quando você não precisar mais usar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7887-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrName* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="b7887-113">O nome é localizado para a linguagem neutra de região para a qual o reconhecedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="b7887-113">The name is localized for the region-neutral language that the recognizer supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7887-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7887-114">Requirements</span></span>



| <span data-ttu-id="b7887-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7887-115">Requirement</span></span> | <span data-ttu-id="b7887-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b7887-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7887-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7887-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7887-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b7887-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7887-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7887-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7887-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b7887-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b7887-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7887-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7887-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b7887-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b7887-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b7887-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7887-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7887-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b7887-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7887-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7887-126">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="b7887-126">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b7887-127">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b7887-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

