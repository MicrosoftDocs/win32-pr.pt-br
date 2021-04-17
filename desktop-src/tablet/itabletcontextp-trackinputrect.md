---
description: Atualiza o Tablet digitalizador para as coordenadas de mapeamento de local de janela.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'Método ITabletContextP:: TrackInputRect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790372"
---
# <a name="itabletcontextptrackinputrect-method"></a><span data-ttu-id="baf7f-103">Método ITabletContextP:: TrackInputRect</span><span class="sxs-lookup"><span data-stu-id="baf7f-103">ITabletContextP::TrackInputRect method</span></span>

<span data-ttu-id="baf7f-104">Atualiza o Tablet digitalizador para as coordenadas de mapeamento de local de janela.</span><span class="sxs-lookup"><span data-stu-id="baf7f-104">Updates the tablet digitizer to window location mapping coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baf7f-105">Syntax</span></span>


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="baf7f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baf7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baf7f-107">*prcInput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="baf7f-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="baf7f-108">O novo retângulo de janela de entrada depois de atualizar o mapeamento entre as coordenadas de janela e digitalizador.</span><span class="sxs-lookup"><span data-stu-id="baf7f-108">The new input window rectangle after updating the mapping between the window and digitizer coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baf7f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baf7f-109">Return value</span></span>

<span data-ttu-id="baf7f-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="baf7f-110">This method can return one of these values.</span></span>



| <span data-ttu-id="baf7f-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="baf7f-111">Return code</span></span>                                                                            | <span data-ttu-id="baf7f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="baf7f-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="baf7f-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="baf7f-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="baf7f-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="baf7f-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="baf7f-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="baf7f-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="baf7f-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="baf7f-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="baf7f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="baf7f-117">Remarks</span></span>

<span data-ttu-id="baf7f-118">Chame esse método sempre que o local da janela na tela for alterado.</span><span class="sxs-lookup"><span data-stu-id="baf7f-118">Call this method anytime the location of the window on the screen changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="baf7f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baf7f-119">Requirements</span></span>



| <span data-ttu-id="baf7f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="baf7f-120">Requirement</span></span> | <span data-ttu-id="baf7f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="baf7f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="baf7f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baf7f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="baf7f-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="baf7f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="baf7f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baf7f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="baf7f-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="baf7f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="baf7f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="baf7f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="baf7f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="baf7f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baf7f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="baf7f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf7f-129">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="baf7f-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




