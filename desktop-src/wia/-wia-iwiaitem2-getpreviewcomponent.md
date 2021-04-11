---
description: Obtém o componente de versão prévia do WIA (Windows Image Acquisition) 2,0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'Método IWiaItem2:: GetPreviewComponent (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090507"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a><span data-ttu-id="8dd8a-103">Método IWiaItem2:: GetPreviewComponent</span><span class="sxs-lookup"><span data-stu-id="8dd8a-103">IWiaItem2::GetPreviewComponent method</span></span>

<span data-ttu-id="8dd8a-104">Obtém o componente de versão prévia do WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-104">Gets the Windows Image Acquisition (WIA) 2.0 preview component.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dd8a-105">Syntax</span></span>


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a><span data-ttu-id="8dd8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dd8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dd8a-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="8dd8a-108">Type: **LONG**</span></span>

<span data-ttu-id="8dd8a-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-109">Not used.</span></span> <span data-ttu-id="8dd8a-110">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-111">*ppWiaPreview* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-111">*ppWiaPreview* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-112">Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-112">Type: **[**IWiaPreview**](-wia-iwiapreview.md)\*\***</span></span>

<span data-ttu-id="8dd8a-113">Retorna o endereço de um ponteiro para a interface [**IWiaPreview**](-wia-iwiapreview.md) do componente de visualização.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-113">Returns the address of a pointer to the [**IWiaPreview**](-wia-iwiapreview.md) interface of the preview component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dd8a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8dd8a-114">Return value</span></span>

<span data-ttu-id="8dd8a-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8dd8a-115">Type: **HRESULT**</span></span>

<span data-ttu-id="8dd8a-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8dd8a-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8dd8a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dd8a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dd8a-118">Remarks</span></span>

<span data-ttu-id="8dd8a-119">Use essa função para retornar um ponteiro para o endereço do componente de visualização do WIA 2,0 para qualquer objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore de objetos de um dispositivo de hardware WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-119">Use this function to return a pointer to the address of the WIA 2.0 preview component for any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device.</span></span>

<span data-ttu-id="8dd8a-120">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppWiaPreview* .</span><span class="sxs-lookup"><span data-stu-id="8dd8a-120">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppWiaPreview* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dd8a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dd8a-121">Requirements</span></span>



| <span data-ttu-id="8dd8a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dd8a-122">Requirement</span></span> | <span data-ttu-id="8dd8a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8dd8a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd8a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dd8a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8dd8a-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8dd8a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dd8a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8dd8a-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8dd8a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8dd8a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dd8a-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dd8a-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8dd8a-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="8dd8a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8dd8a-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8dd8a-131"><dt>Wia.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dd8a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dd8a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd8a-133">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="8dd8a-133">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="8dd8a-134">**IWiaPreview**</span><span class="sxs-lookup"><span data-stu-id="8dd8a-134">**IWiaPreview**</span></span>](-wia-iwiapreview.md)
</dt> </dl>

 

 
