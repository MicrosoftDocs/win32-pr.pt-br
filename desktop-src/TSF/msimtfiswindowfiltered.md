---
title: Função MsimtfIsWindowFiltered
description: A função MsimtfIsWindowFiltered testa se a janela especificada é filtrada por AIMM (Active Input Method Manager).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Estrutura de serviços de texto da função MsimtfIsWindowFiltered
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086128"
---
# <a name="msimtfiswindowfiltered-function"></a><span data-ttu-id="9db02-104">Função MsimtfIsWindowFiltered</span><span class="sxs-lookup"><span data-stu-id="9db02-104">MsimtfIsWindowFiltered function</span></span>

<span data-ttu-id="9db02-105">A função **MsimtfIsWindowFiltered** testa se a janela especificada é filtrada por AIMM (Active Input Method Manager).</span><span class="sxs-lookup"><span data-stu-id="9db02-105">The **MsimtfIsWindowFiltered** function tests if the given window is filtered by AIMM (Active Input Method Manager).</span></span>

## <a name="syntax"></a><span data-ttu-id="9db02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9db02-106">Syntax</span></span>


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="9db02-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9db02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db02-108">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9db02-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db02-109">Um identificador de janela a ser testado.</span><span class="sxs-lookup"><span data-stu-id="9db02-109">A window handle to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db02-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9db02-110">Return value</span></span>



| <span data-ttu-id="9db02-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9db02-111">Return code</span></span>                                                                          | <span data-ttu-id="9db02-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9db02-112">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9db02-113"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="9db02-113"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="9db02-114">Se esta janela for filtrada pelo Gerenciador de método de entrada ativo.</span><span class="sxs-lookup"><span data-stu-id="9db02-114">If this window is filtered by Active Input Method Manager.</span></span><br/>     |
| <dl> <span data-ttu-id="9db02-115"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="9db02-115"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="9db02-116">Se essa janela não for filtrada pelo Gerenciador de método de entrada ativo.</span><span class="sxs-lookup"><span data-stu-id="9db02-116">If this window is not filtered by Active Input Method Manager.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9db02-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9db02-117">Remarks</span></span>

<span data-ttu-id="9db02-118">Uma janela pode ser filtrada por IActiveIMMApp:: FilterClientWindows.</span><span class="sxs-lookup"><span data-stu-id="9db02-118">A window can be filtered by IActiveIMMApp::FilterClientWindows.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db02-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9db02-119">Requirements</span></span>



| <span data-ttu-id="9db02-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db02-120">Requirement</span></span> | <span data-ttu-id="9db02-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9db02-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9db02-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9db02-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9db02-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9db02-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9db02-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9db02-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9db02-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9db02-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9db02-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9db02-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db02-127"><dt>Msimtf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db02-127"><dt>Msimtf.dll</dt></span></span> </dl> |



 

 





