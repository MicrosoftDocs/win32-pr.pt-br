---
description: Especifica se um manipulador de fluxo de bytes pode usar um fluxo de bytes que é aberto para gravação por outro thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Atributo MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780073"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a><span data-ttu-id="97ceb-103">MF \_ BYTESTREAMHANDLER \_ aceita \_ o \_ atributo de gravação de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="97ceb-103">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute</span></span>

<span data-ttu-id="97ceb-104">Especifica se um manipulador de fluxo de bytes pode usar um fluxo de bytes que é aberto para gravação por outro thread.</span><span class="sxs-lookup"><span data-stu-id="97ceb-104">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread.</span></span>

## <a name="data-type"></a><span data-ttu-id="97ceb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="97ceb-105">Data type</span></span>

<span data-ttu-id="97ceb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="97ceb-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="97ceb-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="97ceb-107">Get/set</span></span>

<span data-ttu-id="97ceb-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="97ceb-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="97ceb-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="97ceb-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="97ceb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="97ceb-110">Remarks</span></span>

<span data-ttu-id="97ceb-111">Os manipuladores de fluxo de bytes podem dar suporte a esse atributo.</span><span class="sxs-lookup"><span data-stu-id="97ceb-111">Byte-stream handlers can support this attribute.</span></span> <span data-ttu-id="97ceb-112">Para obter ou definir o atributo, primeiro consulte o manipulador de fluxo de bytes para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="97ceb-112">To get or set the attribute, first query the byte-stream handler for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="97ceb-113">Em seguida, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) ou [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span><span class="sxs-lookup"><span data-stu-id="97ceb-113">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) or [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span></span>

<span data-ttu-id="97ceb-114">Se esse atributo for **true**, significa que o manipulador de fluxo de bytes pode ler de um fluxo enquanto outro thread grava no mesmo fluxo.</span><span class="sxs-lookup"><span data-stu-id="97ceb-114">If this attribute is **TRUE**, it means that the byte-stream handler can read from a stream while another thread writes to the same stream.</span></span> <span data-ttu-id="97ceb-115">Quando um fluxo é aberto para gravação por outro thread, o método [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) retorna o sinalizador de **\_ \_ gravação de compartilhamento MFBYTESTREAM** .</span><span class="sxs-lookup"><span data-stu-id="97ceb-115">When a stream is opened for writing by another thread, the [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) method returns the **MFBYTESTREAM\_SHARE\_WRITE** flag.</span></span>

<span data-ttu-id="97ceb-116">Esse atributo afeta a resolução da origem.</span><span class="sxs-lookup"><span data-stu-id="97ceb-116">This attribute affects source resolution.</span></span> <span data-ttu-id="97ceb-117">Se um fluxo de bytes tiver o sinalizador de **\_ \_ gravação de compartilhamento MFBYTESTREAM** definido, o [resolvedor de origem](source-resolver.md) não passará esse fluxo para um manipulador de fluxo de bytes, a menos que o manipulador tenha o suplemento MF \_ BYTESTREAMHANDLER aceite o \_ \_ \_ atributo de gravação de compartilhamento definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="97ceb-117">If a byte stream has the **MFBYTESTREAM\_SHARE\_WRITE** flag set, the [Source Resolver](source-resolver.md) will not pass that stream to a byte-stream handler unless the handler has the MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute set to **TRUE**.</span></span>

<span data-ttu-id="97ceb-118">O sinalizador de **\_ \_ gravação de compartilhamento MFBYTESTREAM** é uma dica que o comprimento do fluxo pode mudar enquanto o manipulador está lendo nele.</span><span class="sxs-lookup"><span data-stu-id="97ceb-118">The **MFBYTESTREAM\_SHARE\_WRITE** flag is a hint that the length of the stream might change while the handler is reading from it.</span></span>

<span data-ttu-id="97ceb-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="97ceb-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ceb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97ceb-120">Requirements</span></span>



| <span data-ttu-id="97ceb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="97ceb-121">Requirement</span></span> | <span data-ttu-id="97ceb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="97ceb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97ceb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97ceb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="97ceb-124">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="97ceb-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="97ceb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97ceb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="97ceb-126">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="97ceb-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="97ceb-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97ceb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ceb-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97ceb-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ceb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="97ceb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ceb-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97ceb-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="97ceb-131">Manipuladores de esquema e manipuladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="97ceb-131">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




