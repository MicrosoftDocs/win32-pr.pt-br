---
description: Recupera informações de análise do objeto InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: Função CallDivide
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501138"
---
# <a name="calldivide-function"></a><span data-ttu-id="6d9c2-103">Função CallDivide</span><span class="sxs-lookup"><span data-stu-id="6d9c2-103">CallDivide function</span></span>

<span data-ttu-id="6d9c2-104">Recupera informações de análise do objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9c2-104">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="6d9c2-105">Esta função não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d9c2-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9c2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d9c2-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a><span data-ttu-id="6d9c2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d9c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d9c2-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-109">Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9c2-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6d9c2-110">*pWordSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-110">*pWordSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-111">O tamanho da palavra retornada pelo objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9c2-111">The size of the word returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6d9c2-112">*pLineSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-112">*pLineSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-113">O tamanho da linha retornada pelo objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9c2-113">The size of the line returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6d9c2-114">*pParagraphSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-114">*pParagraphSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-115">O tamanho do parágrafo retornado pelo objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9c2-115">The size of the paragraph returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6d9c2-116">*pDrawingSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-116">*pDrawingSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-117">O tamanho do desenho retornado pelo objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9c2-117">The size of the drawing returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6d9c2-118">*pWordCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-118">*pWordCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-119">O número de palavras retornadas pela análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="6d9c2-119">The number of words returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="6d9c2-120">*pLineCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-120">*pLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-121">O número de linhas retornadas pela análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="6d9c2-121">The number of lines returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="6d9c2-122">*pParagraphCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-122">*pParagraphCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9c2-123">O número de parágrafos retornados pela análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="6d9c2-123">The number of paragraphs returned by ink analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d9c2-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d9c2-124">Return value</span></span>

<span data-ttu-id="6d9c2-125">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6d9c2-125">This function can return one of these values.</span></span>



| <span data-ttu-id="6d9c2-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6d9c2-126">Return code</span></span>                                                                                  | <span data-ttu-id="6d9c2-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d9c2-127">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6d9c2-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d9c2-128"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6d9c2-129">A função bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6d9c2-129">The function suceeded.</span></span><br/>              |
| <dl> <span data-ttu-id="6d9c2-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6d9c2-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6d9c2-131">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="6d9c2-131">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6d9c2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d9c2-132">Requirements</span></span>



| <span data-ttu-id="6d9c2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d9c2-133">Requirement</span></span> | <span data-ttu-id="6d9c2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6d9c2-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9c2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d9c2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9c2-136">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6d9c2-136">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6d9c2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d9c2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9c2-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6d9c2-138">None supported</span></span><br/>                                                             |
| <span data-ttu-id="6d9c2-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d9c2-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d9c2-140"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d9c2-140"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




