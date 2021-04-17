---
description: O \_ método Put filename Especifica o nome do arquivo de origem para o detector de mídia a ser usado.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: 'IMediaDet: método de ut_Filename de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789896"
---
# <a name="imediadetput_filename-method"></a><span data-ttu-id="ee4f7-103">IMediaDet: método de nome de arquivo de:p UT \_</span><span class="sxs-lookup"><span data-stu-id="ee4f7-103">IMediaDet::put\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="ee4f7-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-104">\[Deprecated.</span></span> <span data-ttu-id="ee4f7-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ee4f7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ee4f7-106">O `put_Filename` método especifica o nome do arquivo de origem para o detector de mídia a ser usado.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-106">The `put_Filename` method specifies the name of the source file for the media detector to use.</span></span>

<span data-ttu-id="ee4f7-107">Não chame esse método duas vezes no mesmo objeto MediaDet.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-107">Do not call this method twice on the same MediaDet object.</span></span> <span data-ttu-id="ee4f7-108">Para usar essa interface com mais de um arquivo de origem, crie instâncias separadas do objeto MediaDet.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-108">To use this interface with more than one source file, create separate instances of the MediaDet object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4f7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee4f7-109">Syntax</span></span>


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="ee4f7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee4f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee4f7-111">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee4f7-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4f7-112">Nome do arquivo da origem.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-112">File name of the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee4f7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee4f7-113">Return value</span></span>

<span data-ttu-id="ee4f7-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee4f7-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee4f7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee4f7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee4f7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ee4f7-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ee4f7-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ee4f7-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ee4f7-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ee4f7-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee4f7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4f7-120">Requirements</span></span>



| <span data-ttu-id="ee4f7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4f7-121">Requirement</span></span> | <span data-ttu-id="ee4f7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ee4f7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee4f7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ee4f7-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4f7-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ee4f7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee4f7-125">Library</span></span><br/> | <dl> <span data-ttu-id="ee4f7-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee4f7-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4f7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee4f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4f7-128">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="ee4f7-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="ee4f7-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ee4f7-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




