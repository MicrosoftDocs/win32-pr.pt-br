---
description: Define um novo retorno de chamada de aplicativo para o filtro de processamento de imagem a ser usado para chamadas de encaminhamento.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Método IWiaImageFilter:: SetNewCallback (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647482"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a><span data-ttu-id="3ce50-103">Método IWiaImageFilter:: SetNewCallback</span><span class="sxs-lookup"><span data-stu-id="3ce50-103">IWiaImageFilter::SetNewCallback method</span></span>

<span data-ttu-id="3ce50-104">Define um novo retorno de chamada de aplicativo para o filtro de processamento de imagem a ser usado para chamadas de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="3ce50-104">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce50-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ce50-105">Syntax</span></span>


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="3ce50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ce50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce50-107">*pWiaTransferCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ce50-107">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-108">Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span><span class="sxs-lookup"><span data-stu-id="3ce50-108">Type: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span></span>

<span data-ttu-id="3ce50-109">Especifica um ponteiro para a interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3ce50-109">Specifies a pointer to the application's [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce50-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ce50-110">Return value</span></span>

<span data-ttu-id="3ce50-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3ce50-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3ce50-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3ce50-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ce50-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ce50-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce50-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ce50-114">Remarks</span></span>

<span data-ttu-id="3ce50-115">Não chame esse método diretamente do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3ce50-115">Do not call this method directly from your application.</span></span>

<span data-ttu-id="3ce50-116">O filtro de processamento de imagem é necessário para liberar a interface de retorno de chamada de aplicativo armazenada anteriormente antes de definir o novo retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="3ce50-116">The image processing filter is required to release the previously stored application callback interface before setting the new callback.</span></span>

<span data-ttu-id="3ce50-117">Se *pWiaTransferCallback* for **NULL**, o filtro de processamento de imagem deverá simplesmente liberar o retorno de chamada do aplicativo antigo e retornar os S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ce50-117">If *pWiaTransferCallback* is **NULL**, the image processing filter should simply release the old application callback and return S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce50-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ce50-118">Requirements</span></span>



| <span data-ttu-id="3ce50-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce50-119">Requirement</span></span> | <span data-ttu-id="3ce50-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3ce50-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce50-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce50-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce50-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ce50-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ce50-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce50-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce50-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ce50-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ce50-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ce50-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce50-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce50-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ce50-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="3ce50-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ce50-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ce50-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




