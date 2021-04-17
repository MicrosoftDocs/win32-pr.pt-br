---
description: Retorna o tipo de dispositivo de hardware que o objeto do Tablet representa, como mouse, caneta ou toque.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'Método ITablet2:: GetDeviceKind'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772723"
---
# <a name="itablet2getdevicekind-method"></a><span data-ttu-id="0f386-103">Método ITablet2:: GetDeviceKind</span><span class="sxs-lookup"><span data-stu-id="0f386-103">ITablet2::GetDeviceKind method</span></span>

<span data-ttu-id="0f386-104">Retorna o tipo de dispositivo de hardware que o objeto do Tablet representa, como mouse, caneta ou toque.</span><span class="sxs-lookup"><span data-stu-id="0f386-104">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f386-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f386-105">Syntax</span></span>


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a><span data-ttu-id="0f386-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f386-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f386-107">*pKind* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f386-107">*pKind* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f386-108">Valor de enumeração que indica o tipo de Tablet, como mouse, caneta ou toque.</span><span class="sxs-lookup"><span data-stu-id="0f386-108">Enumeration value that indicates the type of tablet such as mouse, pen or touch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f386-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f386-109">Return value</span></span>

<span data-ttu-id="0f386-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0f386-110">This method can return one of these values.</span></span>



| <span data-ttu-id="0f386-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0f386-111">Return code</span></span>                                                                            | <span data-ttu-id="0f386-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f386-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0f386-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f386-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0f386-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0f386-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0f386-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0f386-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0f386-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="0f386-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f386-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f386-117">Remarks</span></span>

<span data-ttu-id="0f386-118">Essa interface e o método foram introduzidos no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0f386-118">This interface and method were introduced in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f386-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f386-119">Requirements</span></span>



| <span data-ttu-id="0f386-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f386-120">Requirement</span></span> | <span data-ttu-id="0f386-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0f386-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f386-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f386-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0f386-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0f386-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f386-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f386-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0f386-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0f386-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0f386-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f386-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f386-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f386-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f386-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f386-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f386-129">**Interface ITablet2**</span><span class="sxs-lookup"><span data-stu-id="0f386-129">**ITablet2 Interface**</span></span>](itablet2.md)
</dt> <dt>

[<span data-ttu-id="0f386-130">**Enumeração de tipo de \_ dispositivo tablet \_**</span><span class="sxs-lookup"><span data-stu-id="0f386-130">**TABLET\_DEVICE\_KIND Enumeration**</span></span>](tablet-device-kind.md)
</dt> <dt>

[<span data-ttu-id="0f386-131">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="0f386-131">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




