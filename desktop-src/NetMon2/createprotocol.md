---
description: A função createprotocol notifica Monitor de Rede de que existe um analisador de protocolo específico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Função createprotocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091725"
---
# <a name="createprotocol-function"></a><span data-ttu-id="27cc6-103">Função createprotocol</span><span class="sxs-lookup"><span data-stu-id="27cc6-103">CreateProtocol function</span></span>

<span data-ttu-id="27cc6-104">A função **createprotocol** notifica monitor de rede de que existe um analisador de protocolo específico.</span><span class="sxs-lookup"><span data-stu-id="27cc6-104">The **CreateProtocol** function notifies Network Monitor that a specific protocol parser exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="27cc6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27cc6-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a><span data-ttu-id="27cc6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27cc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27cc6-107">*ProtocolName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27cc6-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27cc6-108">Nome do protocolo que o analisador detectará.</span><span class="sxs-lookup"><span data-stu-id="27cc6-108">Name of the protocol the parser will detect.</span></span>

</dd> <dt>

<span data-ttu-id="27cc6-109">*lpEntryPoints* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27cc6-109">*lpEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27cc6-110">Uma estrutura de [entryPoints](entrypoints.md) que contém os pontos de entrada da dll do analisador restante.</span><span class="sxs-lookup"><span data-stu-id="27cc6-110">An [ENTRYPOINTS](entrypoints.md) structure that contains the remaining parser DLL entry points.</span></span> <span data-ttu-id="27cc6-111">Consulte comentários para obter uma lista das funções de exportação às quais cada ponto de entrada faz referência.</span><span class="sxs-lookup"><span data-stu-id="27cc6-111">See Remarks for a list of the export functions that each entry point references.</span></span> <span data-ttu-id="27cc6-112">Os pontos de entrada devem ser fornecidos na ordem que a estrutura de **entryPoints** especifica.</span><span class="sxs-lookup"><span data-stu-id="27cc6-112">Entry points must be provided in the order that the **ENTRYPOINTS** structure specifies.</span></span>

</dd> <dt>

<span data-ttu-id="27cc6-113">*cbEntryPoints* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27cc6-113">*cbEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27cc6-114">O tamanho da estrutura de **entryPoints** .</span><span class="sxs-lookup"><span data-stu-id="27cc6-114">The size of the **ENTRYPOINTS** structure.</span></span> <span data-ttu-id="27cc6-115">Monitor de Rede fornece uma \_ macro de tamanho de entryPoints que você pode usar para especificar o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="27cc6-115">Network Monitor provides an ENTRYPOINTS\_SIZE macro that you can use to specify the size of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27cc6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27cc6-116">Return value</span></span>

<span data-ttu-id="27cc6-117">Se a função for bem-sucedida, o valor de retorno será um identificador para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="27cc6-117">If the function is successful, the return value is a handle to the protocol.</span></span>

<span data-ttu-id="27cc6-118">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="27cc6-118">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="27cc6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="27cc6-119">Remarks</span></span>

<span data-ttu-id="27cc6-120">A DLL do analisador chama **createprotocol** durante sua implementação de [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="27cc6-120">The parser DLL calls **CreateProtocol** during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="27cc6-121">A função **createprotocol** é chamada quando o sistema operacional carrega a DLL do analisador pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="27cc6-121">The **CreateProtocol** function is called when the operating system loads the parser DLL for the first time.</span></span>

<span data-ttu-id="27cc6-122">Os pontos de entrada referenciados no parâmetro *lpEntryPoints* incluem ponteiros para as seguintes funções de exportação que devem ser fornecidas na ordem apresentada aqui.</span><span class="sxs-lookup"><span data-stu-id="27cc6-122">The entry points referenced in the *lpEntryPoints* parameter include pointers to the following export functions that must be provided in the order presented here.</span></span>

-   [<span data-ttu-id="27cc6-123">Registrar</span><span class="sxs-lookup"><span data-stu-id="27cc6-123">Register</span></span>](register-parser.md)
-   [<span data-ttu-id="27cc6-124">Cancelar registro</span><span class="sxs-lookup"><span data-stu-id="27cc6-124">Deregister</span></span>](deregister.md)
-   [<span data-ttu-id="27cc6-125">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="27cc6-125">RecognizeFrame</span></span>](recognizeframe.md)
-   [<span data-ttu-id="27cc6-126">Anexarproperties</span><span class="sxs-lookup"><span data-stu-id="27cc6-126">AttachProperties</span></span>](attachproperties.md)
-   [<span data-ttu-id="27cc6-127">Formatproperties</span><span class="sxs-lookup"><span data-stu-id="27cc6-127">FormatProperties</span></span>](formatproperties.md)



| <span data-ttu-id="27cc6-128">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="27cc6-128">For information on</span></span>                                                                                 | <span data-ttu-id="27cc6-129">Consulte</span><span class="sxs-lookup"><span data-stu-id="27cc6-129">See</span></span>                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="27cc6-130">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="27cc6-130">What parsers are, and how they work with Network Monitor.</span></span>                                          | [<span data-ttu-id="27cc6-131">Analisadores</span><span class="sxs-lookup"><span data-stu-id="27cc6-131">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="27cc6-132">Como implementar **DllMain** inclui um exemplo de chamada de **createprotocol** em **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="27cc6-132">How to implement **DllMain** includes an example of calling **CreateProtocol** within **DllMain**.</span></span> | [<span data-ttu-id="27cc6-133">Implementando DllMain</span><span class="sxs-lookup"><span data-stu-id="27cc6-133">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="27cc6-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27cc6-134">Requirements</span></span>



| <span data-ttu-id="27cc6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="27cc6-135">Requirement</span></span> | <span data-ttu-id="27cc6-136">Valor</span><span class="sxs-lookup"><span data-stu-id="27cc6-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27cc6-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27cc6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="27cc6-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="27cc6-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="27cc6-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27cc6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="27cc6-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="27cc6-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="27cc6-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="27cc6-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="27cc6-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="27cc6-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="27cc6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27cc6-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="27cc6-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27cc6-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="27cc6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="27cc6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27cc6-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27cc6-146"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27cc6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="27cc6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27cc6-148">DllMain</span><span class="sxs-lookup"><span data-stu-id="27cc6-148">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

