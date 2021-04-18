---
description: Fornece o progresso e outras notificações durante uma transferência.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'Método IWiaTransferCallback:: TransferCallback (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783750"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a><span data-ttu-id="dbfcd-103">Método IWiaTransferCallback:: TransferCallback</span><span class="sxs-lookup"><span data-stu-id="dbfcd-103">IWiaTransferCallback::TransferCallback method</span></span>

<span data-ttu-id="dbfcd-104">Fornece o progresso e outras notificações durante uma transferência.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-104">Provides progress and other notifications during a transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfcd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbfcd-105">Syntax</span></span>


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a><span data-ttu-id="dbfcd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbfcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbfcd-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbfcd-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfcd-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="dbfcd-108">Type: **LONG**</span></span>

<span data-ttu-id="dbfcd-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-109">Currently unused.</span></span> <span data-ttu-id="dbfcd-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dbfcd-111">*pWiaTransferParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbfcd-111">*pWiaTransferParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfcd-112">Tipo: \**[**WiaTransferParams**](-wia-wiatransferparams.md) \** _</span><span class="sxs-lookup"><span data-stu-id="dbfcd-112">Type: \**[**WiaTransferParams**](-wia-wiatransferparams.md)\** _</span></span>

<span data-ttu-id="dbfcd-113">Especifica um ponteiro para uma estrutura [_ *WiaTransferParams* \*](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="dbfcd-113">Specifies a pointer to a [_ *WiaTransferParams*\*](-wia-wiatransferparams.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbfcd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbfcd-114">Return value</span></span>

<span data-ttu-id="dbfcd-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dbfcd-115">Type: **HRESULT**</span></span>

<span data-ttu-id="dbfcd-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbfcd-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbfcd-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbfcd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbfcd-118">Remarks</span></span>

<span data-ttu-id="dbfcd-119">Quando esse método é implementado por um filtro de processamento de imagem, a minidriver de aquisição de imagens do Windows (WIA) 2,0 o chama durante a aquisição da imagem para enviar mensagens de progresso de volta ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-119">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to send progress messages back to the application.</span></span>

<span data-ttu-id="dbfcd-120">**IWiaTransferCallback:: TransferCallback** de um filtro deve delegar ao método **IWiaTransferCallback:: TransferCallback** do retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-120">A filter's **IWiaTransferCallback::TransferCallback** must delegate to the application callback's **IWiaTransferCallback::TransferCallback** method.</span></span> <span data-ttu-id="dbfcd-121">Normalmente, o fluxo de filtro filtra os dados passados para ele e grava os dados filtrados diretamente no fluxo fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-121">Usually, the filter stream filters the data passed to it and writes the filtered data directly to the application provided stream.</span></span> <span data-ttu-id="dbfcd-122">Quando o filtro de processamento de imagens armazena dados entre chamadas para seu método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , ele também deve modificar os valores *lPercentComplete* e *ulBytesWrittenToCurrentStream* na estrutura [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="dbfcd-122">When image processing filter stores data between calls to its [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method, it must also modify the *lPercentComplete* and *ulBytesWrittenToCurrentStream* values in the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfcd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbfcd-123">Requirements</span></span>



| <span data-ttu-id="dbfcd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfcd-124">Requirement</span></span> | <span data-ttu-id="dbfcd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dbfcd-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfcd-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbfcd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfcd-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbfcd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dbfcd-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbfcd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfcd-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbfcd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dbfcd-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbfcd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbfcd-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbfcd-131"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="dbfcd-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="dbfcd-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dbfcd-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dbfcd-133"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="dbfcd-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbfcd-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbfcd-135"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbfcd-135"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
