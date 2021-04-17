---
description: A função de exportação DllMain para o analisador identifica a existência do analisador e libera os recursos que Monitor de Rede usa para o analisador. DllMain deve ser implementado em todas as DLLs do analisador.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Função de retorno de chamada do DllMain Parser (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783260"
---
# <a name="dllmain-parser-callback-function"></a><span data-ttu-id="c1e67-104">Função de retorno de chamada de análise DllMain</span><span class="sxs-lookup"><span data-stu-id="c1e67-104">DllMain Parser callback function</span></span>

<span data-ttu-id="c1e67-105">A função de exportação **DllMain** para o analisador identifica a existência do analisador e libera os recursos que monitor de rede usa para o analisador.</span><span class="sxs-lookup"><span data-stu-id="c1e67-105">The **DllMain** export function for the parser identifies the existence of the parser, and releases resources that Network Monitor uses for the parser.</span></span> <span data-ttu-id="c1e67-106">**DllMain** deve ser implementado em todas as DLLs do analisador.</span><span class="sxs-lookup"><span data-stu-id="c1e67-106">**DllMain** must be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e67-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1e67-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="c1e67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1e67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e67-109">*HINSTANCE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1e67-109">*hInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e67-110">Identificador para uma instância do analisador.</span><span class="sxs-lookup"><span data-stu-id="c1e67-110">Handle to an instance of the parser.</span></span>

</dd> <dt>

<span data-ttu-id="c1e67-111">*Comando* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1e67-111">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e67-112">Indicador para determinar por que a função é chamada.</span><span class="sxs-lookup"><span data-stu-id="c1e67-112">Indicator to determine why the function is called.</span></span> <span data-ttu-id="c1e67-113">Para obter uma lista de todos os sinalizadores possíveis, consulte [DllMain](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="c1e67-113">For a list of all possible flags, see [DllMain](/windows/desktop/Dlls/dllmain).</span></span> <span data-ttu-id="c1e67-114">A implementação do analisador deve processar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1e67-114">The parser implementation must process the following values.</span></span>



| <span data-ttu-id="c1e67-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c1e67-115">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="c1e67-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c1e67-116">Meaning</span></span>                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="c1e67-117"><dt>**\_anexar processo de dll \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1e67-117"><dt>**DLL\_PROCESS\_ATTACH**</dt></span></span> </dl> | <span data-ttu-id="c1e67-118">Quando **DllMain** é chamado pela primeira vez, a DLL deve chamar [createprotocol](createprotocol.md) para fornecer informações a monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="c1e67-118">When **DllMain** is called for the first time, the DLL must call [CreateProtocol](createprotocol.md) to provide information to Network Monitor.</span></span> <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="c1e67-119"><dt>**desanexar processo de DLL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1e67-119"><dt>**DLL\_PROCESS\_DETACH**</dt></span></span> </dl> | <span data-ttu-id="c1e67-120">Quando **DllMain** é chamado pela última vez, a DLL deve chamar [DestroyProtocol](destroyprotocol.md) para liberar os recursos que a dll usa.</span><span class="sxs-lookup"><span data-stu-id="c1e67-120">When **DllMain** is called for the last time, the DLL must call [DestroyProtocol](destroyprotocol.md) to release the resources that the DLL uses.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c1e67-121">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="c1e67-121">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="c1e67-122">Não usado agora.</span><span class="sxs-lookup"><span data-stu-id="c1e67-122">Not used now.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e67-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1e67-123">Return value</span></span>

<span data-ttu-id="c1e67-124">A DLL do analisador sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="c1e67-124">The parser DLL always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e67-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1e67-125">Remarks</span></span>

<span data-ttu-id="c1e67-126">O sistema operacional chama **DllMain** para carregar e descarregar a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="c1e67-126">The operating system calls **DllMain** to load and unload the parser DLL.</span></span> <span data-ttu-id="c1e67-127">Essa função é baseada na função [DllMain](/windows/desktop/Dlls/dllmain) da biblioteca de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c1e67-127">This function is based on the dynamic-link library [DllMain](/windows/desktop/Dlls/dllmain) function.</span></span>

<span data-ttu-id="c1e67-128">Você também pode usar a implementação de **DllMain** para armazenar uma instância de um analisador para uso no futuro.</span><span class="sxs-lookup"><span data-stu-id="c1e67-128">You can also use the implementation of **DllMain** to store an instance of a parser for use in the future.</span></span> <span data-ttu-id="c1e67-129">Por exemplo, você pode armazenar uma instância de DLL do parser e usá-la para uma chamada do sistema no futuro.</span><span class="sxs-lookup"><span data-stu-id="c1e67-129">For example, you can store a parser DLL instance, and then use it for a system call in the future.</span></span>



| <span data-ttu-id="c1e67-130">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="c1e67-130">For information on</span></span>                                        | <span data-ttu-id="c1e67-131">Consulte</span><span class="sxs-lookup"><span data-stu-id="c1e67-131">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c1e67-132">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="c1e67-132">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="c1e67-133">Analisadores</span><span class="sxs-lookup"><span data-stu-id="c1e67-133">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="c1e67-134">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="c1e67-134">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="c1e67-135">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="c1e67-135">Parser DLL Architecture</span></span>](parser-dll-architecture.md)  |
| <span data-ttu-id="c1e67-136">A implementação de **DllMain**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1e67-136">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="c1e67-137">Implementando DllMain</span><span class="sxs-lookup"><span data-stu-id="c1e67-137">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="c1e67-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1e67-138">Requirements</span></span>



| <span data-ttu-id="c1e67-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1e67-139">Requirement</span></span> | <span data-ttu-id="c1e67-140">Valor</span><span class="sxs-lookup"><span data-stu-id="c1e67-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e67-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1e67-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e67-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1e67-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c1e67-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1e67-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e67-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1e67-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c1e67-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c1e67-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e67-146"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e67-146"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e67-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1e67-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e67-148">Createprotocol</span><span class="sxs-lookup"><span data-stu-id="c1e67-148">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="c1e67-149">DestroyProtocol</span><span class="sxs-lookup"><span data-stu-id="c1e67-149">DestroyProtocol</span></span>](destroyprotocol.md)
</dt> <dt>

[<span data-ttu-id="c1e67-150">DllMain</span><span class="sxs-lookup"><span data-stu-id="c1e67-150">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

