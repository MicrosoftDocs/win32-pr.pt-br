---
description: A função PdhVbOpenQuery cria e Inicializa uma estrutura de consulta exclusiva que é usada para gerenciar a coleta de dados de desempenho.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Função PdhVbOpenQuery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091635"
---
# <a name="pdhvbopenquery-function"></a><span data-ttu-id="49d27-103">Função PdhVbOpenQuery</span><span class="sxs-lookup"><span data-stu-id="49d27-103">PdhVbOpenQuery function</span></span>

<span data-ttu-id="49d27-104">A função **PdhVbOpenQuery** cria e Inicializa uma estrutura de consulta exclusiva que é usada para gerenciar a coleta de dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="49d27-104">The **PdhVbOpenQuery** function creates and initializes a unique query structure that is used to manage the collection of performance data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49d27-105">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="49d27-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="49d27-106">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="49d27-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="49d27-107">Função PdhVbOpenQuery ( \_ ByVal QueryHandle as Long \_ ) enquanto longo</span><span class="sxs-lookup"><span data-stu-id="49d27-107">Function PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="49d27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49d27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d27-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="49d27-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="49d27-110">Variável que é limpa (igual a 0) antes que a função seja chamada e, se a função for bem-sucedida, conterá a ID exclusiva da consulta criada e aberta.</span><span class="sxs-lookup"><span data-stu-id="49d27-110">Variable that is cleared (equals 0) before the function is called and, if the function is successful, contains the unique ID of the query that is created and opened.</span></span> <span data-ttu-id="49d27-111">Esse identificador é usado nas chamadas subsequentes para outras funções de PDH para identificar a consulta.</span><span class="sxs-lookup"><span data-stu-id="49d27-111">This handle is used in the subsequent calls to other PDH functions to identify the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49d27-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49d27-112">Return value</span></span>

<span data-ttu-id="49d27-113">Se a função for bem-sucedida, ela retornará um inteiro **longo** igual a erro de \_ êxito e um novo identificador na variável *QueryHandle* .</span><span class="sxs-lookup"><span data-stu-id="49d27-113">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *QueryHandle* variable.</span></span>

<span data-ttu-id="49d27-114">Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="49d27-114">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="49d27-115">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="49d27-115">The following are possible values.</span></span>



| <span data-ttu-id="49d27-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="49d27-116">Return code</span></span>                                                                                                     | <span data-ttu-id="49d27-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="49d27-117">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="49d27-118"><dt>**\_argumento inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="49d27-118"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="49d27-119">O argumento é inválido ou está incorreto.</span><span class="sxs-lookup"><span data-stu-id="49d27-119">The argument is invalid or incorrect.</span></span><br/>             |
| <dl> <span data-ttu-id="49d27-120"><dt>**\_falha de \_ alocação de memória de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="49d27-120"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="49d27-121">Não foi possível alocar um buffer de memória temporário.</span><span class="sxs-lookup"><span data-stu-id="49d27-121">A temporary memory buffer could not be allocated.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="49d27-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49d27-122">Requirements</span></span>



| <span data-ttu-id="49d27-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="49d27-123">Requirement</span></span> | <span data-ttu-id="49d27-124">Valor</span><span class="sxs-lookup"><span data-stu-id="49d27-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="49d27-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49d27-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49d27-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49d27-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49d27-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49d27-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49d27-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49d27-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="49d27-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49d27-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="49d27-130"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49d27-130"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="49d27-131">DLL</span><span class="sxs-lookup"><span data-stu-id="49d27-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49d27-132"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49d27-132"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d27-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="49d27-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d27-134">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="49d27-134">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

