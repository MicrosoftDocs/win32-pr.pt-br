---
description: Recupera as propriedades de ID dos objetos IInkStrokeDisp da palavra, da linha, do parágrafo ou do desenho correspondente determinado pela análise de tinta.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Função CallDivideResultsStrokeIds
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773013"
---
# <a name="calldivideresultsstrokeids-function"></a><span data-ttu-id="fe903-103">Função CallDivideResultsStrokeIds</span><span class="sxs-lookup"><span data-stu-id="fe903-103">CallDivideResultsStrokeIds function</span></span>

<span data-ttu-id="fe903-104">Recupera as propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) dos objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da palavra, da linha, do parágrafo ou do desenho correspondente determinado pela análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="fe903-104">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span>

<span data-ttu-id="fe903-105">Esta função não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fe903-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe903-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe903-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a><span data-ttu-id="fe903-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe903-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe903-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe903-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe903-109">Um identificador para o objeto [divisória](the-divider-object.md) .</span><span class="sxs-lookup"><span data-stu-id="fe903-109">A handle to the [Divider](the-divider-object.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="fe903-110">*\[ aWordStrokeIds \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="fe903-110">*aWordStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe903-111">Uma matriz das IDs de traço da tinta na palavra.</span><span class="sxs-lookup"><span data-stu-id="fe903-111">An array of the stroke IDs of the ink in the word.</span></span>

</dd> <dt>

<span data-ttu-id="fe903-112">*\[ aLineStrokeIds \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="fe903-112">*aLineStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe903-113">Uma matriz das IDs de traço da tinta na linha.</span><span class="sxs-lookup"><span data-stu-id="fe903-113">An array of the stroke IDs of the ink in the line.</span></span>

</dd> <dt>

<span data-ttu-id="fe903-114">*\[ aParagraphStrokeIds \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="fe903-114">*aParagraphStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe903-115">Uma matriz das IDs de traço da tinta no parágrafo.</span><span class="sxs-lookup"><span data-stu-id="fe903-115">An array of the stroke IDs of the ink in the paragraph.</span></span>

</dd> <dt>

<span data-ttu-id="fe903-116">*\[ aDrawingStrokeIds \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="fe903-116">*aDrawingStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe903-117">Uma matriz das IDs de traço da tinta no desenho.</span><span class="sxs-lookup"><span data-stu-id="fe903-117">An array of the stroke IDs of the ink in the drawing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe903-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe903-118">Return value</span></span>

<span data-ttu-id="fe903-119">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="fe903-119">This function can return one of these values.</span></span>



| <span data-ttu-id="fe903-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fe903-120">Return code</span></span>                                                                                  | <span data-ttu-id="fe903-121">Description</span><span class="sxs-lookup"><span data-stu-id="fe903-121">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="fe903-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe903-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fe903-123">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fe903-123">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="fe903-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fe903-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fe903-125">O parâmetro *hDivider* é inválido.</span><span class="sxs-lookup"><span data-stu-id="fe903-125">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe903-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe903-126">Requirements</span></span>



| <span data-ttu-id="fe903-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe903-127">Requirement</span></span> | <span data-ttu-id="fe903-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fe903-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe903-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe903-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fe903-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fe903-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fe903-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe903-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fe903-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fe903-132">None supported</span></span><br/>                                                             |
| <span data-ttu-id="fe903-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe903-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe903-134"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe903-134"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




