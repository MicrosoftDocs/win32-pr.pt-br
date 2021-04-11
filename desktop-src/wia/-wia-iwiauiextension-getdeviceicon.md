---
description: Obtém um ícone de dispositivo personalizado.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Método IWiaUIExtension:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090500"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="2cc1b-103">Método IWiaUIExtension:: GetDeviceIcon</span><span class="sxs-lookup"><span data-stu-id="2cc1b-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="2cc1b-104">Obtém um ícone de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="2cc1b-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc1b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cc1b-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="2cc1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cc1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc1b-107">*bstrDeviceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cc1b-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc1b-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2cc1b-108">Type: **BSTR**</span></span>

<span data-ttu-id="2cc1b-109">Especifica a ID do dispositivo WIA para o qual o ícone deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="2cc1b-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="2cc1b-110">*phIcon* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2cc1b-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc1b-111">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="2cc1b-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="2cc1b-112">Aponta para um local de memória que receberá um identificador para o ícone do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cc1b-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="2cc1b-113">_nSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cc1b-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc1b-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="2cc1b-114">Type: **ULONG**</span></span>

<span data-ttu-id="2cc1b-115">Especifica o tamanho do ícone desejado, em pixels.</span><span class="sxs-lookup"><span data-stu-id="2cc1b-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="2cc1b-116">O ícone é considerado quadrado e nSize especifica a largura e a altura do ícone solicitado.</span><span class="sxs-lookup"><span data-stu-id="2cc1b-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc1b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cc1b-117">Return value</span></span>

<span data-ttu-id="2cc1b-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2cc1b-118">Type: **HRESULT**</span></span>

<span data-ttu-id="2cc1b-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2cc1b-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2cc1b-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2cc1b-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc1b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cc1b-121">Requirements</span></span>



| <span data-ttu-id="2cc1b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc1b-122">Requirement</span></span> | <span data-ttu-id="2cc1b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2cc1b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc1b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cc1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc1b-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2cc1b-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2cc1b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cc1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc1b-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2cc1b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2cc1b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2cc1b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc1b-129"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc1b-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




