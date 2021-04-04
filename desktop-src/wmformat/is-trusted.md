---
title: Is_Trusted
description: O \_ atributo is Trusted é um atributo de nível de arquivo que especifica se a URL de aquisição de licença no arquivo é confiável.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted o formato Windows Media
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916820"
---
# <a name="is_trusted"></a><span data-ttu-id="6f3f6-104">É \_ confiável</span><span class="sxs-lookup"><span data-stu-id="6f3f6-104">Is\_Trusted</span></span>

<span data-ttu-id="6f3f6-105">O atributo **is \_ Trusted** é um atributo de nível de arquivo que especifica se a URL de aquisição de licença no arquivo é confiável.</span><span class="sxs-lookup"><span data-stu-id="6f3f6-105">The **Is\_Trusted** attribute is a file-level attribute specifying whether the license acquisition URL in the file is trusted.</span></span>

## <a name="global-constant"></a><span data-ttu-id="6f3f6-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="6f3f6-106">Global Constant</span></span>

<span data-ttu-id="6f3f6-107">g \_ wszWMTrusted</span><span class="sxs-lookup"><span data-stu-id="6f3f6-107">g\_wszWMTrusted</span></span>

## <a name="data-type"></a><span data-ttu-id="6f3f6-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="6f3f6-108">Data Type</span></span>

<span data-ttu-id="6f3f6-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6f3f6-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f3f6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f3f6-110">Remarks</span></span>

<span data-ttu-id="6f3f6-111">Este é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="6f3f6-111">This is a coded attribute.</span></span>

<span data-ttu-id="6f3f6-112">Antes de navegar para uma URL de aquisição de licença contida em um arquivo protegido por DRM, um aplicativo deve primeiro verificar se essa propriedade é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="6f3f6-112">Before navigating to a license acquisition URL contained in a DRM-protected file, an application should first verify that this property is true.</span></span> <span data-ttu-id="6f3f6-113">Se for false, o aplicativo deverá notificar o usuário de que a URL possivelmente foi adulterada.</span><span class="sxs-lookup"><span data-stu-id="6f3f6-113">If it is false, the application should notify the user that the URL has possibly been tampered with.</span></span>

<span data-ttu-id="6f3f6-114">Este atributo não pode ser duplicado no nível do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6f3f6-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="6f3f6-115">Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="6f3f6-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f3f6-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f3f6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3f6-117">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="6f3f6-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




