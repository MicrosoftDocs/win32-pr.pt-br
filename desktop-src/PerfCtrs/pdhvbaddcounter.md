---
description: A função PdhVbAddCounter cria uma entrada de contador no objeto de consulta especificado e retorna um identificador para esse contador após a conclusão bem-sucedida.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: Função PdhVbAddCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754614"
---
# <a name="pdhvbaddcounter-function"></a><span data-ttu-id="0a284-103">Função PdhVbAddCounter</span><span class="sxs-lookup"><span data-stu-id="0a284-103">PdhVbAddCounter function</span></span>

<span data-ttu-id="0a284-104">A função **PdhVbAddCounter** cria uma entrada de contador no objeto de consulta especificado e retorna um identificador para esse contador após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0a284-104">The **PdhVbAddCounter** function creates a counter entry in the specified query object, and returns a handle to that counter upon successful completion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a284-105">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="0a284-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="0a284-106">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0a284-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="0a284-107">Função PdhVbAddCounter ( \_ ByVal QueryHandle as Long, \_ ByVal Compath como String, \_ ByVal lide como Long \_ ) enquanto longo</span><span class="sxs-lookup"><span data-stu-id="0a284-107">Function PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="0a284-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a284-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a284-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="0a284-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="0a284-110">ID da consulta à qual este contador deve ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="0a284-110">ID of the query to which this counter is to be assigned.</span></span> <span data-ttu-id="0a284-111">Esse valor é retornado pela função [**PdhVbOpenQuery**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="0a284-111">This value is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0a284-112">*CounterPath*</span><span class="sxs-lookup"><span data-stu-id="0a284-112">*CounterPath*</span></span> 
</dt> <dd>

<span data-ttu-id="0a284-113">Cadeia de texto que especifica o nome do caminho do contador a ser adicionado à consulta.</span><span class="sxs-lookup"><span data-stu-id="0a284-113">Text string that specifies the name of the counter path to add to the query.</span></span> <span data-ttu-id="0a284-114">O conteúdo dessa cadeia de caracteres deve ser um caminho de contador válido, conforme obtido no navegador do contador ou outra fonte.</span><span class="sxs-lookup"><span data-stu-id="0a284-114">The contents of this string must be a valid counter path, as obtained from the counter browser or other source.</span></span>

</dd> <dt>

<span data-ttu-id="0a284-115">*Manipulador*</span><span class="sxs-lookup"><span data-stu-id="0a284-115">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="0a284-116">Referência exclusiva que identifica esse contador na consulta.</span><span class="sxs-lookup"><span data-stu-id="0a284-116">Unique reference that identifies this counter in the query.</span></span> <span data-ttu-id="0a284-117">Essa variável deve ser inicializada para zero antes de a função ser chamada.</span><span class="sxs-lookup"><span data-stu-id="0a284-117">This variable must be initialized to zero before the function is called.</span></span> <span data-ttu-id="0a284-118">Ele contém um valor válido em retornar somente se a função for concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="0a284-118">It contains a valid value on return only if the function completes successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a284-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a284-119">Return value</span></span>

<span data-ttu-id="0a284-120">Se a função for bem-sucedida, ela retornará um inteiro **longo** igual a erro de \_ êxito e um novo identificador na variável de *manipulador* .</span><span class="sxs-lookup"><span data-stu-id="0a284-120">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *CounterHandle* variable.</span></span>

<span data-ttu-id="0a284-121">Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0a284-121">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="0a284-122">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="0a284-122">The following are possible values.</span></span>



| <span data-ttu-id="0a284-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0a284-123">Return code</span></span>                                                                                                     | <span data-ttu-id="0a284-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a284-124">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a284-125"><dt>**\_argumento inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="0a284-126">Um ou mais argumentos são inválidos ou incorretos.</span><span class="sxs-lookup"><span data-stu-id="0a284-126">One or more of the arguments is invalid or incorrect.</span></span><br/>              |
| <dl> <span data-ttu-id="0a284-127"><dt>**\_falha de \_ alocação de memória de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-127"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="0a284-128">Não foi possível alocar um buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="0a284-128">A memory buffer could not be allocated.</span></span><br/>                            |
| <dl> <span data-ttu-id="0a284-129"><dt>**\_identificador inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-129"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>             | <span data-ttu-id="0a284-130">O identificador de consulta não é válido.</span><span class="sxs-lookup"><span data-stu-id="0a284-130">The query handle is not valid.</span></span><br/>                                     |
| <dl> <span data-ttu-id="0a284-131"><dt>**\_CSTATUS PDH \_ sem \_ contador**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-131"><dt>**PDH\_CSTATUS\_NO\_COUNTER**</dt></span></span> </dl>        | <span data-ttu-id="0a284-132">O contador especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="0a284-132">The specified counter was not found.</span></span><br/>                               |
| <dl> <span data-ttu-id="0a284-133"><dt>**PDH \_ CSTATUS \_ nenhum \_ objeto**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-133"><dt>**PDH\_CSTATUS\_NO\_OBJECT**</dt></span></span> </dl>         | <span data-ttu-id="0a284-134">O objeto especificado não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="0a284-134">The specified object could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="0a284-135"><dt>**PDH \_ CSTATUS \_ nenhum \_ computador**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-135"><dt>**PDH\_CSTATUS\_NO\_MACHINE**</dt></span></span> </dl>        | <span data-ttu-id="0a284-136">Não foi possível criar uma entrada de computador.</span><span class="sxs-lookup"><span data-stu-id="0a284-136">A computer entry could not be created.</span></span><br/>                             |
| <dl> <span data-ttu-id="0a284-137"><dt>**CSTATUS de PDH \_ \_ inválido \_ COUNTERNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-137"><dt>**PDH\_CSTATUS\_BAD\_COUNTERNAME**</dt></span></span> </dl>   | <span data-ttu-id="0a284-138">Uma cadeia de caracteres de caminho de nome de contador vazio foi passada.</span><span class="sxs-lookup"><span data-stu-id="0a284-138">An empty counter name path string was passed in.</span></span><br/>                   |
| <dl> <span data-ttu-id="0a284-139"><dt>**\_função PDH \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-139"><dt>**PDH\_FUNCTION\_NOT\_FOUND**</dt></span></span> </dl>        | <span data-ttu-id="0a284-140">Não foi possível determinar a função de cálculo deste contador.</span><span class="sxs-lookup"><span data-stu-id="0a284-140">The calculation function for this counter could not be determined.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0a284-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a284-141">Requirements</span></span>



| <span data-ttu-id="0a284-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a284-142">Requirement</span></span> | <span data-ttu-id="0a284-143">Valor</span><span class="sxs-lookup"><span data-stu-id="0a284-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a284-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a284-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0a284-145">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0a284-145">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a284-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a284-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0a284-147">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a284-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0a284-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a284-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a284-149"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-149"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a284-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0a284-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a284-151"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a284-151"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a284-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a284-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a284-153">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="0a284-153">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
</dt> </dl>

 

