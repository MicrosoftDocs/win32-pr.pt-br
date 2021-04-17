---
title: HasAttachedImages
description: O atributo HasAttachedImages é um atributo em nível de arquivo que especifica se o arquivo é um arquivo MP3 com quadros APIC ID3 anexados.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Formato de mídia do Windows HasAttachedImages
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105811527"
---
# <a name="hasattachedimages"></a><span data-ttu-id="eb8d4-104">HasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="eb8d4-104">HasAttachedImages</span></span>

<span data-ttu-id="eb8d4-105">O atributo **HasAttachedImages** é um atributo em nível de arquivo que especifica se o arquivo é um arquivo MP3 com quadros APIC ID3 anexados.</span><span class="sxs-lookup"><span data-stu-id="eb8d4-105">The **HasAttachedImages** attribute is a file-level attribute specifying whether the file is an MP3 file with attached APIC ID3 frames.</span></span>

## <a name="global-constant"></a><span data-ttu-id="eb8d4-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="eb8d4-106">Global Constant</span></span>

<span data-ttu-id="eb8d4-107">g \_ wszWMHasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="eb8d4-107">g\_wszWMHasAttachedImages</span></span>

## <a name="data-type"></a><span data-ttu-id="eb8d4-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="eb8d4-108">Data Type</span></span>

<span data-ttu-id="eb8d4-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="eb8d4-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="eb8d4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb8d4-110">Remarks</span></span>

<span data-ttu-id="eb8d4-111">Este é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="eb8d4-111">This is a coded attribute.</span></span>

<span data-ttu-id="eb8d4-112">Este atributo não pode ser duplicado no nível do arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb8d4-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="eb8d4-113">Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="eb8d4-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="eb8d4-114">O **HasAttachedImages** foi projetado para informar um aplicativo de que as imagens estavam presentes para que pudessem ser recuperadas usando a interface [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) .</span><span class="sxs-lookup"><span data-stu-id="eb8d4-114">**HasAttachedImages** was designed to inform an application that images were present so that they could be retrieved using the [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) interface.</span></span> <span data-ttu-id="eb8d4-115">Agora que as imagens têm suporte usando o atributo [**WM/Picture**](wmpicture.md) , o **HasAttachedImages** não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="eb8d4-115">Now that images are supported using the [**WM/Picture**](wmpicture.md) attribute, **HasAttachedImages** is no longer needed.</span></span>

<span data-ttu-id="eb8d4-116">Para determinar se um arquivo contém imagens, chame [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) especificando o atributo **WM/Picture** .</span><span class="sxs-lookup"><span data-stu-id="eb8d4-116">To determine whether a file contains images, call [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specifying the **WM/Picture** attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb8d4-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb8d4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8d4-118">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="eb8d4-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




