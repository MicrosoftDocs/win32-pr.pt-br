---
description: O método SetUserName define um nome definido pelo aplicativo para o objeto.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'Método IAMTimelineObj:: SetUserName (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779235"
---
# <a name="iamtimelineobjsetusername-method"></a><span data-ttu-id="57a44-103">Método IAMTimelineObj:: SetUserName</span><span class="sxs-lookup"><span data-stu-id="57a44-103">IAMTimelineObj::SetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="57a44-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="57a44-104">\[Deprecated.</span></span> <span data-ttu-id="57a44-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57a44-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="57a44-106">O `SetUserName` método define um nome definido pelo aplicativo para o objeto.</span><span class="sxs-lookup"><span data-stu-id="57a44-106">The `SetUserName` method sets an application-defined name for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a44-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57a44-107">Syntax</span></span>


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="57a44-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57a44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a44-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="57a44-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="57a44-110">Cadeia de caracteres largos que contém o nome.</span><span class="sxs-lookup"><span data-stu-id="57a44-110">Wide-character string that contains the name.</span></span> <span data-ttu-id="57a44-111">Cadeias com mais de 256 caracteres podem estar truncadas.</span><span class="sxs-lookup"><span data-stu-id="57a44-111">Strings longer than 256 characters might be truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a44-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57a44-112">Return value</span></span>

<span data-ttu-id="57a44-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="57a44-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57a44-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57a44-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a44-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="57a44-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="57a44-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="57a44-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="57a44-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="57a44-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="57a44-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="57a44-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57a44-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a44-119">Requirements</span></span>



| <span data-ttu-id="57a44-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a44-120">Requirement</span></span> | <span data-ttu-id="57a44-121">Valor</span><span class="sxs-lookup"><span data-stu-id="57a44-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57a44-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57a44-122">Header</span></span><br/>  | <dl> <span data-ttu-id="57a44-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57a44-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="57a44-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57a44-124">Library</span></span><br/> | <dl> <span data-ttu-id="57a44-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57a44-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a44-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="57a44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a44-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="57a44-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="57a44-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="57a44-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




