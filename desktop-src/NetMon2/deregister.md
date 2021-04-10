---
description: A função de exportação de cancelamento de registro libera os recursos usados para criar o banco de dados de propriedades de protocolo. A DLL do analisador deve implementar o cancelamento de registro.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Função de retorno de chamada de cancelamento de registro (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169377"
---
# <a name="deregister-callback-function"></a><span data-ttu-id="52262-104">Cancelar registro da função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="52262-104">Deregister callback function</span></span>

<span data-ttu-id="52262-105">A função de exportação de **cancelamento de registro** libera os recursos usados para criar o [*banco de dados de propriedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="52262-105">The **Deregister** export function frees the resources used to create the protocol [*property database*](p.md).</span></span> <span data-ttu-id="52262-106">A DLL do analisador deve implementar o **cancelamento de registro**.</span><span class="sxs-lookup"><span data-stu-id="52262-106">The parser DLL must implement **Deregister**.</span></span>

## <a name="syntax"></a><span data-ttu-id="52262-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52262-107">Syntax</span></span>


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="52262-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52262-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52262-109">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52262-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52262-110">Identificador do protocolo para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="52262-110">Handle of the protocol for a specific database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52262-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52262-111">Return value</span></span>

<span data-ttu-id="52262-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="52262-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="52262-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="52262-113">Remarks</span></span>

<span data-ttu-id="52262-114">Monitor de Rede chama o **cancelamento do registro** depois de passar todas as informações de captura para a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="52262-114">Network Monitor calls **Deregister** after passing all the capture information to the parser DLL.</span></span> <span data-ttu-id="52262-115">A DLL do analisador deve implementar uma função de **cancelamento de registro** para cada protocolo compatível com o analisador.</span><span class="sxs-lookup"><span data-stu-id="52262-115">The parser DLL must implement a **Deregister** function for each protocol that the parser supports.</span></span>

<span data-ttu-id="52262-116">Ao implementar o **cancelamento do registro**, a DLL do analisador deve chamar a função [DestroyPropertyDatabase](destroypropertydatabase.md) para liberar os recursos do banco de [*dados de propriedade*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="52262-116">When implementing **Deregister**, the parser DLL must call the [DestroyPropertyDatabase](destroypropertydatabase.md) function to release the [*property database*](p.md) resources.</span></span>



| <span data-ttu-id="52262-117">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="52262-117">For information on</span></span>                                        | <span data-ttu-id="52262-118">Consulte</span><span class="sxs-lookup"><span data-stu-id="52262-118">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="52262-119">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="52262-119">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="52262-120">Analisadores</span><span class="sxs-lookup"><span data-stu-id="52262-120">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="52262-121">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="52262-121">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="52262-122">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="52262-122">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="52262-123">Como implementar o **cancelamento de registro**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="52262-123">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="52262-124">Implementando cancelamento de registro</span><span class="sxs-lookup"><span data-stu-id="52262-124">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="52262-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52262-125">Requirements</span></span>



| <span data-ttu-id="52262-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="52262-126">Requirement</span></span> | <span data-ttu-id="52262-127">Valor</span><span class="sxs-lookup"><span data-stu-id="52262-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52262-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52262-128">Minimum supported client</span></span><br/> | <span data-ttu-id="52262-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52262-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="52262-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52262-130">Minimum supported server</span></span><br/> | <span data-ttu-id="52262-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52262-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52262-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52262-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="52262-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="52262-133"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52262-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="52262-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52262-135">DestroyPropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="52262-135">DestroyPropertyDatabase</span></span>](destroypropertydatabase.md)
</dt> </dl>

 

 




