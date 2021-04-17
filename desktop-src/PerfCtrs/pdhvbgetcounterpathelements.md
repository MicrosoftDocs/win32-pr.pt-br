---
description: A função PdhVbGetCounterPathElements analisa uma cadeia de caracteres de caminho de contador de desempenho totalmente qualificado em seus elementos individuais.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: Função PdhVbGetCounterPathElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780488"
---
# <a name="pdhvbgetcounterpathelements-function"></a><span data-ttu-id="a1fb8-103">Função PdhVbGetCounterPathElements</span><span class="sxs-lookup"><span data-stu-id="a1fb8-103">PdhVbGetCounterPathElements function</span></span>

<span data-ttu-id="a1fb8-104">A função **PdhVbGetCounterPathElements** analisa uma cadeia de caracteres de caminho de contador de desempenho totalmente qualificado em seus elementos individuais.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-104">The **PdhVbGetCounterPathElements** function parses a fully qualified performance counter path string into its individual elements.</span></span> <span data-ttu-id="a1fb8-105">Cada uma das variáveis de cadeia de caracteres deve ter o mesmo tamanho (*BufferSize*) e dimensionada e inicializada antes de ser usada nessa função.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-105">Each of the string variables must be the same size (*BufferSize*) and dimensioned and initialized before it is used in this function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1fb8-106">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-106">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="a1fb8-107">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a1fb8-107">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="a1fb8-108">Função PdhVbGetCounterPathElements ( \_ ByVal pathstring como String, \_ ByVal MachineName as String, \_ ByVal ObjectName as String, \_ ByVal InstanceName as String, \_ ByVal ParentInstance as String, \_ ByVal CounterName as String, \_ ByVal BufferSize as Long \_ ) como Long</span><span class="sxs-lookup"><span data-stu-id="a1fb8-108">Function PdhVbGetCounterPathElements( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="a1fb8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1fb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1fb8-110">*Caminho da*</span><span class="sxs-lookup"><span data-stu-id="a1fb8-110">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fb8-111">Cadeia de caracteres de caminho do contador que deve ser dividida em seus elementos individuais.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-111">Counter path string that is to be broken up into its individual elements.</span></span>

</dd> <dt>

<span data-ttu-id="a1fb8-112">*MachineName*</span><span class="sxs-lookup"><span data-stu-id="a1fb8-112">*MachineName*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fb8-113">Cadeia de caracteres para receber o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-113">String to receive the computer name.</span></span>

</dd> <dt>

<span data-ttu-id="a1fb8-114">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="a1fb8-114">*ObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fb8-115">Cadeia de caracteres para receber o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-115">String to receive the object name.</span></span>

</dd> <dt>

<span data-ttu-id="a1fb8-116">*InstanceName*</span><span class="sxs-lookup"><span data-stu-id="a1fb8-116">*InstanceName*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fb8-117">Cadeia de caracteres para receber o nome da instância, se usado.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-117">String to receive the instance name, if used.</span></span>

</dd> <dt>

<span data-ttu-id="a1fb8-118">*ParentInstance*</span><span class="sxs-lookup"><span data-stu-id="a1fb8-118">*ParentInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fb8-119">Cadeia de caracteres para receber a instância pai, se usada.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-119">String to receive the parent instance, if used.</span></span>

</dd> <dt>

<span data-ttu-id="a1fb8-120">*CounterName*</span><span class="sxs-lookup"><span data-stu-id="a1fb8-120">*CounterName*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fb8-121">Cadeia de caracteres para receber o nome do contador.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-121">String to receive the counter name.</span></span>

</dd> <dt>

<span data-ttu-id="a1fb8-122">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="a1fb8-122">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a1fb8-123">Tamanho máximo de cada variável de cadeia de caracteres usada como parâmetro para esta chamada de função.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-123">Maximum size of each string variable used as a parameter to this function call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1fb8-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1fb8-124">Return value</span></span>

<span data-ttu-id="a1fb8-125">Se a função for bem-sucedida, ela retornará um inteiro **longo** igual a erro de \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-125">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a1fb8-126">Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a1fb8-126">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="a1fb8-127">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-127">The following are possible values.</span></span>



| <span data-ttu-id="a1fb8-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a1fb8-128">Return code</span></span>                                                                                                     | <span data-ttu-id="a1fb8-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1fb8-129">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1fb8-130"><dt>**\_argumento inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1fb8-130"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="a1fb8-131">Um ou mais dos buffers de cadeia de caracteres não tem o tamanho correto.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-131">One or more of the string buffers is not the correct size.</span></span><br/>                          |
| <dl> <span data-ttu-id="a1fb8-132"><dt>**\_mais \_ dados da PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="a1fb8-132"><dt>**PDH\_MORE\_DATA**</dt></span></span> </dl>                  | <span data-ttu-id="a1fb8-133">Um ou mais dos elementos do caminho do contador é muito grande para o comprimento do buffer de retorno.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-133">One or more of the counter path elements is too large for the return buffer length.</span></span><br/> |
| <dl> <span data-ttu-id="a1fb8-134"><dt>**\_falha de \_ alocação de memória de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1fb8-134"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="a1fb8-135">Não foi possível alocar um buffer de memória temporário.</span><span class="sxs-lookup"><span data-stu-id="a1fb8-135">A temporary memory buffer could not be allocated.</span></span><br/>                                   |



 

## <a name="requirements"></a><span data-ttu-id="a1fb8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1fb8-136">Requirements</span></span>



| <span data-ttu-id="a1fb8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1fb8-137">Requirement</span></span> | <span data-ttu-id="a1fb8-138">Valor</span><span class="sxs-lookup"><span data-stu-id="a1fb8-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1fb8-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1fb8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a1fb8-140">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a1fb8-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1fb8-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1fb8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a1fb8-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1fb8-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1fb8-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1fb8-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1fb8-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1fb8-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="a1fb8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a1fb8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1fb8-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1fb8-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1fb8-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1fb8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1fb8-148">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="a1fb8-148">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="a1fb8-149">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="a1fb8-149">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="a1fb8-150">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="a1fb8-150">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

