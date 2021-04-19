---
description: O método LoadDefSettings restaura as configurações padrão da transição de apagamento.
ms.assetid: 3f81002a-ecac-4d5a-8d2a-ada4d4884d7d
title: 'Método IDxtJpeg:: LoadDefSettings (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.LoadDefSettings
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51438a21782d1a703a3b43134517e8337ce9f75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757287"
---
# <a name="idxtjpegloaddefsettings-method"></a><span data-ttu-id="bf27f-103">Método IDxtJpeg:: LoadDefSettings</span><span class="sxs-lookup"><span data-stu-id="bf27f-103">IDxtJpeg::LoadDefSettings method</span></span>

> [!Note]  
> <span data-ttu-id="bf27f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="bf27f-104">\[Deprecated.</span></span> <span data-ttu-id="bf27f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bf27f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bf27f-106">O `LoadDefSettings` método restaura as configurações padrão da transição de apagamento.</span><span class="sxs-lookup"><span data-stu-id="bf27f-106">The `LoadDefSettings` method restores the default settings of the Wipe transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf27f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf27f-107">Syntax</span></span>


```C++
HRESULT LoadDefSettings();
```



## <a name="parameters"></a><span data-ttu-id="bf27f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf27f-108">Parameters</span></span>

<span data-ttu-id="bf27f-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bf27f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf27f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf27f-110">Return value</span></span>

<span data-ttu-id="bf27f-111">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bf27f-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf27f-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf27f-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf27f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf27f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf27f-114">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="bf27f-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bf27f-115">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bf27f-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bf27f-116">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bf27f-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf27f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf27f-117">Requirements</span></span>



| <span data-ttu-id="bf27f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf27f-118">Requirement</span></span> | <span data-ttu-id="bf27f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bf27f-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf27f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf27f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bf27f-121"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf27f-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bf27f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf27f-122">Library</span></span><br/> | <dl> <span data-ttu-id="bf27f-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf27f-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf27f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf27f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf27f-125">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="bf27f-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




