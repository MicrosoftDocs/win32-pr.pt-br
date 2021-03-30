---
title: WM/ContainerFormat
description: O atributo WM/ContainerFormat especifica o tipo de arquivo que é carregado no objeto de chamada.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Formato de mídia do Windows do WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638599"
---
# <a name="wmcontainerformat"></a><span data-ttu-id="9ca4d-104">WM/ContainerFormat</span><span class="sxs-lookup"><span data-stu-id="9ca4d-104">WM/ContainerFormat</span></span>

<span data-ttu-id="9ca4d-105">O atributo **WM/containerFormat** especifica o tipo de arquivo que é carregado no objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-105">The **WM/ContainerFormat** attribute specifies the type of file that is loaded in the calling object.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9ca4d-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="9ca4d-106">Global Constant</span></span>

<span data-ttu-id="9ca4d-107">g \_ wszWMContainerFormat</span><span class="sxs-lookup"><span data-stu-id="9ca4d-107">g\_wszWMContainerFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="9ca4d-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="9ca4d-108">Data Type</span></span>

<span data-ttu-id="9ca4d-109">[**WMT \_ \_formato de armazenamento**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT \_ tipo \_ Binary**)</span><span class="sxs-lookup"><span data-stu-id="9ca4d-109">[**WMT\_STORAGE\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca4d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ca4d-110">Remarks</span></span>

<span data-ttu-id="9ca4d-111">Esse atributo é usado em vez de **IWMProfile3:: GetStorageFormat** e **IWMProfile3:: SetStorageFormat**, que não têm mais suporte.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-111">This attribute is used in place of **IWMProfile3::GetStorageFormat** and **IWMProfile3::SetStorageFormat**, which are no longer supported.</span></span>

<span data-ttu-id="9ca4d-112">Este é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-112">This is a coded attribute.</span></span>

<span data-ttu-id="9ca4d-113">Este atributo não pode ser duplicado no nível do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="9ca4d-114">Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9ca4d-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ca4d-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9ca4d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca4d-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="9ca4d-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




