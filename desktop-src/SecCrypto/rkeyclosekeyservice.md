---
description: Não há suporte para a função RKeyCloseKeyService.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Função RKeyCloseKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827141"
---
# <a name="rkeyclosekeyservice-function"></a><span data-ttu-id="51eb3-103">Função RKeyCloseKeyService</span><span class="sxs-lookup"><span data-stu-id="51eb3-103">RKeyCloseKeyService function</span></span>

<span data-ttu-id="51eb3-104">Não há suporte para a função **RKeyCloseKeyService** .</span><span class="sxs-lookup"><span data-stu-id="51eb3-104">The **RKeyCloseKeyService** function is not supported.</span></span>

<span data-ttu-id="51eb3-105">**Windows Server 2003:** A função **RKeyCloseKeyService** fecha um identificador de serviço de chave aberto por uma chamada anterior à função [**RKeyOpenKeyService**](rkeyopenkeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="51eb3-105">**Windows Server 2003:** The **RKeyCloseKeyService** function closes a key service handle opened by a previous call to the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) function.</span></span> <span data-ttu-id="51eb3-106">Observe que esse comportamento foi alterado com o Windows Server 2003 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="51eb3-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="51eb3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51eb3-107">Syntax</span></span>


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="51eb3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51eb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51eb3-109">*hKeySvcCli* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51eb3-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51eb3-110">Um identificador de [**\_ identificador KEYSVCC**](keysvcc-handle.md) aberto anteriormente pelo [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="51eb3-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="51eb3-111">Esse valor não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="51eb3-111">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51eb3-112">*preservado* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="51eb3-112">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="51eb3-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="51eb3-113">Reserved.</span></span> <span data-ttu-id="51eb3-114">Defina esse valor como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="51eb3-114">Set this value to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51eb3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51eb3-115">Return value</span></span>

<span data-ttu-id="51eb3-116">Se a função for bem-sucedida, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="51eb3-116">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="51eb3-117">Se a função falhar, o valor de retorno será um **ULONG** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="51eb3-117">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="51eb3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51eb3-118">Requirements</span></span>



| <span data-ttu-id="51eb3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51eb3-119">Requirement</span></span> | <span data-ttu-id="51eb3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="51eb3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51eb3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51eb3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51eb3-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="51eb3-122">None supported</span></span><br/>                                                             |
| <span data-ttu-id="51eb3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51eb3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51eb3-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51eb3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51eb3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51eb3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="51eb3-126"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="51eb3-126"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51eb3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="51eb3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51eb3-128">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="51eb3-128">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> <dt>

[<span data-ttu-id="51eb3-129">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="51eb3-129">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




