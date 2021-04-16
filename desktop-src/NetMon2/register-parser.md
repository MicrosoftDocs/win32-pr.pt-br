---
description: A função de exportação de registro deve ser implementada em todas as DLLs do analisador. A implementação do registro cria e preenche um banco de dados de propriedade para um protocolo. Monitor de Rede usa o banco de dados para determinar a quais propriedades o protocolo dá suporte.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Registrar função de retorno de chamada do analisador (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758588"
---
# <a name="register-parser-callback-function"></a><span data-ttu-id="6940a-105">Registrar função de retorno de chamada do analisador</span><span class="sxs-lookup"><span data-stu-id="6940a-105">Register Parser callback function</span></span>

<span data-ttu-id="6940a-106">A função de exportação de **registro** deve ser implementada em todas as DLLs do analisador.</span><span class="sxs-lookup"><span data-stu-id="6940a-106">The **Register** export function must be implemented in all parser DLLs.</span></span> <span data-ttu-id="6940a-107">A implementação do **registro** cria e preenche um banco de [*dados de propriedade*](p.md) para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="6940a-107">The implementation of **Register** creates and fills-in a [*property database*](p.md) for a protocol.</span></span> <span data-ttu-id="6940a-108">Monitor de Rede usa o banco de dados para determinar a quais propriedades o protocolo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="6940a-108">Network Monitor uses the database to determine which properties the protocol supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="6940a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6940a-109">Syntax</span></span>


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="6940a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6940a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6940a-111">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6940a-111">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6940a-112">O identificador do protocolo que o Monitor de Rede fornece ao chamar **o registro**.</span><span class="sxs-lookup"><span data-stu-id="6940a-112">The handle of the protocol that Network Monitor provides when calling **Register**.</span></span> <span data-ttu-id="6940a-113">O identificador *hProtocol* é necessário ao chamar funções auxiliares de exportação.</span><span class="sxs-lookup"><span data-stu-id="6940a-113">The *hProtocol* handle is needed when calling export helper functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6940a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6940a-114">Return value</span></span>

<span data-ttu-id="6940a-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6940a-115">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6940a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6940a-116">Remarks</span></span>

<span data-ttu-id="6940a-117">Monitor de Rede começa a chamar a função de **registro** assim que uma captura é carregada.</span><span class="sxs-lookup"><span data-stu-id="6940a-117">Network Monitor starts calling the **Register** function as soon as a capture is loaded.</span></span> <span data-ttu-id="6940a-118">Monitor de Rede chama a função de **registro** para cada protocolo que pode identificar.</span><span class="sxs-lookup"><span data-stu-id="6940a-118">Network Monitor calls the **Register** function for each protocol it can identify.</span></span> <span data-ttu-id="6940a-119">A função [createprotocol](createprotocol.md) passa um ponteiro para a função **Register** .</span><span class="sxs-lookup"><span data-stu-id="6940a-119">The [CreateProtocol](createprotocol.md) function passes a pointer to the **Register** function.</span></span>

<span data-ttu-id="6940a-120">A implementação do **registro** inclui chamadas para as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6940a-120">The implementation of **Register** includes calls to the following functions.</span></span>

-   <span data-ttu-id="6940a-121">Uma chamada para as funções [CreatePropertyDatabase](createpropertydatabase.md) e [AddProperty](/previous-versions/bb251873(v=msdn.10)) para criar um banco de dados de todas as propriedades às quais o protocolo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="6940a-121">A call to the [CreatePropertyDatabase](createpropertydatabase.md) and [AddProperty](/previous-versions/bb251873(v=msdn.10)) functions to create a database of all the properties that the protocol supports.</span></span>
-   <span data-ttu-id="6940a-122">Uma chamada para a função [Createentregatable](createhandofftable.md) será necessária se o protocolo usar um [*conjunto de entrega*](h.md).</span><span class="sxs-lookup"><span data-stu-id="6940a-122">A call to the [CreateHandoffTable](createhandofftable.md) function is required if the protocol uses a [*handoff set*](h.md).</span></span>

<span data-ttu-id="6940a-123">Se a DLL do analisador contiver vários analisadores e o analisador puder detectar mais de um protocolo, você deverá implementar uma função de **registro** para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="6940a-123">If the parser DLL contains multiple parsers, and the parser can detect more than one protocol, you must implement a **Register** function for each protocol.</span></span>



| <span data-ttu-id="6940a-124">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="6940a-124">For Information on</span></span>                                        | <span data-ttu-id="6940a-125">Consulte</span><span class="sxs-lookup"><span data-stu-id="6940a-125">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6940a-126">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="6940a-126">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="6940a-127">Analisadores</span><span class="sxs-lookup"><span data-stu-id="6940a-127">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="6940a-128">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="6940a-128">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="6940a-129">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="6940a-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="6940a-130">Como implementar **o registro**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="6940a-130">How to implement **Register**  includes an example.</span></span>       | [<span data-ttu-id="6940a-131">Implementando o registro</span><span class="sxs-lookup"><span data-stu-id="6940a-131">Implementing Register</span></span>](implementing-register.md)     |



 

## <a name="requirements"></a><span data-ttu-id="6940a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6940a-132">Requirements</span></span>



| <span data-ttu-id="6940a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6940a-133">Requirement</span></span> | <span data-ttu-id="6940a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6940a-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6940a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6940a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6940a-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6940a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6940a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6940a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6940a-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6940a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6940a-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6940a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6940a-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6940a-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6940a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="6940a-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="6940a-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6940a-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="6940a-143">Createentregatable</span><span class="sxs-lookup"><span data-stu-id="6940a-143">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> <dt>

[<span data-ttu-id="6940a-144">CreatePropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="6940a-144">CreatePropertyDatabase</span></span>](createpropertydatabase.md)
</dt> <dt>

[<span data-ttu-id="6940a-145">Createprotocol</span><span class="sxs-lookup"><span data-stu-id="6940a-145">CreateProtocol</span></span>](createprotocol.md)
</dt> </dl>

 

