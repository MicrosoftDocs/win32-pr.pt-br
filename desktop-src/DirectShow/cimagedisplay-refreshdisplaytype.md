---
description: O método RefreshDisplayType atualiza o formato de vídeo do objeto para corresponder à exibição especificada.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Método CImageDisplay. RefreshDisplayType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759319"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a><span data-ttu-id="44df5-103">Método CImageDisplay. RefreshDisplayType</span><span class="sxs-lookup"><span data-stu-id="44df5-103">CImageDisplay.RefreshDisplayType method</span></span>

<span data-ttu-id="44df5-104">O `RefreshDisplayType` método atualiza o formato de vídeo do objeto para corresponder à exibição especificada.</span><span class="sxs-lookup"><span data-stu-id="44df5-104">The `RefreshDisplayType` method updates the object's video format to match the specified display.</span></span>

## <a name="syntax"></a><span data-ttu-id="44df5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44df5-105">Syntax</span></span>


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a><span data-ttu-id="44df5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44df5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44df5-107">*szDeviceName*</span><span class="sxs-lookup"><span data-stu-id="44df5-107">*szDeviceName*</span></span> 
</dt> <dd>

<span data-ttu-id="44df5-108">Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI.</span><span class="sxs-lookup"><span data-stu-id="44df5-108">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="44df5-109">Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="44df5-109">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44df5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44df5-110">Return value</span></span>

<span data-ttu-id="44df5-111">Retorna S \_ OK se for bem-sucedido ou E \_ falhar se não for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="44df5-111">Returns S\_OK if successful, or E\_FAIL if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="44df5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="44df5-112">Remarks</span></span>

<span data-ttu-id="44df5-113">Esse método inicializa o membro de **\_ exibição m** para um tipo de vídeo que corresponde ao modo de exibição no dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="44df5-113">This method initializes the **m\_Display** member to a video type that corresponds to the display mode on the specified device.</span></span>

<span data-ttu-id="44df5-114">Chame esse método sempre que uma \_ mensagem do WM DISplaychanged for recebida ou para especificar um dispositivo de vídeo secundário.</span><span class="sxs-lookup"><span data-stu-id="44df5-114">Call this method whenever a WM\_DISPLAYCHANGED message is received, or to specify a secondary display device.</span></span>

## <a name="requirements"></a><span data-ttu-id="44df5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44df5-115">Requirements</span></span>



| <span data-ttu-id="44df5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44df5-116">Requirement</span></span> | <span data-ttu-id="44df5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="44df5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44df5-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44df5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="44df5-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44df5-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44df5-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44df5-120">Library</span></span><br/> | <dl> <span data-ttu-id="44df5-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="44df5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44df5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="44df5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44df5-123">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="44df5-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




