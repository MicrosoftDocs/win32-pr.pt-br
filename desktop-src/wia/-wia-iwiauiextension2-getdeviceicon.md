---
description: Obtém um ícone de dispositivo personalizado.
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
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501786"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="01d96-103">Método IWiaUIExtension2:: GetDeviceIcon</span><span class="sxs-lookup"><span data-stu-id="01d96-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="01d96-104">Obtém um ícone de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="01d96-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d96-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01d96-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="01d96-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01d96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d96-107">*bstrDeviceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01d96-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d96-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="01d96-108">Type: **BSTR**</span></span>

<span data-ttu-id="01d96-109">Especifica a ID do dispositivo WIA para o qual o ícone deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="01d96-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="01d96-110">*phIcon* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01d96-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01d96-111">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="01d96-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="01d96-112">Aponta para um local de memória que receberá um identificador para o ícone do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d96-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="01d96-113">_nSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01d96-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d96-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="01d96-114">Type: **ULONG**</span></span>

<span data-ttu-id="01d96-115">Especifica o tamanho do ícone desejado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="01d96-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="01d96-116">O ícone é considerado quadrado e nSize especifica a largura e a altura do ícone solicitado.</span><span class="sxs-lookup"><span data-stu-id="01d96-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d96-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01d96-117">Return value</span></span>

<span data-ttu-id="01d96-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="01d96-118">Type: **HRESULT**</span></span>

<span data-ttu-id="01d96-119">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01d96-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="01d96-120">Se o método falhar, ele retornará um código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="01d96-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="01d96-121">A tabela a seguir mostra alguns dos possíveis códigos de status de retorno.</span><span class="sxs-lookup"><span data-stu-id="01d96-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="01d96-122">Código do erro</span><span class="sxs-lookup"><span data-stu-id="01d96-122">Error code</span></span>    | <span data-ttu-id="01d96-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="01d96-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d96-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="01d96-124">E\_INVALIDARG</span></span> | <span data-ttu-id="01d96-125">O parâmetro bstrDeviceId ou phIcon é **nulo** ou bstrDeviceId não aponta para uma cadeia de caracteres de ID de dispositivo WIA válida</span><span class="sxs-lookup"><span data-stu-id="01d96-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="01d96-126">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="01d96-126">E\_FAIL</span></span>       | <span data-ttu-id="01d96-127">Nenhum recurso de ícone está disponível.</span><span class="sxs-lookup"><span data-stu-id="01d96-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="01d96-128">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="01d96-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="01d96-129">Nenhum ícone do tamanho solicitado está disponível.</span><span class="sxs-lookup"><span data-stu-id="01d96-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="01d96-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01d96-130">Requirements</span></span>



| <span data-ttu-id="01d96-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="01d96-131">Requirement</span></span> | <span data-ttu-id="01d96-132">Valor</span><span class="sxs-lookup"><span data-stu-id="01d96-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="01d96-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01d96-133">Minimum supported client</span></span><br/> | <span data-ttu-id="01d96-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01d96-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="01d96-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01d96-135">Minimum supported server</span></span><br/> | <span data-ttu-id="01d96-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01d96-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="01d96-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01d96-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="01d96-138"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="01d96-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




