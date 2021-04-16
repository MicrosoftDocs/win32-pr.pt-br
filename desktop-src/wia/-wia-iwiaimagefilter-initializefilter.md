---
description: Inicializa o filtro. Chamado pelo WIA (Windows Image Acquisition) 2,0 antes de cada download de imagem.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Método IWiaImageFilter:: InitializeFilter (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808332"
---
# <a name="iwiaimagefilterinitializefilter-method"></a><span data-ttu-id="0b276-104">Método IWiaImageFilter:: InitializeFilter</span><span class="sxs-lookup"><span data-stu-id="0b276-104">IWiaImageFilter::InitializeFilter method</span></span>

<span data-ttu-id="0b276-105">Inicializa o filtro.</span><span class="sxs-lookup"><span data-stu-id="0b276-105">Initializes the filter.</span></span> <span data-ttu-id="0b276-106">Chamado pelo WIA (Windows Image Acquisition) 2,0 antes de cada download de imagem.</span><span class="sxs-lookup"><span data-stu-id="0b276-106">Called by Windows Image Acquisition (WIA) 2.0 before each image download.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b276-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b276-107">Syntax</span></span>


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="0b276-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b276-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b276-109">*pWiaItem2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b276-109">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b276-110">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="0b276-110">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="0b276-111">Especifica um ponteiro para o item [_ *IWiaItem2* \*](-wia-iwiaitem2.md) que representa a imagem de visualização.</span><span class="sxs-lookup"><span data-stu-id="0b276-111">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item that represents the preview image.</span></span>

</dd> <dt>

<span data-ttu-id="0b276-112">*pWiaTransferCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b276-112">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b276-113">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="0b276-113">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="0b276-114">Especifica um ponteiro para a interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b276-114">Specifies a pointer to the application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b276-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b276-115">Return value</span></span>

<span data-ttu-id="0b276-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0b276-116">Type: **HRESULT**</span></span>

<span data-ttu-id="0b276-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0b276-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b276-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0b276-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b276-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b276-119">Remarks</span></span>

<span data-ttu-id="0b276-120">Esse método é chamado quando um aplicativo chama [**Download**](-wia-iwiatransfer-download.md) e quando um aplicativo chama a função do componente de visualização do WIA 2,0 `GetNewPreview` .</span><span class="sxs-lookup"><span data-stu-id="0b276-120">This method is called when an application calls [**Download**](-wia-iwiatransfer-download.md) and when an application calls the WIA 2.0 Preview Component's `GetNewPreview` function.</span></span> <span data-ttu-id="0b276-121">**IWiaImageFilter:: InitializeFilter** armazena as referências a *pWiaItem2* e *pWiaTransferCallback* para passar nessas funções.</span><span class="sxs-lookup"><span data-stu-id="0b276-121">**IWiaImageFilter::InitializeFilter** stores the references to *pWiaItem2* and *pWiaTransferCallback* to pass into these functions.</span></span> <span data-ttu-id="0b276-122">Esses dois ponteiros de interface devem ser armazenados como variáveis de membro e [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) deve ser chamado para cada um.</span><span class="sxs-lookup"><span data-stu-id="0b276-122">These two interface pointers should be stored as member variables and [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) should be called for each.</span></span> <span data-ttu-id="0b276-123">Os ponteiros de interface também são necessários na implementação do filtro de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) e [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante a aquisição da imagem.</span><span class="sxs-lookup"><span data-stu-id="0b276-123">The interface pointers are also needed in the filter's implementation of [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) and [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) during image acquisition.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b276-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b276-124">Requirements</span></span>



| <span data-ttu-id="0b276-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b276-125">Requirement</span></span> | <span data-ttu-id="0b276-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0b276-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b276-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b276-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b276-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b276-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0b276-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b276-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b276-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b276-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0b276-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b276-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b276-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b276-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b276-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="0b276-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b276-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b276-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 
