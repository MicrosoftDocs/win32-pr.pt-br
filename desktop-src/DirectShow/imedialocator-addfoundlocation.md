---
description: O método AddFoundLocation adiciona um diretório ao cache de diretório.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'Método IMediaLocator:: AddFoundLocation (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76d878e5b013b8c6a061d777d4ec837bca85f8e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783385"
---
# <a name="imedialocatoraddfoundlocation-method"></a><span data-ttu-id="24362-103">Método IMediaLocator:: AddFoundLocation</span><span class="sxs-lookup"><span data-stu-id="24362-103">IMediaLocator::AddFoundLocation method</span></span>

> [!Note]  
> <span data-ttu-id="24362-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="24362-104">\[Deprecated.</span></span> <span data-ttu-id="24362-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24362-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="24362-106">O `AddFoundLocation` método adiciona um diretório ao cache de diretório.</span><span class="sxs-lookup"><span data-stu-id="24362-106">The `AddFoundLocation` method adds a directory to the directory cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="24362-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24362-107">Syntax</span></span>


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a><span data-ttu-id="24362-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24362-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24362-109">*DirectoryName*</span><span class="sxs-lookup"><span data-stu-id="24362-109">*DirectoryName*</span></span> 
</dt> <dd>

<span data-ttu-id="24362-110">Caminho do diretório a ser adicionado ao cache.</span><span class="sxs-lookup"><span data-stu-id="24362-110">Directory path to add to the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24362-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24362-111">Return value</span></span>

<span data-ttu-id="24362-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="24362-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24362-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24362-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="24362-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="24362-114">Remarks</span></span>

<span data-ttu-id="24362-115">O localizador de mídia mantém um cache de caminhos de diretório onde encontrou com êxito os arquivos nas pesquisas anteriores.</span><span class="sxs-lookup"><span data-stu-id="24362-115">The media locator keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="24362-116">Quando ele localiza um arquivo com êxito, ele adiciona o diretório ao cache.</span><span class="sxs-lookup"><span data-stu-id="24362-116">When it successfully locates a file, it adds the directory to the cache.</span></span>

> [!Note]  
> <span data-ttu-id="24362-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="24362-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="24362-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="24362-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="24362-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="24362-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24362-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24362-120">Requirements</span></span>



| <span data-ttu-id="24362-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="24362-121">Requirement</span></span> | <span data-ttu-id="24362-122">Valor</span><span class="sxs-lookup"><span data-stu-id="24362-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24362-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24362-123">Header</span></span><br/>  | <dl> <span data-ttu-id="24362-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="24362-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="24362-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24362-125">Library</span></span><br/> | <dl> <span data-ttu-id="24362-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24362-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24362-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="24362-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24362-128">**Interface IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="24362-128">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="24362-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="24362-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




