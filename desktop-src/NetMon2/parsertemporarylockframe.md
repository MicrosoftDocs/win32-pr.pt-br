---
description: A função ParserTemporaryLockFrame bloqueia um quadro quando ele entra em um analisador e desbloqueia o quadro quando a função sai do analisador.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Função ParserTemporaryLockFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771836"
---
# <a name="parsertemporarylockframe-function"></a><span data-ttu-id="4d3d8-103">Função ParserTemporaryLockFrame</span><span class="sxs-lookup"><span data-stu-id="4d3d8-103">ParserTemporaryLockFrame function</span></span>

<span data-ttu-id="4d3d8-104">A função **ParserTemporaryLockFrame** bloqueia um quadro quando ele entra em um analisador e desbloqueia o quadro quando a função sai do analisador.</span><span class="sxs-lookup"><span data-stu-id="4d3d8-104">The **ParserTemporaryLockFrame** function locks a frame when it enters a parser and unlocks the frame when the function exits the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d3d8-105">Syntax</span></span>


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="4d3d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d3d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d3d8-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d3d8-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d3d8-108">Identificador para o quadro para o qual o analisador aponta.</span><span class="sxs-lookup"><span data-stu-id="4d3d8-108">Handle to the frame that the parser points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d3d8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d3d8-109">Return value</span></span>

<span data-ttu-id="4d3d8-110">Se a função for bem-sucedida, o valor de retorno será um ponteiro para o primeiro byte de dados no quadro.</span><span class="sxs-lookup"><span data-stu-id="4d3d8-110">If the function is successful, the return value is a pointer to the first byte of data in the frame.</span></span>

<span data-ttu-id="4d3d8-111">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4d3d8-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d3d8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d3d8-112">Remarks</span></span>

<span data-ttu-id="4d3d8-113">Os analisadores não devem chamar a função **LockFrame** .</span><span class="sxs-lookup"><span data-stu-id="4d3d8-113">Parsers should not call the **LockFrame** function.</span></span> <span data-ttu-id="4d3d8-114">Se um analisador usar um bloqueio e, em seguida, gerar uma falha ou retornar sem desbloquear o quadro, o analisador deixará o sistema em um estado em que ele não possa alterar protocolos nem recortar ou copiar quadros.</span><span class="sxs-lookup"><span data-stu-id="4d3d8-114">If a parser takes a lock and then generates a fault or returns without unlocking the frame, the parser leaves the system in a state where it cannot change protocols or cut or copy frames.</span></span> <span data-ttu-id="4d3d8-115">Os analisadores devem usar a função **ParserTemporaryLockFrame** , que concede um bloqueio somente durante o contexto da entrada da função no analisador.</span><span class="sxs-lookup"><span data-stu-id="4d3d8-115">Parsers should use the **ParserTemporaryLockFrame** function, which grants a lock only during the context of the function entry into the parser.</span></span> <span data-ttu-id="4d3d8-116">Ao sair do analisador, o bloqueio para esse quadro é liberado.</span><span class="sxs-lookup"><span data-stu-id="4d3d8-116">On exit from the parser, the lock for that frame is released.</span></span> <span data-ttu-id="4d3d8-117">Como resultado, o ponteiro será válido somente depois que o analisador retornar da chamada para a função **attachproperties** ou **RecognizeFrame** .</span><span class="sxs-lookup"><span data-stu-id="4d3d8-117">As a result, the pointer will be valid only after the parser returns from the call to the **AttachProperties** or **RecognizeFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d3d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d3d8-118">Requirements</span></span>



| <span data-ttu-id="4d3d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d3d8-119">Requirement</span></span> | <span data-ttu-id="4d3d8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3d8-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3d8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d3d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4d3d8-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d3d8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4d3d8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d3d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4d3d8-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d3d8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4d3d8-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4d3d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d3d8-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d8-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4d3d8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d3d8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d3d8-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d8-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d3d8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4d3d8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d3d8-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d8-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




