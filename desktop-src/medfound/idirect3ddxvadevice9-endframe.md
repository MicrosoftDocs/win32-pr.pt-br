---
description: Encerra o processamento para criar uma imagem decodificada.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'Método IDirect3DDXVADevice9:: endframe (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090968"
---
# <a name="idirect3ddxvadevice9endframe-method"></a><span data-ttu-id="b770f-103">Método IDirect3DDXVADevice9:: endframe</span><span class="sxs-lookup"><span data-stu-id="b770f-103">IDirect3DDXVADevice9::EndFrame method</span></span>

<span data-ttu-id="b770f-104">Encerra o processamento para criar uma imagem decodificada.</span><span class="sxs-lookup"><span data-stu-id="b770f-104">Ends the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b770f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b770f-105">Syntax</span></span>


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a><span data-ttu-id="b770f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b770f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b770f-107">*SizeMiscData*</span><span class="sxs-lookup"><span data-stu-id="b770f-107">*SizeMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="b770f-108">O tamanho do buffer especificado por *pMiscData*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b770f-108">The size of the buffer specified by *pMiscData*, in bytes.</span></span> <span data-ttu-id="b770f-109">O valor deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="b770f-109">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="b770f-110">*pMiscData*</span><span class="sxs-lookup"><span data-stu-id="b770f-110">*pMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="b770f-111">Ponteiro para um buffer que contém dados para o acelerador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b770f-111">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="b770f-112">Esse buffer deve conter o mesmo índice de quadro que foi passado para o método [**IDirect3DDXVADevice9:: BeginFrame**](idirect3ddxvadevice9-beginframe.md) no parâmetro *pInputData* .</span><span class="sxs-lookup"><span data-stu-id="b770f-112">This buffer must contain the same frame index that was passed to the [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) method in the *pInputData* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b770f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b770f-113">Return value</span></span>

<span data-ttu-id="b770f-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b770f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b770f-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b770f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b770f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b770f-116">Requirements</span></span>



| <span data-ttu-id="b770f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b770f-117">Requirement</span></span> | <span data-ttu-id="b770f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b770f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b770f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b770f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b770f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b770f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b770f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b770f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b770f-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b770f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b770f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b770f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b770f-124"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b770f-124"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b770f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b770f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b770f-126">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="b770f-126">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




