---
description: Atributos de fluxo de bytes
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Atributos de fluxo de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761145"
---
# <a name="byte-stream-attributes"></a><span data-ttu-id="24f5a-103">Atributos de fluxo de bytes</span><span class="sxs-lookup"><span data-stu-id="24f5a-103">Byte Stream Attributes</span></span>

<span data-ttu-id="24f5a-104">Os atributos a seguir se aplicam a alguns fluxos de bytes.</span><span class="sxs-lookup"><span data-stu-id="24f5a-104">The following attributes apply to some byte streams.</span></span> <span data-ttu-id="24f5a-105">Para descobrir se um fluxo de bytes dá suporte a atributos, consulte o objeto de fluxo de bytes para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="24f5a-105">To find out whether a byte stream supports attributes, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>



| <span data-ttu-id="24f5a-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="24f5a-106">Attribute</span></span>                                                                                  | <span data-ttu-id="24f5a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="24f5a-107">Description</span></span>                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="24f5a-108">**\_tipo de \_ conteúdo \_ bytes MF**</span><span class="sxs-lookup"><span data-stu-id="24f5a-108">**MF\_BYTESTREAM\_CONTENT\_TYPE**</span></span>](mf-bytestream-content-type-attribute.md)              | <span data-ttu-id="24f5a-109">Especifica o tipo MIME de um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="24f5a-109">Specifies the MIME type of a byte stream.</span></span>                         |
| [<span data-ttu-id="24f5a-110">**\_duração de bytes MF \_**</span><span class="sxs-lookup"><span data-stu-id="24f5a-110">**MF\_BYTESTREAM\_DURATION**</span></span>](mf-bytestream-duration-attribute.md)                       | <span data-ttu-id="24f5a-111">Especifica a duração de um fluxo de bytes, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="24f5a-111">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="24f5a-112">\_URI do arquivo MF bytes \_ IFO \_ \_</span><span class="sxs-lookup"><span data-stu-id="24f5a-112">MF\_BYTESTREAM\_IFO\_FILE\_URI</span></span>](mf-bytestream-ifo-file-uri.md)                           | <span data-ttu-id="24f5a-113">Especifica a URL de um arquivo IFO associado.</span><span class="sxs-lookup"><span data-stu-id="24f5a-113">Specifies the URL of an associated IFO file.</span></span>                      |
| [<span data-ttu-id="24f5a-114">**\_hora da \_ última \_ modificação \_ do MF bytes**</span><span class="sxs-lookup"><span data-stu-id="24f5a-114">**MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME**</span></span>](mf-bytestream-last-modified-time-attribute.md) | <span data-ttu-id="24f5a-115">Especifica quando um fluxo de bytes foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="24f5a-115">Specifies when a byte stream was last modified.</span></span>                   |
| [<span data-ttu-id="24f5a-116">**nome da origem do MF \_ bytes \_ \_**</span><span class="sxs-lookup"><span data-stu-id="24f5a-116">**MF\_BYTESTREAM\_ORIGIN\_NAME**</span></span>](mf-bytestream-origin-name-attribute.md)                | <span data-ttu-id="24f5a-117">Especifica a URL original para um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="24f5a-117">Specifies the original URL for a byte stream.</span></span>                     |



 

<span data-ttu-id="24f5a-118">Os atributos a seguir se aplicam a manipuladores de fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="24f5a-118">The following attributes apply to byte-stream handlers.</span></span>



| <span data-ttu-id="24f5a-119">Atributo</span><span class="sxs-lookup"><span data-stu-id="24f5a-119">Attribute</span></span>                                                                                    | <span data-ttu-id="24f5a-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="24f5a-120">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24f5a-121">MF \_ BYTESTREAMHANDLER \_ aceita \_ gravação de compartilhamento \_</span><span class="sxs-lookup"><span data-stu-id="24f5a-121">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE</span></span>](mf-bytestreamhandler-accepts-share-write.md) | <span data-ttu-id="24f5a-122">Especifica se um manipulador de fluxo de bytes pode usar um fluxo de bytes que é aberto para gravação por outro thread</span><span class="sxs-lookup"><span data-stu-id="24f5a-122">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="24f5a-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24f5a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24f5a-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="24f5a-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[<span data-ttu-id="24f5a-125">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24f5a-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



