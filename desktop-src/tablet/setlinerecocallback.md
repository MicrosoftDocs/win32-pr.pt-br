---
description: Define uma função de retorno de chamada a ser usada durante o reconhecimento de linha.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: Função SetLineRecoCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170074"
---
# <a name="setlinerecocallback-function"></a><span data-ttu-id="9437f-103">Função SetLineRecoCallback</span><span class="sxs-lookup"><span data-stu-id="9437f-103">SetLineRecoCallback function</span></span>

<span data-ttu-id="9437f-104">Define uma função de retorno de chamada a ser usada durante o reconhecimento de linha.</span><span class="sxs-lookup"><span data-stu-id="9437f-104">Sets a callback function to be used during line recognition.</span></span>

<span data-ttu-id="9437f-105">Essa função auxiliar não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9437f-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9437f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9437f-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a><span data-ttu-id="9437f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9437f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9437f-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9437f-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9437f-109">Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="9437f-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9437f-110">*PFN*</span><span class="sxs-lookup"><span data-stu-id="9437f-110">*pfn*</span></span> 
</dt> <dd>

<span data-ttu-id="9437f-111">Um ponteiro para uma função que é chamada quando o reconhecimento ocorre no [**InkDivider**](inkdivider-class.md) passado.</span><span class="sxs-lookup"><span data-stu-id="9437f-111">A pointer to a function that is called when recognition occurs on the [**InkDivider**](inkdivider-class.md) passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9437f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9437f-112">Return value</span></span>

<span data-ttu-id="9437f-113">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9437f-113">This function can return one of these values.</span></span>



| <span data-ttu-id="9437f-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9437f-114">Return code</span></span>                                                                                  | <span data-ttu-id="9437f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9437f-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9437f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9437f-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9437f-117">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9437f-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="9437f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9437f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9437f-119">O parâmetro *pDivider* é inválido.</span><span class="sxs-lookup"><span data-stu-id="9437f-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9437f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9437f-120">Remarks</span></span>

<span data-ttu-id="9437f-121">Veja a seguir a sintaxe da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9437f-121">The following is the syntax for the callback function.</span></span>

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a><span data-ttu-id="9437f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9437f-122">Requirements</span></span>



| <span data-ttu-id="9437f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9437f-123">Requirement</span></span> | <span data-ttu-id="9437f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9437f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9437f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9437f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9437f-126">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9437f-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9437f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9437f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9437f-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9437f-128">None supported</span></span><br/>                                                             |
| <span data-ttu-id="9437f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9437f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9437f-130"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9437f-130"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




