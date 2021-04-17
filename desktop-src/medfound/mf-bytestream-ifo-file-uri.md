---
description: 'Contém a URL do arquivo IFO (informações de DVD) especificado pelo servidor HTTP no cabeçalho HTTP, &\# 0034; Pragma: ifoFileURI.dlna.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Atributo MF_BYTESTREAM_IFO_FILE_URI (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792575"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a><span data-ttu-id="661e7-103">\_Atributo de \_ \_ URI de arquivo MF bytes IFO \_</span><span class="sxs-lookup"><span data-stu-id="661e7-103">MF\_BYTESTREAM\_IFO\_FILE\_URI attribute</span></span>

<span data-ttu-id="661e7-104">Contém a URL do arquivo IFO (informações de DVD) especificado pelo servidor HTTP no cabeçalho HTTP, "pragma: ifoFileURI.dlna.org".</span><span class="sxs-lookup"><span data-stu-id="661e7-104">Contains the URL of the IFO (DVD Information) file specified by the HTTP server in the HTTP header, "Pragma: ifoFileURI.dlna.org".</span></span>

## <a name="data-type"></a><span data-ttu-id="661e7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="661e7-105">Data type</span></span>

<span data-ttu-id="661e7-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="661e7-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="661e7-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="661e7-107">Get/set</span></span>

<span data-ttu-id="661e7-108">Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="661e7-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="661e7-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="661e7-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="661e7-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="661e7-110">Applies to</span></span>

[<span data-ttu-id="661e7-111">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="661e7-111">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="661e7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="661e7-112">Remarks</span></span>

<span data-ttu-id="661e7-113">O fluxo de bytes HTTP pesquisa o cabeçalho HTTP para a cadeia de caracteres "ifoFileURI.dlna.org".</span><span class="sxs-lookup"><span data-stu-id="661e7-113">The HTTP byte stream searches the HTTP header for the "ifoFileURI.dlna.org" string.</span></span> <span data-ttu-id="661e7-114">Se a cadeia de caracteres for encontrada, ela será copiada para esse atributo no fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="661e7-114">If the string is found, it is copied to this attribute on the byte stream.</span></span>

<span data-ttu-id="661e7-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="661e7-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="661e7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="661e7-116">Requirements</span></span>



| <span data-ttu-id="661e7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="661e7-117">Requirement</span></span> | <span data-ttu-id="661e7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="661e7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="661e7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="661e7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="661e7-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="661e7-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                                        |
| <span data-ttu-id="661e7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="661e7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="661e7-122">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="661e7-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="661e7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="661e7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="661e7-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="661e7-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661e7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="661e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661e7-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="661e7-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="661e7-127">Atributos de fluxo de bytes</span><span class="sxs-lookup"><span data-stu-id="661e7-127">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="661e7-128">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="661e7-128">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




