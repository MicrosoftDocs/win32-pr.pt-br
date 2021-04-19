---
description: Move um contexto do Tablet para a frente ou para trás da fila de entrada.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'Método ITabletContextP:: sobreposição'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798253"
---
# <a name="itabletcontextpoverlap-method"></a><span data-ttu-id="b0b8f-103">Método ITabletContextP:: sobreposição</span><span class="sxs-lookup"><span data-stu-id="b0b8f-103">ITabletContextP::Overlap method</span></span>

<span data-ttu-id="b0b8f-104">Move um contexto do Tablet para a frente ou para trás da fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-104">Moves a tablet context to the front or back of the input queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0b8f-105">Syntax</span></span>


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a><span data-ttu-id="b0b8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0b8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b8f-107">*bTop* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0b8f-107">*bTop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b8f-108">Indica se o contexto do Tablet deve ser movido para a parte superior ou inferior da fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-108">Indicates if the tablet context should be moved to the top or bottom of the input queue.</span></span>

</dd> <dt>

<span data-ttu-id="b0b8f-109">*pdwtcid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0b8f-109">*pdwtcid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b8f-110">O identificador de contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-110">The tablet context identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b8f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0b8f-111">Return value</span></span>

<span data-ttu-id="b0b8f-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b0b8f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b0b8f-113">Return code</span></span>                                                                            | <span data-ttu-id="b0b8f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0b8f-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="b0b8f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b8f-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b0b8f-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="b0b8f-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b8f-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b0b8f-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b0b8f-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0b8f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b8f-119">Requirements</span></span>



| <span data-ttu-id="b0b8f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b8f-120">Requirement</span></span> | <span data-ttu-id="b0b8f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b0b8f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b8f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0b8f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b8f-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b0b8f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b0b8f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0b8f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b8f-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b0b8f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b0b8f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0b8f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0b8f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0b8f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b8f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0b8f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b8f-129">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="b0b8f-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




