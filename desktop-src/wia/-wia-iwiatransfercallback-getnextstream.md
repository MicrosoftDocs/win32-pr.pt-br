---
description: Obtém um novo fluxo para o item especificado.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'Método IWiaTransferCallback:: GetNextStream (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764019"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a><span data-ttu-id="567b2-103">Método IWiaTransferCallback:: GetNextStream</span><span class="sxs-lookup"><span data-stu-id="567b2-103">IWiaTransferCallback::GetNextStream method</span></span>

<span data-ttu-id="567b2-104">Obtém um novo fluxo para o item especificado.</span><span class="sxs-lookup"><span data-stu-id="567b2-104">Gets a new stream for the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="567b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="567b2-105">Syntax</span></span>


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a><span data-ttu-id="567b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="567b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="567b2-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="567b2-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567b2-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="567b2-108">Type: **LONG**</span></span>

<span data-ttu-id="567b2-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="567b2-109">Currently unused.</span></span> <span data-ttu-id="567b2-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="567b2-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="567b2-111">*bstrItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="567b2-111">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567b2-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="567b2-112">Type: **BSTR**</span></span>

<span data-ttu-id="567b2-113">Especifica o nome do item para o qual criar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="567b2-113">Specifies the name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="567b2-114">*bstrFullItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="567b2-114">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567b2-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="567b2-115">Type: **BSTR**</span></span>

<span data-ttu-id="567b2-116">Especifica o nome completo do item para o qual criar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="567b2-116">Specifies the full name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="567b2-117">*ppDestination* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="567b2-117">*ppDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="567b2-118">Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span><span class="sxs-lookup"><span data-stu-id="567b2-118">Type: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span></span>

<span data-ttu-id="567b2-119">Recebe o endereço de um ponteiro para o novo objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="567b2-119">Receives the address of a pointer to the new [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="567b2-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="567b2-120">Return value</span></span>

<span data-ttu-id="567b2-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="567b2-121">Type: **HRESULT**</span></span>

<span data-ttu-id="567b2-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="567b2-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="567b2-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="567b2-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="567b2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="567b2-124">Remarks</span></span>

<span data-ttu-id="567b2-125">Quando esse método é implementado por um filtro de processamento de imagem, a minidriver de aquisição de imagens do Windows (WIA) 2,0 o chama durante a aquisição da imagem para obter o fluxo de destino do cliente.</span><span class="sxs-lookup"><span data-stu-id="567b2-125">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to get the destination stream from the client.</span></span>

<span data-ttu-id="567b2-126">**IWiaTransferCallback:: GetNextStream** de um filtro deve delegar ao método de retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="567b2-126">A filter's **IWiaTransferCallback::GetNextStream** must delegate to the application's callback method.</span></span> <span data-ttu-id="567b2-127">O filtro usa o fluxo retornado pela implementação **IWiaTransferCallback:: GetNextStream** do retorno de chamada do aplicativo para criar seu próprio fluxo que passa de volta para o serviço WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="567b2-127">The filter uses the stream returned by the application callback's **IWiaTransferCallback::GetNextStream** implementation to create its own stream that it passes back to the WIA 2.0 service.</span></span> <span data-ttu-id="567b2-128">A filtragem é feita quando o fluxo do filtro chama o método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .</span><span class="sxs-lookup"><span data-stu-id="567b2-128">The filtering is done when the filter's stream calls the [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method.</span></span>

<span data-ttu-id="567b2-129">O fluxo do filtro não pode fazer suposições sobre o número de bytes gravados nele em cada gravação, já que os dados da imagem não filtrada podem vir do componente de visualização do WIA 2,0 em vez do driver.</span><span class="sxs-lookup"><span data-stu-id="567b2-129">The filter's stream cannot make any assumptions on the number of bytes that are written to it on each write, since the unfiltered image data may come from the WIA 2.0 Preview Component rather than the driver.</span></span> <span data-ttu-id="567b2-130">O componente de visualização do WIA 2,0 sempre grava todos os dados de imagem não filtrados no fluxo do filtro apenas uma vez, o que significa que o fluxo do filtro tem uma fonte que está gravando.</span><span class="sxs-lookup"><span data-stu-id="567b2-130">The WIA 2.0 Preview Component always writes the whole unfiltered image data into the filter's stream only once, which means that the filter's stream has one source writing into it.</span></span> <span data-ttu-id="567b2-131">Se o driver e o componente de visualização gravarem no fluxo do filtro, o fluxo do filtro não poderá supor, por exemplo, que ele receberá o cabeçalho completo na primeira vez que [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) for chamado, embora seu driver correspondente sempre grave os dados de cabeçalho primeiro em uma gravação.</span><span class="sxs-lookup"><span data-stu-id="567b2-131">If both the driver and the preview component write into the filter's stream, the filter's stream cannot assume, for example, that it will receive the full header the first time [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) is called although its corresponding driver always writes the header data first in one write.</span></span> <span data-ttu-id="567b2-132">Nem é possível pressupor que uma gravação subsequente contém exatamente uma linha de verificação.</span><span class="sxs-lookup"><span data-stu-id="567b2-132">Nor can it assume that a subsequent write contains exactly one scan line.</span></span> <span data-ttu-id="567b2-133">Portanto, o fluxo de filtragem pode ter que contar o número de bytes gravados para determinar, por exemplo, onde os dados da imagem são iniciados.</span><span class="sxs-lookup"><span data-stu-id="567b2-133">So the filtering stream may have to count the number of bytes written to it to determine, for example, where the image data starts.</span></span>

<span data-ttu-id="567b2-134">A implementação de **IWiaTransferCallback:: GetNextStream** do filtro de processamento de imagens deve ler as propriedades necessárias para seu processamento de imagem do item para o qual a imagem está sendo adquirida.</span><span class="sxs-lookup"><span data-stu-id="567b2-134">The image processing filter's **IWiaTransferCallback::GetNextStream** implementation should read the properties needed for its image processing from the item for which the image is being acquired.</span></span> <span data-ttu-id="567b2-135">O filtro não lê as propriedades diretamente do *pWiaItem2* passado para [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="567b2-135">The filter does not read the properties directly from the *pWiaItem2* passed into [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span> <span data-ttu-id="567b2-136">Em vez disso, o filtro deve chamar [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) neste item WIA 2,0 para obter o item atual do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="567b2-136">Instead the filter must call [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) on this WIA 2.0 item to obtain the actual WIA 2.0 item.</span></span> <span data-ttu-id="567b2-137">O motivo disso é que a imagem que está sendo adquirida pode ser, na verdade, um item filho de *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="567b2-137">The reason for this is that the image being acquired may actually be a child item of *pWiaItem2*.</span></span> <span data-ttu-id="567b2-138">Por exemplo, durante uma aquisição de pasta, o filtro usa *pWiaItem2* para obter itens filho de *pWiaItem2* em **IWiaTransferCallback:: GetNextStream** (durante uma aquisição de pasta, o driver retorna as imagens representadas pelos itens filho de *pWiaItem2*).</span><span class="sxs-lookup"><span data-stu-id="567b2-138">For example, during a folder acquisition the filter uses *pWiaItem2* to obtain *pWiaItem2*'s child items in **IWiaTransferCallback::GetNextStream** (during a folder acquisition the driver returns the images represented by the child items of *pWiaItem2*).</span></span> <span data-ttu-id="567b2-139">O mesmo acontece quando o componente de visualização do WIA 2,0 chama o filtro de processamento de imagem, passando um item filho WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="567b2-139">The same is true when the WIA 2.0 Preview Component calls into the image processing filter passing a child WIA 2.0 item.</span></span>

## <a name="requirements"></a><span data-ttu-id="567b2-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="567b2-140">Requirements</span></span>



| <span data-ttu-id="567b2-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="567b2-141">Requirement</span></span> | <span data-ttu-id="567b2-142">Valor</span><span class="sxs-lookup"><span data-stu-id="567b2-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="567b2-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="567b2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="567b2-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="567b2-144">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="567b2-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="567b2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="567b2-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="567b2-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="567b2-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="567b2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="567b2-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="567b2-148"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="567b2-149">INSERI</span><span class="sxs-lookup"><span data-stu-id="567b2-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="567b2-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="567b2-150"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="567b2-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="567b2-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="567b2-152"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="567b2-152"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
