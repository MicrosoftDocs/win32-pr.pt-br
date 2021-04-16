---
description: O método getvendoridstring recupera o nome do fornecedor. Para os objetos do mecanismo de renderização que são fornecidos pelo DirectShow, a cadeia de caracteres do fornecedor é &\# 0034; Microsoft Corporation&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'Método IRenderEngine:: getvendor (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760738"
---
# <a name="irenderenginegetvendorstring-method"></a><span data-ttu-id="9b576-104">Método IRenderEngine:: getvendor</span><span class="sxs-lookup"><span data-stu-id="9b576-104">IRenderEngine::GetVendorString method</span></span>

> [!Note]  
> <span data-ttu-id="9b576-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9b576-105">\[Deprecated.</span></span> <span data-ttu-id="9b576-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9b576-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9b576-107">O `GetVendorString` método recupera o nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9b576-107">The `GetVendorString` method retrieves the name of the vendor.</span></span> <span data-ttu-id="9b576-108">Para os objetos do mecanismo de renderização que são fornecidos pelo DirectShow, a cadeia de caracteres do fornecedor é "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="9b576-108">For the render engine objects that are provided by DirectShow, the vendor string is "Microsoft Corporation".</span></span>

## <a name="syntax"></a><span data-ttu-id="9b576-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b576-109">Syntax</span></span>


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a><span data-ttu-id="9b576-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b576-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b576-111">*pVendorID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9b576-111">*pVendorID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9b576-112">Recebe um **BSTR** contendo a cadeia de caracteres do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9b576-112">Receives a **BSTR** containing the vendor string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b576-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b576-113">Return value</span></span>

<span data-ttu-id="9b576-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9b576-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b576-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b576-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b576-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b576-116">Remarks</span></span>

<span data-ttu-id="9b576-117">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9b576-117">The method allocates memory for the string.</span></span> <span data-ttu-id="9b576-118">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="9b576-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="9b576-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="9b576-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9b576-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b576-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9b576-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9b576-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b576-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b576-122">Requirements</span></span>



| <span data-ttu-id="9b576-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b576-123">Requirement</span></span> | <span data-ttu-id="9b576-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9b576-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b576-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b576-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9b576-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b576-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9b576-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b576-127">Library</span></span><br/> | <dl> <span data-ttu-id="9b576-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b576-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b576-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b576-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b576-130">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="9b576-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="9b576-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="9b576-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




