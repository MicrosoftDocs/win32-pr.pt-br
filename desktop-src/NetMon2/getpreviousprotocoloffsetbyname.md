---
description: A função GetPreviousProtocolOffsetByName retorna a instância anterior de um determinado protocolo.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Função GetPreviousProtocolOffsetByName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779599"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a><span data-ttu-id="2ce1f-103">Função GetPreviousProtocolOffsetByName</span><span class="sxs-lookup"><span data-stu-id="2ce1f-103">GetPreviousProtocolOffsetByName function</span></span>

<span data-ttu-id="2ce1f-104">A função **GetPreviousProtocolOffsetByName** retorna a instância anterior de um determinado protocolo.</span><span class="sxs-lookup"><span data-stu-id="2ce1f-104">The **GetPreviousProtocolOffsetByName** function returns the previous instance of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ce1f-105">Syntax</span></span>


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a><span data-ttu-id="2ce1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ce1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce1f-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ce1f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce1f-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="2ce1f-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="2ce1f-109">*dwStartOffset* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ce1f-109">*dwStartOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce1f-110">Deslocamento no quadro.</span><span class="sxs-lookup"><span data-stu-id="2ce1f-110">Offset in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="2ce1f-111">*szProtocolName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ce1f-111">*szProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce1f-112">Nome do protocolo que você deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="2ce1f-112">Name of the protocol you want to search for.</span></span>

</dd> <dt>

<span data-ttu-id="2ce1f-113">*pdwPreviousOffset* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2ce1f-113">*pdwPreviousOffset* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce1f-114">Ponteiro para um **DWORD** que contém o deslocamento para o protocolo anterior (se a função tiver sucesso).</span><span class="sxs-lookup"><span data-stu-id="2ce1f-114">Pointer to a **DWORD** that contains the offset to the previous protocol (if the function succeeds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce1f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ce1f-115">Return value</span></span>

<span data-ttu-id="2ce1f-116">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="2ce1f-116">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2ce1f-117">Se a função não for bem-sucedida, o valor de retorno será o \_ protocolo NMERR \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="2ce1f-117">If the function is unsuccessful, the return value is NMERR\_PROTOCOL\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce1f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ce1f-118">Remarks</span></span>

<span data-ttu-id="2ce1f-119">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar o **GetPreviousProtocolOffsetByName**.</span><span class="sxs-lookup"><span data-stu-id="2ce1f-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPreviousProtocolOffsetByName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce1f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ce1f-120">Requirements</span></span>



| <span data-ttu-id="2ce1f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ce1f-121">Requirement</span></span> | <span data-ttu-id="2ce1f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2ce1f-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce1f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ce1f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce1f-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ce1f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2ce1f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ce1f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce1f-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ce1f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2ce1f-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ce1f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ce1f-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1f-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2ce1f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ce1f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ce1f-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1f-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2ce1f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2ce1f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ce1f-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1f-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




