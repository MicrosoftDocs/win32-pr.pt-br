---
description: O método SaveToBlob salva os dados de propriedade em um formato de persistência.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Método IPropertySetter:: SaveToBlob (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786967"
---
# <a name="ipropertysettersavetoblob-method"></a><span data-ttu-id="3c733-103">Método IPropertySetter:: SaveToBlob</span><span class="sxs-lookup"><span data-stu-id="3c733-103">IPropertySetter::SaveToBlob method</span></span>

> [!Note]  
> <span data-ttu-id="3c733-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="3c733-104">\[Deprecated.</span></span> <span data-ttu-id="3c733-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c733-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3c733-106">O `SaveToBlob` método salva os dados de propriedade em um formato de persistência.</span><span class="sxs-lookup"><span data-stu-id="3c733-106">The `SaveToBlob` method saves the property data to a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c733-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c733-107">Syntax</span></span>


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a><span data-ttu-id="3c733-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c733-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c733-109">*pcSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3c733-109">*pcSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c733-110">Recebe o tamanho dos dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3c733-110">Receives the size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3c733-111">*ppb* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3c733-111">*ppb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c733-112">Recebe um ponteiro para uma matriz de bytes que recebe os dados.</span><span class="sxs-lookup"><span data-stu-id="3c733-112">Receives a pointer to an array of bytes that receives the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c733-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c733-113">Return value</span></span>

<span data-ttu-id="3c733-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c733-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c733-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c733-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c733-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c733-116">Remarks</span></span>

<span data-ttu-id="3c733-117">O método aloca memória para a matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="3c733-117">The method allocates memory for the byte array.</span></span> <span data-ttu-id="3c733-118">O chamador deve liberá-lo, usando a função **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="3c733-118">The caller must free it, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="3c733-119">Todos os nomes de propriedade e valores são truncados para 40 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="3c733-119">All property names and values are truncated to 40 characters in length.</span></span> <span data-ttu-id="3c733-120">Por esse motivo, XML é o formato de persistência preferencial.</span><span class="sxs-lookup"><span data-stu-id="3c733-120">For this reason, XML is the preferred persistence format.</span></span> <span data-ttu-id="3c733-121">Consulte a [**interface IXml2Dex**](ixml2dex.md).</span><span class="sxs-lookup"><span data-stu-id="3c733-121">See [**IXml2Dex Interface**](ixml2dex.md).</span></span>

> [!Note]  
> <span data-ttu-id="3c733-122">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="3c733-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3c733-123">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3c733-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3c733-124">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3c733-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c733-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c733-125">Requirements</span></span>



| <span data-ttu-id="3c733-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c733-126">Requirement</span></span> | <span data-ttu-id="3c733-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3c733-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c733-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c733-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3c733-129"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c733-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3c733-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c733-130">Library</span></span><br/> | <dl> <span data-ttu-id="3c733-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c733-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c733-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c733-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c733-133">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="3c733-133">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="3c733-134">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="3c733-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




