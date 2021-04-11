---
title: Busca
description: O atributo pesquisável é um atributo de nível de arquivo que especifica se um aplicativo pode buscar pontos dentro do conteúdo.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato de mídia do Windows pesquisável
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104293847"
---
# <a name="seekable"></a><span data-ttu-id="167dd-104">Busca</span><span class="sxs-lookup"><span data-stu-id="167dd-104">Seekable</span></span>

<span data-ttu-id="167dd-105">O atributo **pesquisável** é um atributo de nível de arquivo que especifica se um aplicativo pode buscar pontos dentro do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="167dd-105">The **Seekable** attribute is a file-level attribute specifying whether an application can seek to points within the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="167dd-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="167dd-106">Global Constant</span></span>

<span data-ttu-id="167dd-107">g \_ wszWMSeekable</span><span class="sxs-lookup"><span data-stu-id="167dd-107">g\_wszWMSeekable</span></span>

## <a name="data-type"></a><span data-ttu-id="167dd-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="167dd-108">Data Type</span></span>

<span data-ttu-id="167dd-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="167dd-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="167dd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="167dd-110">Remarks</span></span>

<span data-ttu-id="167dd-111">Este é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="167dd-111">This is a coded attribute.</span></span>

<span data-ttu-id="167dd-112">Este atributo não pode ser duplicado no nível do arquivo.</span><span class="sxs-lookup"><span data-stu-id="167dd-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="167dd-113">Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="167dd-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="167dd-114">O valor desse atributo para um arquivo pode variar dependendo do objeto expondo a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) usada para recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="167dd-114">The value of this attribute for a file may vary depending upon the object exposing the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface used to retrieve it.</span></span> <span data-ttu-id="167dd-115">Isso ocorre porque os objetos do leitor (síncrono e assíncrono) executam uma verificação mais completa do que o objeto do editor de metadados, para verificar se você pode buscar um ponto em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="167dd-115">This is because the reader objects (both synchronous and asynchronous) perform a more thorough check than the metadata editor object does, to ascertain whether you can seek to a point in a file.</span></span> <span data-ttu-id="167dd-116">O valor de atributo **pesquisável** retornado por um objeto leitor é mais preciso.</span><span class="sxs-lookup"><span data-stu-id="167dd-116">The **Seekable** attribute value returned by a reader object is more accurate.</span></span>

## <a name="see-also"></a><span data-ttu-id="167dd-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="167dd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="167dd-118">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="167dd-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




