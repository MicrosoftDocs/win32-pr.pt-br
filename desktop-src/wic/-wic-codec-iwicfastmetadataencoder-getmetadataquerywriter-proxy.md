---
description: Função de proxy para o método GetMetadataQueryWriter.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: Função IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772536"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="b1f82-103">\_Função de \_ proxy IWICFastMetadataEncoder GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="b1f82-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="b1f82-104">Função de proxy para o método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="b1f82-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1f82-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="b1f82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1f82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1f82-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="b1f82-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1f82-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="b1f82-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="b1f82-109">Ponteiro para este objeto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="b1f82-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="b1f82-110">*ppIMetadataQueryWriter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1f82-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1f82-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1f82-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="b1f82-112">Um ponteiro que recebe um ponteiro para o gravador de consulta de metadados do codificador.</span><span class="sxs-lookup"><span data-stu-id="b1f82-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1f82-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1f82-113">Return value</span></span>

<span data-ttu-id="b1f82-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b1f82-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b1f82-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b1f82-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1f82-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1f82-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1f82-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1f82-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b1f82-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f82-118">Requirements</span></span>



| <span data-ttu-id="b1f82-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f82-119">Requirement</span></span> | <span data-ttu-id="b1f82-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b1f82-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f82-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f82-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f82-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1f82-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b1f82-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f82-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f82-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1f82-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b1f82-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b1f82-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1f82-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1f82-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




