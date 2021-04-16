---
description: O \_ método Get mascaraname recupera o nome de um arquivo JPEG a ser usado como a máscara de apagamento.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Método IDxtJpeg:: get_MaskName (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759289"
---
# <a name="idxtjpegget_maskname-method"></a><span data-ttu-id="846f4-103">Método de IDxtJpeg:: obter \_ mascaraname</span><span class="sxs-lookup"><span data-stu-id="846f4-103">IDxtJpeg::get\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="846f4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="846f4-104">\[Deprecated.</span></span> <span data-ttu-id="846f4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="846f4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="846f4-106">O `get_MaskName` método recupera o nome de um arquivo JPEG a ser usado como a máscara de apagamento.</span><span class="sxs-lookup"><span data-stu-id="846f4-106">The `get_MaskName` method retrieves the name of a JPEG file to be used as the wipe mask.</span></span>

## <a name="syntax"></a><span data-ttu-id="846f4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="846f4-107">Syntax</span></span>


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="846f4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="846f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="846f4-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="846f4-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="846f4-110">Recebe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="846f4-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="846f4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="846f4-111">Return value</span></span>

<span data-ttu-id="846f4-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="846f4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="846f4-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="846f4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="846f4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="846f4-114">Remarks</span></span>

<span data-ttu-id="846f4-115">Se a transição de apagamento estiver usando um dos apagamentos internos do SMPTE aos quais ele dá suporte, o valor dessa propriedade será uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="846f4-115">If the wipe transition is using one of the built-in SMPTE wipes that it supports, the value of this property is an empty string.</span></span>

<span data-ttu-id="846f4-116">O chamador deve liberar a cadeia de caracteres retornada, usando a função **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="846f4-116">The caller must release the returned string, using the **SysFreeString** function.</span></span>

> [!Note]  
> <span data-ttu-id="846f4-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="846f4-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="846f4-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="846f4-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="846f4-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="846f4-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="846f4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="846f4-120">Requirements</span></span>



| <span data-ttu-id="846f4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="846f4-121">Requirement</span></span> | <span data-ttu-id="846f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="846f4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="846f4-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="846f4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="846f4-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="846f4-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="846f4-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="846f4-125">Library</span></span><br/> | <dl> <span data-ttu-id="846f4-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="846f4-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="846f4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="846f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="846f4-128">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="846f4-128">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="846f4-129">**IDxtJpeg:: obter \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="846f4-129">**IDxtJpeg::get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




