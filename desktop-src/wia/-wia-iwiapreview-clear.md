---
description: 'Libera a imagem não filtrada armazenada em cache pelo método IWiaPreview:: GetNewPreview. Ele também libera o filtro de processamento de imagem.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'Método IWiaPreview:: Clear (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813622"
---
# <a name="iwiapreviewclear-method"></a><span data-ttu-id="4f273-104">Método IWiaPreview:: Clear</span><span class="sxs-lookup"><span data-stu-id="4f273-104">IWiaPreview::Clear method</span></span>

<span data-ttu-id="4f273-105">Libera a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="4f273-105">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="4f273-106">Ele também libera o filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="4f273-106">It also releases the image processing filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f273-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f273-107">Syntax</span></span>


```C++
void Clear();
```



## <a name="parameters"></a><span data-ttu-id="4f273-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f273-108">Parameters</span></span>

<span data-ttu-id="4f273-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4f273-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f273-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f273-110">Return value</span></span>

<span data-ttu-id="4f273-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4f273-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f273-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f273-112">Remarks</span></span>

<span data-ttu-id="4f273-113">Em **IWiaPreview:: limpar** o componente de versão prévia do WIA (Windows Image Acquisition) 2,0 libera todos os ponteiros de interface que ele armazena.</span><span class="sxs-lookup"><span data-stu-id="4f273-113">On **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component releases all interface pointers that it stores.</span></span> <span data-ttu-id="4f273-114">O componente de visualização do WIA 2,0 mantém referências a *pWiaItem2* e *PWiaTransferCallback* passados em [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="4f273-114">The WIA 2.0 Preview Component keeps references to *pWiaItem2* and *pWiaTransferCallback* passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="4f273-115">Para ser preciso, o componente de visualização do WIA 2,0 mantém uma referência ao *pWiaItem2* e ao filtro de processamento de imagem do driver, que, por sua vez, mantém uma referência ao *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="4f273-115">To be precise, the WIA 2.0 Preview Component keeps a reference to *pWiaItem2* and the driver's image processing filter, which in turn keeps a reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="4f273-116">Em **IWiaPreview:: Clear**, o componente de visualização do WIA 2,0 também libera sua referência para *pWiaItem2* e para o filtro de processamento de imagem que, por sua vez, libera sua referência para *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="4f273-116">On **IWiaPreview::Clear**, the WIA 2.0 Preview Component also releases its reference to *pWiaItem2* and to the image processing filter, which in turn releases its reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="4f273-117">O componente de visualização do WIA 2,0 exclui a imagem armazenada em cache e não filtrada internamente.</span><span class="sxs-lookup"><span data-stu-id="4f273-117">The WIA 2.0 Preview Component deletes the cached, unfiltered image that it stores internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f273-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f273-118">Requirements</span></span>



| <span data-ttu-id="4f273-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f273-119">Requirement</span></span> | <span data-ttu-id="4f273-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4f273-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f273-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f273-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f273-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f273-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4f273-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f273-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f273-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f273-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4f273-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f273-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f273-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f273-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f273-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="4f273-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f273-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f273-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




