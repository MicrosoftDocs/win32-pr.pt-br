---
description: A estrutura ENTRYPOINTs define os pontos de entrada para as funções de exportação que Monitor de Rede usa para operar o analisador.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Estrutura de ENTRYPOINTs (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920713"
---
# <a name="entrypoints-structure"></a><span data-ttu-id="5b179-103">Estrutura de ENTRYPOINTs</span><span class="sxs-lookup"><span data-stu-id="5b179-103">ENTRYPOINTS structure</span></span>

<span data-ttu-id="5b179-104">A estrutura **entryPoints** define os pontos de entrada para as funções de exportação que monitor de rede usa para operar o analisador.</span><span class="sxs-lookup"><span data-stu-id="5b179-104">The **ENTRYPOINTS** structure defines the entry points to the export functions that Network Monitor uses to operate the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b179-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b179-105">Syntax</span></span>


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a><span data-ttu-id="5b179-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5b179-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b179-107">**Registrar**</span><span class="sxs-lookup"><span data-stu-id="5b179-107">**Register**</span></span>
</dt> <dd>

<span data-ttu-id="5b179-108">Ponteiro para a implementação da função de [*especialista de registro*](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="5b179-108">Pointer to the implementation of the [*Register expert*](register-expert.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5b179-109">**Cancelar registro**</span><span class="sxs-lookup"><span data-stu-id="5b179-109">**Deregister**</span></span>
</dt> <dd>

<span data-ttu-id="5b179-110">Ponteiro para a implementação da função de [**cancelamento de registro**](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="5b179-110">Pointer to the implementation of the [**Deregister**](deregister.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5b179-111">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="5b179-111">**RecognizeFrame**</span></span>
</dt> <dd>

<span data-ttu-id="5b179-112">Ponteiro para a implementação da função de exportação [**RecognizeFrame**](recognizeframe.md) .</span><span class="sxs-lookup"><span data-stu-id="5b179-112">Pointer to the implementation of the [**RecognizeFrame**](recognizeframe.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="5b179-113">**Anexarproperties**</span><span class="sxs-lookup"><span data-stu-id="5b179-113">**AttachProperties**</span></span>
</dt> <dd>

<span data-ttu-id="5b179-114">Ponteiro para a implementação da função de exportação [**attachproperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="5b179-114">Pointer to the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="5b179-115">**Formatproperties**</span><span class="sxs-lookup"><span data-stu-id="5b179-115">**FormatProperties**</span></span>
</dt> <dd>

<span data-ttu-id="5b179-116">Ponteiro para a implementação da função de exportação [**formatproperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="5b179-116">Pointer to the implementation of the [**FormatProperties**](formatproperties.md) export function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b179-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b179-117">Remarks</span></span>

<span data-ttu-id="5b179-118">A função **createprotocol** usa a estrutura **entryPoints** para fornecer ponteiros para monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="5b179-118">The **CreateProtocol** function uses the **ENTRYPOINTS** structure to provide pointers to Network Monitor.</span></span> <span data-ttu-id="5b179-119">Os ponteiros devem ser especificados na ordem identificada na seção membros anteriores.</span><span class="sxs-lookup"><span data-stu-id="5b179-119">The pointers must be specified in the order identified in the previous Members section.</span></span>

<span data-ttu-id="5b179-120">A função [**formatproperties**](formatproperties.md) não precisará ser implementada se monitor de rede nunca exibirá os dados do protocolo.</span><span class="sxs-lookup"><span data-stu-id="5b179-120">The [**FormatProperties**](formatproperties.md) function does not need to be implemented if Network Monitor will never display the protocol data.</span></span> <span data-ttu-id="5b179-121">Por exemplo, **formatproperties** não precisa ser implementado se um aplicativo de exportação usar a saída do analisador e monitor de rede não exibir a saída.</span><span class="sxs-lookup"><span data-stu-id="5b179-121">For example, **FormatProperties** does not need to be implemented if an export application uses the output from the parser, and Network Monitor does not display the output.</span></span>



| <span data-ttu-id="5b179-122">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="5b179-122">For information on</span></span>                                        | <span data-ttu-id="5b179-123">Consulte</span><span class="sxs-lookup"><span data-stu-id="5b179-123">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5b179-124">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="5b179-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="5b179-125">Analisadores</span><span class="sxs-lookup"><span data-stu-id="5b179-125">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="5b179-126">A implementação de **DllMain**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="5b179-126">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="5b179-127">Implementando DllMain</span><span class="sxs-lookup"><span data-stu-id="5b179-127">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="5b179-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b179-128">Requirements</span></span>



| <span data-ttu-id="5b179-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b179-129">Requirement</span></span> | <span data-ttu-id="5b179-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5b179-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b179-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b179-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5b179-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5b179-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5b179-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b179-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5b179-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5b179-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5b179-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5b179-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b179-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b179-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b179-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b179-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b179-138">Anexarproperties</span><span class="sxs-lookup"><span data-stu-id="5b179-138">AttachProperties</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="5b179-139">Createprotocol</span><span class="sxs-lookup"><span data-stu-id="5b179-139">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="5b179-140">Cancelar registro</span><span class="sxs-lookup"><span data-stu-id="5b179-140">Deregister</span></span>](deregister.md)
</dt> <dt>

[<span data-ttu-id="5b179-141">Formatproperties</span><span class="sxs-lookup"><span data-stu-id="5b179-141">FormatProperties</span></span>](formatproperties.md)
</dt> <dt>

[<span data-ttu-id="5b179-142">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="5b179-142">RecognizeFrame</span></span>](recognizeframe.md)
</dt> <dt>

[<span data-ttu-id="5b179-143">Registrar</span><span class="sxs-lookup"><span data-stu-id="5b179-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




