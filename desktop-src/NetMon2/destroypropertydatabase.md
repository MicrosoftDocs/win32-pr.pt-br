---
description: A função DestroyPropertyDatabase libera os recursos usados para criar o banco de dados de propriedades de protocolo.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Função DestroyPropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922620"
---
# <a name="destroypropertydatabase-function"></a><span data-ttu-id="8e1bf-103">Função DestroyPropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="8e1bf-103">DestroyPropertyDatabase function</span></span>

<span data-ttu-id="8e1bf-104">A função **DestroyPropertyDatabase** libera os recursos usados para criar o [*banco de dados de propriedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-104">The **DestroyPropertyDatabase** function releases the resources used to create the protocol [*property database*](p.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e1bf-105">Syntax</span></span>


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="8e1bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e1bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1bf-107">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e1bf-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1bf-108">Identificador para o banco de dados de propriedades a ser destruído.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-108">Handle to the property database to be destroyed.</span></span> <span data-ttu-id="8e1bf-109">O identificador é passado para a DLL do analisador quando Monitor de Rede chama a função de [cancelamento de registro](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="8e1bf-109">The handle is passed to the parser DLL when Network Monitor calls the [Deregister](deregister.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1bf-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e1bf-110">Return value</span></span>

<span data-ttu-id="8e1bf-111">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-111">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8e1bf-112">Se a função não for bem-sucedida, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-112">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="8e1bf-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8e1bf-113">Return code</span></span>                                                                                              | <span data-ttu-id="8e1bf-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e1bf-114">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="8e1bf-115"><dt>**\_erro interno de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e1bf-115"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="8e1bf-116">Ocorreu um erro interno.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-116">An internal error occurred.</span></span> <br/>    |
| <dl> <span data-ttu-id="8e1bf-117"><dt>**NMERR \_ HPROTOCOL inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e1bf-117"><dt>**NMERR\_INVALID\_HPROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="8e1bf-118">Identificador inválido em *hProtocol*.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-118">Invalid handle in *hProtocol*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e1bf-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e1bf-119">Remarks</span></span>

<span data-ttu-id="8e1bf-120">A função **DestroyPropertyDatabase** deve ser chamada somente ao implementar a função de exportação de [cancelamento de registro](deregister.md) para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-120">The **DestroyPropertyDatabase** function should be called only when implementing the [Deregister](deregister.md) export function for the protocol.</span></span> <span data-ttu-id="8e1bf-121">Para DLLs do analisador que dão suporte a vários protocolos, a função **DestroyPropertyDatabase** é chamada para cada implementação de **cancelamento de registro**.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-121">For parser DLLs that support multiple protocols, the **DestroyPropertyDatabase** function is called for each implementation of **Deregister**.</span></span>



| <span data-ttu-id="8e1bf-122">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="8e1bf-122">For information on</span></span>                                        | <span data-ttu-id="8e1bf-123">Consulte</span><span class="sxs-lookup"><span data-stu-id="8e1bf-123">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="8e1bf-124">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="8e1bf-125">Analisadores</span><span class="sxs-lookup"><span data-stu-id="8e1bf-125">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="8e1bf-126">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-126">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="8e1bf-127">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="8e1bf-127">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="8e1bf-128">Como implementar o **cancelamento de registro**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-128">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="8e1bf-129">Implementando cancelamento de registro</span><span class="sxs-lookup"><span data-stu-id="8e1bf-129">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="8e1bf-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1bf-130">Requirements</span></span>



| <span data-ttu-id="8e1bf-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1bf-131">Requirement</span></span> | <span data-ttu-id="8e1bf-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8e1bf-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1bf-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e1bf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1bf-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8e1bf-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8e1bf-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e1bf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1bf-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8e1bf-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8e1bf-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e1bf-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e1bf-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1bf-138"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8e1bf-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e1bf-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e1bf-140"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e1bf-140"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8e1bf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8e1bf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e1bf-142"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1bf-142"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1bf-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e1bf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1bf-144">Cancelar registro</span><span class="sxs-lookup"><span data-stu-id="8e1bf-144">Deregister</span></span>](deregister.md)
</dt> </dl>

 

 




