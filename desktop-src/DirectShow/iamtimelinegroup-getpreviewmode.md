---
description: O método getpreviewmode recupera o modo de visualização para o grupo.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'Método IAMTimelineGroup:: getpreviewmode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768793"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a><span data-ttu-id="697cc-103">Método IAMTimelineGroup:: getpreviewmode</span><span class="sxs-lookup"><span data-stu-id="697cc-103">IAMTimelineGroup::GetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="697cc-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="697cc-104">\[Deprecated.</span></span> <span data-ttu-id="697cc-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="697cc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="697cc-106">O `GetPreviewMode` método recupera o modo de visualização para o grupo.</span><span class="sxs-lookup"><span data-stu-id="697cc-106">The `GetPreviewMode` method retrieves the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="697cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="697cc-107">Syntax</span></span>


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a><span data-ttu-id="697cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="697cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="697cc-109">*pfPreview*</span><span class="sxs-lookup"><span data-stu-id="697cc-109">*pfPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="697cc-110">Recebe um valor booliano que indica o modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="697cc-110">Receives a Boolean value indicating the preview mode.</span></span> <span data-ttu-id="697cc-111">Se for **true**, o grupo estará no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="697cc-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="697cc-112">Se for **false**, o grupo estará no modo de criação.</span><span class="sxs-lookup"><span data-stu-id="697cc-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="697cc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="697cc-113">Return value</span></span>

<span data-ttu-id="697cc-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="697cc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="697cc-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="697cc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="697cc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="697cc-116">Remarks</span></span>

<span data-ttu-id="697cc-117">No modo de visualização, os quadros são removidos durante efeitos lentos ou transições para manter o vídeo sincronizado com o áudio.</span><span class="sxs-lookup"><span data-stu-id="697cc-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="697cc-118">O vídeo pode parecer instável como resultado.</span><span class="sxs-lookup"><span data-stu-id="697cc-118">The video might look choppy as a result.</span></span> <span data-ttu-id="697cc-119">No modo de criação, cada quadro é renderizado.</span><span class="sxs-lookup"><span data-stu-id="697cc-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="697cc-120">O modo de criação é apropriado para gravar arquivos; para visualização na tela, o vídeo pode ficar fora de sincronia com o áudio.</span><span class="sxs-lookup"><span data-stu-id="697cc-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might become out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="697cc-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="697cc-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="697cc-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="697cc-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="697cc-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="697cc-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="697cc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="697cc-124">Requirements</span></span>



| <span data-ttu-id="697cc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="697cc-125">Requirement</span></span> | <span data-ttu-id="697cc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="697cc-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="697cc-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="697cc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="697cc-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="697cc-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="697cc-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="697cc-129">Library</span></span><br/> | <dl> <span data-ttu-id="697cc-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="697cc-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="697cc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="697cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="697cc-132">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="697cc-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="697cc-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="697cc-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




