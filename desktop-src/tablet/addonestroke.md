---
description: Adiciona um novo objeto IInkStrokeDisp ao objeto InkDivider que foi passado.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: Função AddOneStroke
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457194"
---
# <a name="addonestroke-function"></a><span data-ttu-id="1672e-103">Função AddOneStroke</span><span class="sxs-lookup"><span data-stu-id="1672e-103">AddOneStroke function</span></span>

<span data-ttu-id="1672e-104">Adiciona um novo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ao objeto [**InkDivider**](inkdivider-class.md) que foi passado.</span><span class="sxs-lookup"><span data-stu-id="1672e-104">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>

<span data-ttu-id="1672e-105">Esta função não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1672e-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1672e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1672e-106">Syntax</span></span>


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a><span data-ttu-id="1672e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1672e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1672e-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1672e-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1672e-109">Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1672e-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1672e-110">*strokeid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1672e-110">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1672e-111">A [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) do objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) a ser adicionado ao objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1672e-111">The [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to be added to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1672e-112">*CPoints* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1672e-112">*cPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1672e-113">O número de pacotes que compõem o novo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="1672e-113">The number of packets that make up the new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="1672e-114">*aPoints* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1672e-114">*aPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1672e-115">A matriz de pacotes que compõe o objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) em *strokeid*.</span><span class="sxs-lookup"><span data-stu-id="1672e-115">The array of packets that make up the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object in *strokeId*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1672e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1672e-116">Return value</span></span>

<span data-ttu-id="1672e-117">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1672e-117">This function can return one of these values.</span></span>



| <span data-ttu-id="1672e-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1672e-118">Return code</span></span>                                                                                  | <span data-ttu-id="1672e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="1672e-119">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1672e-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1672e-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1672e-121">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1672e-121">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="1672e-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1672e-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1672e-123">O parâmetro *hDivider* é inválido.</span><span class="sxs-lookup"><span data-stu-id="1672e-123">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1672e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1672e-124">Requirements</span></span>



| <span data-ttu-id="1672e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1672e-125">Requirement</span></span> | <span data-ttu-id="1672e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1672e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1672e-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1672e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1672e-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1672e-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1672e-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1672e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1672e-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1672e-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="1672e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1672e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="1672e-132"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1672e-132"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




