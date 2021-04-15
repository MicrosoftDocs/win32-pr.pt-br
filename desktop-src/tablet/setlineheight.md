---
description: Define a propriedade LineHeight no objeto InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: Função SetLineHeight
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761640"
---
# <a name="setlineheight-function"></a><span data-ttu-id="e5ad1-103">Função SetLineHeight</span><span class="sxs-lookup"><span data-stu-id="e5ad1-103">SetLineHeight function</span></span>

<span data-ttu-id="e5ad1-104">Define a propriedade [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) no objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ad1-104">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="e5ad1-105">Essa função auxiliar não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5ad1-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ad1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5ad1-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a><span data-ttu-id="e5ad1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5ad1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ad1-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5ad1-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad1-109">Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ad1-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad1-110">*lLineHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5ad1-110">*lLineHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad1-111">A propriedade [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) do objeto [**InkDivider**](inkdivider-class.md) , em unidades HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="e5ad1-111">The [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property of the [**InkDivider**](inkdivider-class.md) object, in HIMETRIC units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ad1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5ad1-112">Return value</span></span>

<span data-ttu-id="e5ad1-113">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e5ad1-113">This function can return one of these values.</span></span>



| <span data-ttu-id="e5ad1-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e5ad1-114">Return code</span></span>                                                                                  | <span data-ttu-id="e5ad1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5ad1-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e5ad1-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad1-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e5ad1-117">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e5ad1-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="e5ad1-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e5ad1-119">O parâmetro *pDivider* é inválido.</span><span class="sxs-lookup"><span data-stu-id="e5ad1-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5ad1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5ad1-120">Requirements</span></span>



| <span data-ttu-id="e5ad1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5ad1-121">Requirement</span></span> | <span data-ttu-id="e5ad1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e5ad1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ad1-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5ad1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ad1-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e5ad1-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e5ad1-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5ad1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ad1-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e5ad1-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="e5ad1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5ad1-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5ad1-128"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad1-128"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 
