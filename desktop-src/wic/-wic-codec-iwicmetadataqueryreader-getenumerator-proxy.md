---
description: Função de proxy para o método GetEnumerator.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: Função IWICMetadataQueryReader_GetEnumerator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810268"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a><span data-ttu-id="aa180-103">\_ \_ Função de proxy GetEnumerator IWICMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="aa180-103">IWICMetadataQueryReader\_GetEnumerator\_Proxy function</span></span>

<span data-ttu-id="aa180-104">Função de proxy para o método [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) .</span><span class="sxs-lookup"><span data-stu-id="aa180-104">Proxy function for the [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa180-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa180-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a><span data-ttu-id="aa180-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa180-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="aa180-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa180-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="aa180-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="aa180-109">Ponteiro para este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="aa180-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="aa180-110">*ppIEnumString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa180-110">*ppIEnumString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa180-111">Tipo: **IEnumString \* \***</span><span class="sxs-lookup"><span data-stu-id="aa180-111">Type: **IEnumString\*\***</span></span>

<span data-ttu-id="aa180-112">Um ponteiro que recebe um ponteiro para um enumerador de metadados.</span><span class="sxs-lookup"><span data-stu-id="aa180-112">A pointer that receives a pointer to a metadata enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa180-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa180-113">Return value</span></span>

<span data-ttu-id="aa180-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aa180-114">Type: **HRESULT**</span></span>

<span data-ttu-id="aa180-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aa180-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aa180-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa180-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa180-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa180-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="aa180-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa180-118">Requirements</span></span>



| <span data-ttu-id="aa180-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa180-119">Requirement</span></span> | <span data-ttu-id="aa180-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aa180-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa180-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa180-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aa180-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa180-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="aa180-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa180-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aa180-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa180-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="aa180-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aa180-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa180-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa180-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




