---
description: Obtém o IMFDXGIDeviceManager do coletor de renderização de vídeo Microsoft Media Foundation.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'Método IMFDXGIDeviceManagerSource:: GetManager'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784969"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a><span data-ttu-id="f8c9f-103">Método IMFDXGIDeviceManagerSource:: GetManager</span><span class="sxs-lookup"><span data-stu-id="f8c9f-103">IMFDXGIDeviceManagerSource::GetManager method</span></span>

<span data-ttu-id="f8c9f-104">Obtém o [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) do coletor de renderização de vídeo Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-104">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c9f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8c9f-105">Syntax</span></span>


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="f8c9f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8c9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c9f-107">*ppManager* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f8c9f-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c9f-108">O objeto [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="f8c9f-108">The [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c9f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8c9f-109">Return value</span></span>

<span data-ttu-id="f8c9f-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8c9f-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8c9f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c9f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8c9f-112">Requirements</span></span>



| <span data-ttu-id="f8c9f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8c9f-113">Requirement</span></span> | <span data-ttu-id="f8c9f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f8c9f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c9f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8c9f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c9f-116">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f8c9f-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f8c9f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8c9f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c9f-118">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f8c9f-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="f8c9f-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="f8c9f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8c9f-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8c9f-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8c9f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8c9f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c9f-122">**IMFDXGIDeviceManagerSource**</span><span class="sxs-lookup"><span data-stu-id="f8c9f-122">**IMFDXGIDeviceManagerSource**</span></span>](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




