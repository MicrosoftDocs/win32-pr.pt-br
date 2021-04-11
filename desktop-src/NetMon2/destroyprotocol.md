---
description: A função DestroyProtocol destrói o protocolo criado pela função createprotocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Função DestroyProtocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169376"
---
# <a name="destroyprotocol-function"></a><span data-ttu-id="2be66-103">Função DestroyProtocol</span><span class="sxs-lookup"><span data-stu-id="2be66-103">DestroyProtocol function</span></span>

<span data-ttu-id="2be66-104">A função **DestroyProtocol** destrói o protocolo criado pela função **createprotocol** .</span><span class="sxs-lookup"><span data-stu-id="2be66-104">The **DestroyProtocol** function destroys the protocol that the **CreateProtocol** function creates.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2be66-105">Syntax</span></span>


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="2be66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2be66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be66-107">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2be66-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be66-108">Identificador para o protocolo a ser destruído.</span><span class="sxs-lookup"><span data-stu-id="2be66-108">Handle to the protocol to be destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be66-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2be66-109">Return value</span></span>

<span data-ttu-id="2be66-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2be66-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="2be66-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2be66-111">Remarks</span></span>

<span data-ttu-id="2be66-112">A DLL do analisador chama a função **DestroyProtocol** durante sua implementação de [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="2be66-112">The parser DLL calls the **DestroyProtocol** function during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="2be66-113">**DestroyProtocol** é chamado quando o sistema operacional vai descarregar a dll.</span><span class="sxs-lookup"><span data-stu-id="2be66-113">**DestroyProtocol** is called when the operating system is going to unload the DLL.</span></span>



| <span data-ttu-id="2be66-114">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="2be66-114">For information on</span></span>                                        | <span data-ttu-id="2be66-115">Consulte</span><span class="sxs-lookup"><span data-stu-id="2be66-115">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2be66-116">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="2be66-116">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="2be66-117">Analisadores</span><span class="sxs-lookup"><span data-stu-id="2be66-117">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="2be66-118">A implementação de **DllMain** inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="2be66-118">How to implement **DllMain** includes an example.</span></span>         | [<span data-ttu-id="2be66-119">Implementando DllMain</span><span class="sxs-lookup"><span data-stu-id="2be66-119">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="2be66-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be66-120">Requirements</span></span>



| <span data-ttu-id="2be66-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be66-121">Requirement</span></span> | <span data-ttu-id="2be66-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2be66-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2be66-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2be66-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2be66-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2be66-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2be66-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2be66-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2be66-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2be66-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2be66-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2be66-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2be66-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2be66-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2be66-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2be66-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2be66-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2be66-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2be66-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2be66-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2be66-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2be66-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be66-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2be66-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be66-134">DllMain</span><span class="sxs-lookup"><span data-stu-id="2be66-134">DllMain</span></span>](dllmain-parser.md)
</dt> </dl>

 

 




