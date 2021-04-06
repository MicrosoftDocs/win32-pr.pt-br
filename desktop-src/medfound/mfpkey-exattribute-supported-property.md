---
description: Especifica se uma Media Foundation transformação (MFT) copia atributos de exemplos de entrada para exemplos de saída.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Propriedade MFPKEY_EXATTRIBUTE_SUPPORTED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827910"
---
# <a name="mfpkey_exattribute_supported-property"></a><span data-ttu-id="96324-103">\_Propriedade com suporte do FILEATTRIBUTE MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="96324-103">MFPKEY\_EXATTRIBUTE\_SUPPORTED property</span></span>

<span data-ttu-id="96324-104">Especifica se uma Media Foundation transformação (MFT) copia atributos de exemplos de entrada para exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="96324-104">Specifies whether a Media Foundation transform (MFT) copies attributes from input samples to output samples.</span></span>



<span data-ttu-id="96324-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="96324-105">Data type</span></span>

<span data-ttu-id="96324-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="96324-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="96324-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="96324-107">PROPVARIANT member</span></span>

<span data-ttu-id="96324-108">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="96324-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="96324-109">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="96324-109">VT\_BOOL</span></span>

<span data-ttu-id="96324-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="96324-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="96324-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="96324-111">Remarks</span></span>

<span data-ttu-id="96324-112">Esse atributo pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="96324-112">This attribute can have the following values.</span></span>



| <span data-ttu-id="96324-113">Valor</span><span class="sxs-lookup"><span data-stu-id="96324-113">Value</span></span>              | <span data-ttu-id="96324-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="96324-114">Description</span></span>                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96324-115">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="96324-115">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="96324-116">O MFT copia atributos dos exemplos de entrada para os exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="96324-116">The MFT copies attributes from the input samples to the output samples.</span></span>                                                                                 |
| <span data-ttu-id="96324-117">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="96324-117">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="96324-118">A sessão de mídia copia atributos de exemplos de entrada para exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="96324-118">The Media Session copies attributes from input samples to output samples.</span></span> <span data-ttu-id="96324-119">Ele não substitui nenhum atributo que o MFT define na saída Samples.</span><span class="sxs-lookup"><span data-stu-id="96324-119">It does not overwrite any attributes that the MFT sets on the output samples.</span></span> |



 

<span data-ttu-id="96324-120">Para obter esse atributo, chame **QueryInterface** no MFT para a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="96324-120">To get this attribute, call **QueryInterface** on the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="96324-121">O valor padrão é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="96324-121">The default value is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="96324-122">Se o MFT não expor a interface **IPropertyStore** ou se essa propriedade não estiver definida, trate o valor como **variante \_ false**.</span><span class="sxs-lookup"><span data-stu-id="96324-122">If the MFT does not expose the **IPropertyStore** interface, or if this property is not set, treat the value as **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="96324-123">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="96324-123">This property is read-only.</span></span>

> [!NOTE] 
> <span data-ttu-id="96324-124">Este atributo não se aplica a MFTs assíncronas.</span><span class="sxs-lookup"><span data-stu-id="96324-124">This attribute does not apply to asynchronous MFTs.</span></span> <span data-ttu-id="96324-125">Os atributos não serão copiados dos exemplos de entrada para os exemplos de saída para MFTs assíncronas, independentemente do valor desse atributo.</span><span class="sxs-lookup"><span data-stu-id="96324-125">Attributes will not be copied from the input samples to the output samples for asynchronous MFTs, regardless of the value of this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="96324-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96324-126">Examples</span></span>

<span data-ttu-id="96324-127">O exemplo a seguir retornará VARIANT \_ true se um MFT copiar atributos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="96324-127">The following example returns VARIANT\_TRUE if an MFT copies sample attributes.</span></span>


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a><span data-ttu-id="96324-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96324-128">Requirements</span></span>



| <span data-ttu-id="96324-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="96324-129">Requirement</span></span> | <span data-ttu-id="96324-130">Valor</span><span class="sxs-lookup"><span data-stu-id="96324-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96324-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96324-131">Minimum supported client</span></span><br/> | <span data-ttu-id="96324-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96324-132">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96324-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96324-133">Minimum supported server</span></span><br/> | <span data-ttu-id="96324-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96324-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="96324-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96324-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="96324-136"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="96324-136"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96324-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="96324-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96324-138">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96324-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="96324-139">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="96324-139">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="96324-140">**IMFTransform::P rocessOutput**</span><span class="sxs-lookup"><span data-stu-id="96324-140">**IMFTransform::ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




