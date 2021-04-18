---
description: A função GetProtocolStartOffsetHandle retorna o deslocamento de quadro de um determinado protocolo.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Função GetProtocolStartOffsetHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766846"
---
# <a name="getprotocolstartoffsethandle-function"></a><span data-ttu-id="ecee5-103">Função GetProtocolStartOffsetHandle</span><span class="sxs-lookup"><span data-stu-id="ecee5-103">GetProtocolStartOffsetHandle function</span></span>

<span data-ttu-id="ecee5-104">A função **GetProtocolStartOffsetHandle** retorna o deslocamento de quadro de um determinado protocolo.</span><span class="sxs-lookup"><span data-stu-id="ecee5-104">The **GetProtocolStartOffsetHandle** function returns the frame offset of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecee5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecee5-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="ecee5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecee5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecee5-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecee5-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecee5-108">Identificador para um quadro.</span><span class="sxs-lookup"><span data-stu-id="ecee5-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="ecee5-109">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecee5-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecee5-110">Identificador para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="ecee5-110">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecee5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ecee5-111">Return value</span></span>

<span data-ttu-id="ecee5-112">Se a função for bem-sucedida, o valor de retorno será o deslocamento do quadro medido em bytes.</span><span class="sxs-lookup"><span data-stu-id="ecee5-112">If the function is successful, the return value is the offset of the frame   measured in bytes.</span></span>

<span data-ttu-id="ecee5-113">Se a função não for bem-sucedida, o valor de retorno será um (1).</span><span class="sxs-lookup"><span data-stu-id="ecee5-113">If the function is unsuccessful, the return value is one (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="ecee5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecee5-114">Remarks</span></span>

<span data-ttu-id="ecee5-115">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetProtocolStartOffsetHandle** .</span><span class="sxs-lookup"><span data-stu-id="ecee5-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolStartOffsetHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecee5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecee5-116">Requirements</span></span>



| <span data-ttu-id="ecee5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecee5-117">Requirement</span></span> | <span data-ttu-id="ecee5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ecee5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ecee5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecee5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ecee5-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecee5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ecee5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecee5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ecee5-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecee5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ecee5-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ecee5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecee5-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecee5-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ecee5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ecee5-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecee5-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecee5-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ecee5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ecee5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecee5-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecee5-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




