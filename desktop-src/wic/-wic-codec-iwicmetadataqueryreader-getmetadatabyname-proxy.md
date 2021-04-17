---
description: Função de proxy para o método GetMetadataByName.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: Função IWICMetadataQueryReader_GetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811977"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a><span data-ttu-id="8a2c9-103">\_Função de \_ proxy IWICMetadataQueryReader GetMetadataByName</span><span class="sxs-lookup"><span data-stu-id="8a2c9-103">IWICMetadataQueryReader\_GetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="8a2c9-104">Função de proxy para o método [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="8a2c9-104">Proxy function for the [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a2c9-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="8a2c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a2c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2c9-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="8a2c9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2c9-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="8a2c9-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="8a2c9-109">Ponteiro para este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="8a2c9-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="8a2c9-110">*wzName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a2c9-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2c9-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="8a2c9-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="8a2c9-112">O nome do item de metadados solicitado.</span><span class="sxs-lookup"><span data-stu-id="8a2c9-112">The name of the requested metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="8a2c9-113">*pvarValue* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8a2c9-113">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2c9-114">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="8a2c9-114">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="8a2c9-115">Ponteiro que recebe a propriedade de metadados.</span><span class="sxs-lookup"><span data-stu-id="8a2c9-115">Pointer that receives the metadata property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2c9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a2c9-116">Return value</span></span>

<span data-ttu-id="8a2c9-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8a2c9-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8a2c9-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8a2c9-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a2c9-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a2c9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a2c9-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a2c9-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8a2c9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a2c9-121">Requirements</span></span>



| <span data-ttu-id="8a2c9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a2c9-122">Requirement</span></span> | <span data-ttu-id="8a2c9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8a2c9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2c9-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a2c9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2c9-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a2c9-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8a2c9-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a2c9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2c9-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a2c9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8a2c9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8a2c9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a2c9-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a2c9-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

