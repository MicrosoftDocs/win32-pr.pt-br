---
title: Função WsSetAutoFail (WebServicesDebug. h)
description: Define o próximo ponto para injetar uma falha. Esta é uma função somente depuração.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Serviços Web da função WsSetAutoFail para Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499628"
---
# <a name="wssetautofail-function"></a><span data-ttu-id="cdf99-105">Função WsSetAutoFail</span><span class="sxs-lookup"><span data-stu-id="cdf99-105">WsSetAutoFail function</span></span>

<span data-ttu-id="cdf99-106">Define o próximo ponto para injetar uma falha.</span><span class="sxs-lookup"><span data-stu-id="cdf99-106">Sets the next point to inject a failure.</span></span> <span data-ttu-id="cdf99-107">Esta é uma função somente depuração.</span><span class="sxs-lookup"><span data-stu-id="cdf99-107">This is a DEBUG ONLY function.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf99-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdf99-108">Syntax</span></span>


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="cdf99-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdf99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdf99-110">*contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="cdf99-110">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf99-111">Especifica quantas operações antes de falhas começam a ocorrer.</span><span class="sxs-lookup"><span data-stu-id="cdf99-111">Specifies how many operations before failures begin to occur.</span></span>

</dd> <dt>

<span data-ttu-id="cdf99-112">*erro* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cdf99-112">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf99-113">Um ponteiro para um objeto de [ \_ erro WS](ws-error.md) em que informações adicionais sobre o erro devem ser armazenadas se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="cdf99-113">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdf99-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cdf99-114">Return value</span></span>

<span data-ttu-id="cdf99-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cdf99-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cdf99-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cdf99-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf99-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdf99-117">Requirements</span></span>



| <span data-ttu-id="cdf99-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdf99-118">Requirement</span></span> | <span data-ttu-id="cdf99-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cdf99-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf99-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdf99-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf99-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cdf99-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdf99-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdf99-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf99-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="cdf99-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cdf99-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cdf99-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdf99-125"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdf99-125"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





