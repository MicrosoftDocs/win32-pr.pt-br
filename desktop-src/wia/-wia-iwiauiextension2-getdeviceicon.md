---
description: 'Método IWiaUIExtension2:: GetDeviceIcon – Obtém um ícone de dispositivo personalizado.'
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'Método IWiaUIExtension2:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116614"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="ffded-103">Método IWiaUIExtension2:: GetDeviceIcon</span><span class="sxs-lookup"><span data-stu-id="ffded-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="ffded-104">Obtém um ícone de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="ffded-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffded-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffded-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="ffded-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffded-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffded-107">*bstrDeviceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ffded-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffded-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ffded-108">Type: **BSTR**</span></span>

<span data-ttu-id="ffded-109">Especifica a ID do dispositivo WIA para o qual o ícone deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="ffded-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="ffded-110">*phIcon* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ffded-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffded-111">Tipo: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="ffded-111">Type: **HICON\***</span></span>

<span data-ttu-id="ffded-112">Aponta para um local de memória que receberá um identificador para o ícone do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ffded-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="ffded-113">*nSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ffded-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffded-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="ffded-114">Type: **ULONG**</span></span>

<span data-ttu-id="ffded-115">Especifica o tamanho do ícone desejado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="ffded-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="ffded-116">O ícone é considerado quadrado e nSize especifica a largura e a altura do ícone solicitado.</span><span class="sxs-lookup"><span data-stu-id="ffded-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffded-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ffded-117">Return value</span></span>

<span data-ttu-id="ffded-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ffded-118">Type: **HRESULT**</span></span>

<span data-ttu-id="ffded-119">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ffded-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ffded-120">Se o método falhar, ele retornará um código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="ffded-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="ffded-121">A tabela a seguir mostra alguns dos possíveis códigos de status de retorno.</span><span class="sxs-lookup"><span data-stu-id="ffded-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="ffded-122">Código do erro</span><span class="sxs-lookup"><span data-stu-id="ffded-122">Error code</span></span>    | <span data-ttu-id="ffded-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ffded-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffded-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ffded-124">E\_INVALIDARG</span></span> | <span data-ttu-id="ffded-125">O parâmetro bstrDeviceId ou phIcon é **nulo** ou bstrDeviceId não aponta para uma cadeia de caracteres de ID de dispositivo WIA válida</span><span class="sxs-lookup"><span data-stu-id="ffded-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="ffded-126">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="ffded-126">E\_FAIL</span></span>       | <span data-ttu-id="ffded-127">Nenhum recurso de ícone está disponível.</span><span class="sxs-lookup"><span data-stu-id="ffded-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="ffded-128">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="ffded-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="ffded-129">Nenhum ícone do tamanho solicitado está disponível.</span><span class="sxs-lookup"><span data-stu-id="ffded-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="ffded-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffded-130">Requirements</span></span>



| <span data-ttu-id="ffded-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffded-131">Requirement</span></span> | <span data-ttu-id="ffded-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ffded-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ffded-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffded-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ffded-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ffded-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ffded-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffded-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ffded-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ffded-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ffded-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ffded-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffded-138"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffded-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




