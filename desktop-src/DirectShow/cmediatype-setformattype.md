---
description: O método setformatype especifica o tipo de formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Método CMediaType. setformattype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780866"
---
# <a name="cmediatypesetformattype-method"></a><span data-ttu-id="981a6-103">Método CMediaType. setformatype</span><span class="sxs-lookup"><span data-stu-id="981a6-103">CMediaType.SetFormatType method</span></span>

<span data-ttu-id="981a6-104">O método setformattype especifica o tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="981a6-104">The \`\`SetFormatType method specifies the format type.</span></span>

## <a name="syntax"></a><span data-ttu-id="981a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="981a6-105">Syntax</span></span>


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a><span data-ttu-id="981a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="981a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="981a6-107">*pformattype*</span><span class="sxs-lookup"><span data-stu-id="981a6-107">*pformattype*</span></span> 
</dt> <dd>

<span data-ttu-id="981a6-108">Ponteiro para um **GUID** que especifica o tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="981a6-108">Pointer to a **GUID** that specifies the format type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="981a6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="981a6-109">Return value</span></span>

<span data-ttu-id="981a6-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="981a6-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="981a6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="981a6-111">Remarks</span></span>

<span data-ttu-id="981a6-112">Esse método define o membro **formatType** .</span><span class="sxs-lookup"><span data-stu-id="981a6-112">This method sets the **formattype** member.</span></span> <span data-ttu-id="981a6-113">O tipo de formato define o layout do bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="981a6-113">The format type defines the layout of the format block.</span></span> <span data-ttu-id="981a6-114">Por exemplo, se o tipo de formato for FORMAT \_ VIDEOINFO, o bloco de formato deverá conter uma estrutura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="981a6-114">For example, if the format type is FORMAT\_VideoInfo, the format block should contain a **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="981a6-115">Para definir o bloco de formato, chame o método [**CMediaType:: SetFormat**](cmediatype-setformat.md) .</span><span class="sxs-lookup"><span data-stu-id="981a6-115">To set the format block, call the [**CMediaType::SetFormat**](cmediatype-setformat.md) method.</span></span> <span data-ttu-id="981a6-116">O chamador é responsável por verificar se o bloco de formato corresponde ao tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="981a6-116">The caller is responsible for making sure that the format block matches the format type.</span></span>

## <a name="requirements"></a><span data-ttu-id="981a6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="981a6-117">Requirements</span></span>



| <span data-ttu-id="981a6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="981a6-118">Requirement</span></span> | <span data-ttu-id="981a6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="981a6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="981a6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="981a6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="981a6-121"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="981a6-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="981a6-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="981a6-122">Library</span></span><br/> | <dl> <span data-ttu-id="981a6-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="981a6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="981a6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="981a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981a6-125">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="981a6-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 


``
