---
title: Is_Protected
description: O \_ atributo is Protected é um atributo de nível de arquivo que especifica se o conteúdo no arquivo foi protegido usando o DRM (gerenciamento de direitos digitais).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected o formato Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105762485"
---
# <a name="is_protected"></a><span data-ttu-id="8e021-104">É \_ protegido</span><span class="sxs-lookup"><span data-stu-id="8e021-104">Is\_Protected</span></span>

<span data-ttu-id="8e021-105">O atributo **is \_ Protected** é um atributo de nível de arquivo que especifica se o conteúdo no arquivo foi protegido usando o DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="8e021-105">The **Is\_Protected** attribute is a file-level attribute specifying whether the content in the file was protected using digital rights management (DRM).</span></span>

## <a name="global-constant"></a><span data-ttu-id="8e021-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="8e021-106">Global Constant</span></span>

<span data-ttu-id="8e021-107">g \_ wszWMProtected</span><span class="sxs-lookup"><span data-stu-id="8e021-107">g\_wszWMProtected</span></span>

## <a name="data-type"></a><span data-ttu-id="8e021-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="8e021-108">Data Type</span></span>

<span data-ttu-id="8e021-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="8e021-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="8e021-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e021-110">Remarks</span></span>

<span data-ttu-id="8e021-111">Este é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="8e021-111">This is a coded attribute.</span></span> <span data-ttu-id="8e021-112">A recuperação dessa propriedade fornece as mesmas informações que chamam [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span><span class="sxs-lookup"><span data-stu-id="8e021-112">Retrieving this property provides the same information as calling [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span></span>

<span data-ttu-id="8e021-113">Este atributo não pode ser duplicado no nível do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e021-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="8e021-114">Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="8e021-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e021-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e021-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e021-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="8e021-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




