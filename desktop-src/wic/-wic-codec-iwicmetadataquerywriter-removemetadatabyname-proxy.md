---
description: Função de proxy para o método RemoveMetadataByName.
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: Função IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829095"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a><span data-ttu-id="3c4cd-103">\_Função de \_ proxy IWICMetadataQueryWriter RemoveMetadataByName</span><span class="sxs-lookup"><span data-stu-id="3c4cd-103">IWICMetadataQueryWriter\_RemoveMetadataByName\_Proxy function</span></span>

<span data-ttu-id="3c4cd-104">Função de proxy para o método [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="3c4cd-104">Proxy function for the [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c4cd-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a><span data-ttu-id="3c4cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c4cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c4cd-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="3c4cd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4cd-108">Tipo: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="3c4cd-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="3c4cd-109">Ponteiro para este objeto [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="3c4cd-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c4cd-110">*wzName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c4cd-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4cd-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3c4cd-112">O nome do item de metadados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3c4cd-112">The name of the metadata item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c4cd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c4cd-113">Return value</span></span>

<span data-ttu-id="3c4cd-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-114">Type: **HRESULT**</span></span>

<span data-ttu-id="3c4cd-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c4cd-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c4cd-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c4cd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c4cd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c4cd-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3c4cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c4cd-118">Requirements</span></span>



| <span data-ttu-id="3c4cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c4cd-119">Requirement</span></span> | <span data-ttu-id="3c4cd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3c4cd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4cd-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c4cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3c4cd-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c4cd-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3c4cd-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c4cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3c4cd-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c4cd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c4cd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3c4cd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c4cd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c4cd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




