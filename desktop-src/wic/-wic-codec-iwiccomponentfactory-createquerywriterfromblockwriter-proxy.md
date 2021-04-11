---
description: Função de proxy para o método CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: Função IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170875"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a><span data-ttu-id="4279a-103">\_Função de \_ proxy IWICComponentFactory CreateQueryWriterFromBlockWriter</span><span class="sxs-lookup"><span data-stu-id="4279a-103">IWICComponentFactory\_CreateQueryWriterFromBlockWriter\_Proxy function</span></span>

<span data-ttu-id="4279a-104">Função de proxy para o método [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) .</span><span class="sxs-lookup"><span data-stu-id="4279a-104">Proxy function for the [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4279a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4279a-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="4279a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4279a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4279a-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="4279a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4279a-108">Tipo: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="4279a-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="4279a-109">Ponteiro para este objeto [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="4279a-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="4279a-110">*pIBlockWriter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4279a-110">*pIBlockWriter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4279a-111">Tipo: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _</span><span class="sxs-lookup"><span data-stu-id="4279a-111">Type: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\** _</span></span>

</dd> <dt>

<span data-ttu-id="4279a-112">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4279a-112">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4279a-113">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="4279a-113">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4279a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4279a-114">Return value</span></span>

<span data-ttu-id="4279a-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4279a-115">Type: **HRESULT**</span></span>

<span data-ttu-id="4279a-116">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4279a-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4279a-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4279a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4279a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4279a-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4279a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4279a-119">Requirements</span></span>



| <span data-ttu-id="4279a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4279a-120">Requirement</span></span> | <span data-ttu-id="4279a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4279a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4279a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4279a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4279a-123">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4279a-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4279a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4279a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4279a-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4279a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4279a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4279a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4279a-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4279a-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




