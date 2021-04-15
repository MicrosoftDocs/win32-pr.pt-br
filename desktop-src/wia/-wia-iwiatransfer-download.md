---
description: Inicia um download de dados para o chamador.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: 'IWiaTransfer: método aixar de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501790"
---
# <a name="iwiatransferdownload-method"></a><span data-ttu-id="69d00-103">IWiaTransfer: método aixar de:D</span><span class="sxs-lookup"><span data-stu-id="69d00-103">IWiaTransfer::Download method</span></span>

<span data-ttu-id="69d00-104">Inicia um download de dados para o chamador.</span><span class="sxs-lookup"><span data-stu-id="69d00-104">Initiates a data download to the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d00-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69d00-105">Syntax</span></span>


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="69d00-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69d00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d00-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69d00-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d00-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="69d00-108">Type: **LONG**</span></span>

<span data-ttu-id="69d00-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="69d00-109">Currently unused.</span></span> <span data-ttu-id="69d00-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="69d00-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="69d00-111">*pIWiaTransferCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69d00-111">*pIWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d00-112">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="69d00-112">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="69d00-113">Especifica um ponteiro para a interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) do chamador.</span><span class="sxs-lookup"><span data-stu-id="69d00-113">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d00-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69d00-114">Return value</span></span>

<span data-ttu-id="69d00-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="69d00-115">Type: **HRESULT**</span></span>

<span data-ttu-id="69d00-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="69d00-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69d00-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69d00-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69d00-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d00-118">Remarks</span></span>

<span data-ttu-id="69d00-119">Se uma pasta for baixada, todos os itens filho dessa pasta também serão transferidos.</span><span class="sxs-lookup"><span data-stu-id="69d00-119">If a folder is downloaded, then all the child items of that folder are also transferred.</span></span> <span data-ttu-id="69d00-120">Cada item é transferido em um fluxo separado.</span><span class="sxs-lookup"><span data-stu-id="69d00-120">Each item is transferred in a separate stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d00-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d00-121">Requirements</span></span>



| <span data-ttu-id="69d00-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d00-122">Requirement</span></span> | <span data-ttu-id="69d00-123">Valor</span><span class="sxs-lookup"><span data-stu-id="69d00-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69d00-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d00-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69d00-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69d00-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="69d00-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d00-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69d00-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69d00-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69d00-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69d00-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d00-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d00-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="69d00-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="69d00-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69d00-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="69d00-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="69d00-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69d00-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="69d00-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69d00-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




