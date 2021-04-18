---
description: O método SetResizerGUID especifica o CLSID de um filtro de redimensionamento de vídeo personalizado.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'Método IRenderEngine2:: SetResizerGUID (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758464"
---
# <a name="irenderengine2setresizerguid-method"></a><span data-ttu-id="200fc-103">Método IRenderEngine2:: SetResizerGUID</span><span class="sxs-lookup"><span data-stu-id="200fc-103">IRenderEngine2::SetResizerGUID method</span></span>

> [!Note]  
> <span data-ttu-id="200fc-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="200fc-104">\[Deprecated.</span></span> <span data-ttu-id="200fc-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="200fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="200fc-106">O `SetResizerGUID` método especifica o CLSID de um filtro de redimensionamento de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="200fc-106">The `SetResizerGUID` method specifies the CLSID of a custom video resizing filter.</span></span> <span data-ttu-id="200fc-107">Chame esse método para substituir o filtro de redimensionamento padrão usado pelos serviços de edição do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="200fc-107">Call this method to replace the default resizing filter used by DirectShow Editing Services.</span></span> <span data-ttu-id="200fc-108">O filtro deve ser registrado como um objeto COM no sistema do usuário e deve dar suporte à interface [**IResize**](iresize.md) .</span><span class="sxs-lookup"><span data-stu-id="200fc-108">Your filter must be registered as a COM object on the user's system, and it must support the [**IResize**](iresize.md) interface.</span></span>

<span data-ttu-id="200fc-109">Chame esse método antes de chamar [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="200fc-109">Call this method before calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="200fc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="200fc-110">Syntax</span></span>


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a><span data-ttu-id="200fc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="200fc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200fc-112">*ResizerGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="200fc-112">*ResizerGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="200fc-113">O CLSID do filtro.</span><span class="sxs-lookup"><span data-stu-id="200fc-113">The CLSID of the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200fc-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="200fc-114">Return value</span></span>

<span data-ttu-id="200fc-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="200fc-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="200fc-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="200fc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="200fc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="200fc-117">Remarks</span></span>

<span data-ttu-id="200fc-118">Para reverter para o redimensionador DES padrão, use o seguinte CLSID:</span><span class="sxs-lookup"><span data-stu-id="200fc-118">To revert to the default DES resizer, use the following CLSID:</span></span>


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> <span data-ttu-id="200fc-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="200fc-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="200fc-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="200fc-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="200fc-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="200fc-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="200fc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="200fc-122">Requirements</span></span>



| <span data-ttu-id="200fc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="200fc-123">Requirement</span></span> | <span data-ttu-id="200fc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="200fc-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="200fc-125">Versão</span><span class="sxs-lookup"><span data-stu-id="200fc-125">Version</span></span><br/> | <span data-ttu-id="200fc-126">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="200fc-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="200fc-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="200fc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="200fc-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="200fc-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="200fc-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="200fc-129">Library</span></span><br/> | <dl> <span data-ttu-id="200fc-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="200fc-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200fc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="200fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200fc-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="200fc-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="200fc-133">**Interface IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="200fc-133">**IRenderEngine2 Interface**</span></span>](irenderengine2.md)
</dt> </dl>

 

 




