---
description: O \_ método obter tamanho retorna o tamanho de saída atual e o modo de ampliação.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Método IResize:: get_Size (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759071"
---
# <a name="iresizeget_size-method"></a><span data-ttu-id="8c528-103">Método de tamanho IResize:: get \_</span><span class="sxs-lookup"><span data-stu-id="8c528-103">IResize::get\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="8c528-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8c528-104">\[Deprecated.</span></span> <span data-ttu-id="8c528-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c528-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8c528-106">O `get_Size` método retorna o tamanho de saída atual e o modo de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8c528-106">The `get_Size` method returns the current output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c528-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c528-107">Syntax</span></span>


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a><span data-ttu-id="8c528-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c528-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c528-109">*piHeight* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8c528-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c528-110">Recebe a altura do vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="8c528-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8c528-111">*piWidth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8c528-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c528-112">Recebe a largura do vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="8c528-112">Receives the video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8c528-113">*pFlag* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8c528-113">*pFlag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c528-114">Recebe um sinalizador que especifica o modo de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8c528-114">Receives a flag specifying the stretch mode.</span></span> <span data-ttu-id="8c528-115">Consulte [**redimensionar sinalizadores**](resize-flags.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8c528-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c528-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c528-116">Return value</span></span>

<span data-ttu-id="8c528-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8c528-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c528-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c528-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c528-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c528-119">Remarks</span></span>

<span data-ttu-id="8c528-120">Se o tipo de saída não tiver sido definido, o filtro deverá retornar valores padrão.</span><span class="sxs-lookup"><span data-stu-id="8c528-120">If the output type has not been set, the filter should return default values.</span></span> <span data-ttu-id="8c528-121">Esses valores podem ser escolhidos arbitrariamente em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="8c528-121">These values can be arbitrarily chosen at design time.</span></span>

> [!Note]  
> <span data-ttu-id="8c528-122">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8c528-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8c528-123">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c528-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8c528-124">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8c528-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c528-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c528-125">Requirements</span></span>



| <span data-ttu-id="8c528-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c528-126">Requirement</span></span> | <span data-ttu-id="8c528-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8c528-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c528-128">Versão</span><span class="sxs-lookup"><span data-stu-id="8c528-128">Version</span></span><br/> | <span data-ttu-id="8c528-129">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8c528-129">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="8c528-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c528-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8c528-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c528-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8c528-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c528-132">Library</span></span><br/> | <dl> <span data-ttu-id="8c528-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c528-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c528-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c528-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c528-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="8c528-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="8c528-136">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="8c528-136">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




