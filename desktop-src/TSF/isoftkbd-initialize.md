---
title: Método de inicialização de ISoftKbd (Softkbdc. h)
description: O método de inicialização ISoftKbd inicializa todos os campos necessários para um teclado virtual e gera layouts de teclado flexível padrão.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Inicializar o método de estrutura de serviços de texto
- Inicializar o método Text Services Framework, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método Initialize
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644326"
---
# <a name="isoftkbdinitialize-method"></a><span data-ttu-id="e4af5-106">Método ISoftKbd:: Initialize</span><span class="sxs-lookup"><span data-stu-id="e4af5-106">ISoftKbd::Initialize method</span></span>

<span data-ttu-id="e4af5-107">O método **ISoftKbd:: Initialize** inicializa todos os campos necessários para um teclado virtual e gera layouts de teclado flexível padrão.</span><span class="sxs-lookup"><span data-stu-id="e4af5-107">The **ISoftKbd::Initialize** method initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4af5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4af5-108">Syntax</span></span>


```C++
HRESULT Initialize();
```



## <a name="parameters"></a><span data-ttu-id="e4af5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4af5-109">Parameters</span></span>

<span data-ttu-id="e4af5-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e4af5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4af5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4af5-111">Return value</span></span>

<span data-ttu-id="e4af5-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e4af5-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e4af5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e4af5-113">Value</span></span>                                                                                | <span data-ttu-id="e4af5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4af5-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e4af5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4af5-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e4af5-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e4af5-116">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e4af5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4af5-117">Requirements</span></span>



| <span data-ttu-id="e4af5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4af5-118">Requirement</span></span> | <span data-ttu-id="e4af5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e4af5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4af5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4af5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4af5-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4af5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e4af5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4af5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4af5-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4af5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4af5-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e4af5-124">Redistributable</span></span><br/>          | <span data-ttu-id="e4af5-125">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e4af5-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="e4af5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4af5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4af5-127"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4af5-127"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="e4af5-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="e4af5-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4af5-129"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4af5-129"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4af5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e4af5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4af5-131"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4af5-131"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4af5-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e4af5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4af5-133">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="e4af5-133">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





