---
description: O método PrintXML converte dados de propriedade em uma cadeia de caracteres XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: 'IPropertySetter: método rintXML de:P (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812774"
---
# <a name="ipropertysetterprintxml-method"></a><span data-ttu-id="3ab1c-103">IPropertySetter: método rintXML de:P</span><span class="sxs-lookup"><span data-stu-id="3ab1c-103">IPropertySetter::PrintXML method</span></span>

> [!Note]  
> <span data-ttu-id="3ab1c-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-104">\[Deprecated.</span></span> <span data-ttu-id="3ab1c-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3ab1c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3ab1c-106">O `PrintXML` método converte dados de propriedade em uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-106">The `PrintXML` method converts property data into an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab1c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ab1c-107">Syntax</span></span>


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a><span data-ttu-id="3ab1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ab1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab1c-109">*pszXML* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ab1c-109">*pszXML* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ab1c-110">Ponteiro para um buffer que recebe a cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-110">Pointer to a buffer that receives the XML string.</span></span>

</dd> <dt>

<span data-ttu-id="3ab1c-111">*cbXML* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ab1c-111">*cbXML* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ab1c-112">Tamanho do buffer apontado por *pszXML*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-112">Size of the buffer pointed to by *pszXML*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3ab1c-113">*pcbPrinted* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ab1c-113">*pcbPrinted* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ab1c-114">Ponteiro para uma variável que recebe o comprimento da cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-114">Pointer to a variable that receives the length of the XML string.</span></span> <span data-ttu-id="3ab1c-115">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3ab1c-116">*recuar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ab1c-116">*indent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ab1c-117">Número de níveis de recuo para a marca externa.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-117">Number of indent levels for the outermost tag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ab1c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ab1c-118">Return value</span></span>

<span data-ttu-id="3ab1c-119">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-119">Returns S\_OK if successful.</span></span> <span data-ttu-id="3ab1c-120">Caso contrário, retorna um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-120">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span> <span data-ttu-id="3ab1c-121">Se a cadeia de caracteres XML for maior que o buffer, o método retornará E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-121">If the XML string is longer than the buffer, the method returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ab1c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ab1c-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3ab1c-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3ab1c-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ab1c-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3ab1c-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3ab1c-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ab1c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ab1c-126">Requirements</span></span>



| <span data-ttu-id="3ab1c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab1c-127">Requirement</span></span> | <span data-ttu-id="3ab1c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3ab1c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab1c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ab1c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3ab1c-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ab1c-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3ab1c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ab1c-131">Library</span></span><br/> | <dl> <span data-ttu-id="3ab1c-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ab1c-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ab1c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ab1c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab1c-134">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="3ab1c-134">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="3ab1c-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="3ab1c-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




