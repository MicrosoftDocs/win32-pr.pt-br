---
description: Inicia um carregamento de dados de um único item do chamador.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Método IWiaTransfer:: upload (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164529"
---
# <a name="iwiatransferupload-method"></a><span data-ttu-id="352c8-103">Método IWiaTransfer:: upload</span><span class="sxs-lookup"><span data-stu-id="352c8-103">IWiaTransfer::Upload method</span></span>

<span data-ttu-id="352c8-104">Inicia um carregamento de dados de um único item do chamador.</span><span class="sxs-lookup"><span data-stu-id="352c8-104">Initiates a data upload of a single item from the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="352c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="352c8-105">Syntax</span></span>


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="352c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="352c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352c8-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="352c8-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352c8-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="352c8-108">Type: **LONG**</span></span>

<span data-ttu-id="352c8-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="352c8-109">Currently unused.</span></span> <span data-ttu-id="352c8-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="352c8-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="352c8-111">*pSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="352c8-111">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352c8-112">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="352c8-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="352c8-113">Especifica um ponteiro para os dados de [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="352c8-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) data.</span></span>

</dd> <dt>

<span data-ttu-id="352c8-114">_pIWiaTransferCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="352c8-114">_pIWiaTransferCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352c8-115">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="352c8-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="352c8-116">Especifica um ponteiro para a interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) do chamador.</span><span class="sxs-lookup"><span data-stu-id="352c8-116">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352c8-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="352c8-117">Return value</span></span>

<span data-ttu-id="352c8-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="352c8-118">Type: **HRESULT**</span></span>

<span data-ttu-id="352c8-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="352c8-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="352c8-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="352c8-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="352c8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="352c8-121">Requirements</span></span>



| <span data-ttu-id="352c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="352c8-122">Requirement</span></span> | <span data-ttu-id="352c8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="352c8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="352c8-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="352c8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="352c8-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="352c8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="352c8-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="352c8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="352c8-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="352c8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="352c8-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="352c8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="352c8-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="352c8-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="352c8-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="352c8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="352c8-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="352c8-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="352c8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="352c8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="352c8-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="352c8-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
