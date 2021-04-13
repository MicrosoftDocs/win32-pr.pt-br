---
description: Recupera dados das entradas especificadas que pertencem a uma entrada EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: Função SdbQueryDataExTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370360"
---
# <a name="sdbquerydataextagid-function"></a><span data-ttu-id="0c098-103">Função SdbQueryDataExTagID</span><span class="sxs-lookup"><span data-stu-id="0c098-103">SdbQueryDataExTagID function</span></span>

<span data-ttu-id="0c098-104">Recupera dados das entradas especificadas que pertencem a uma entrada EXE.</span><span class="sxs-lookup"><span data-stu-id="0c098-104">Retrieves data from the specified entries belonging to an EXE entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c098-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c098-105">Syntax</span></span>


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a><span data-ttu-id="0c098-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c098-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0c098-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c098-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="0c098-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0c098-109">*tiExe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0c098-109">*tiExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c098-110">O [**TagId**](tagid.md) da entrada exe.</span><span class="sxs-lookup"><span data-stu-id="0c098-110">The [**TAGID**](tagid.md) of the EXE entry.</span></span>

</dd> <dt>

<span data-ttu-id="0c098-111">*lpszDataName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0c098-111">*lpszDataName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c098-112">O nome da entrada de dados a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="0c098-112">The name of the data entry to be retrieved.</span></span> <span data-ttu-id="0c098-113">Para especificar várias entradas, separe os nomes com o caractere de barra invertida (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="0c098-113">To specify multiple entries, separate the names with the backslash character ("\\").</span></span> <span data-ttu-id="0c098-114">Se esse parâmetro for **nulo**, a função tentará retornar todas as entradas de dados.</span><span class="sxs-lookup"><span data-stu-id="0c098-114">If this parameter is **NULL**, the function attempts to return all data entries.</span></span>

</dd> <dt>

<span data-ttu-id="0c098-115">*lpdwDataType* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0c098-115">*lpdwDataType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c098-116">O tipo de dados das entradas retornadas.</span><span class="sxs-lookup"><span data-stu-id="0c098-116">The data type of the returned entries.</span></span> <span data-ttu-id="0c098-117">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="0c098-117">This parameter can be one of the following values:</span></span>

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

<span data-ttu-id="0c098-118">**\_binário reg**</span><span class="sxs-lookup"><span data-stu-id="0c098-118">**REG\_BINARY**</span></span>
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

<span data-ttu-id="0c098-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0c098-119">**REG\_DWORD**</span></span>
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

<span data-ttu-id="0c098-120">**REG \_ multi \_ sz**</span><span class="sxs-lookup"><span data-stu-id="0c098-120">**REG\_MULTI\_SZ**</span></span>
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

<span data-ttu-id="0c098-121">**REG \_ None**</span><span class="sxs-lookup"><span data-stu-id="0c098-121">**REG\_NONE**</span></span>
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

<span data-ttu-id="0c098-122">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="0c098-122">**REG\_QWORD**</span></span>
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

<span data-ttu-id="0c098-123">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="0c098-123">**REG\_SZ**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0c098-124">*lpBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c098-124">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c098-125">O buffer que recebe os dados.</span><span class="sxs-lookup"><span data-stu-id="0c098-125">The buffer that receives the data.</span></span> <span data-ttu-id="0c098-126">Se o buffer não for grande o suficiente para conter os dados, a função falhará e retornará o **\_ \_ buffer insuficiente de erro**.</span><span class="sxs-lookup"><span data-stu-id="0c098-126">If buffer is not large enough to contain the data, the function fails and returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span>

</dd> <dt>

<span data-ttu-id="0c098-127">*lpcbBufferSize* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0c098-127">*lpcbBufferSize* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c098-128">O tamanho do buffer *lpBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="0c098-128">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0c098-129">*ptiData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c098-129">*ptiData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c098-130">O [**TagId**](tagid.md) da entrada de dados.</span><span class="sxs-lookup"><span data-stu-id="0c098-130">The [**TAGID**](tagid.md) of the data entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c098-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c098-131">Return value</span></span>

<span data-ttu-id="0c098-132">Essa função retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c098-132">This function returns one of the following values.</span></span>



| <span data-ttu-id="0c098-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0c098-133">Return code</span></span>                                                                                                    | <span data-ttu-id="0c098-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c098-134">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c098-135"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c098-135"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>       | <span data-ttu-id="0c098-136">Um ou mais parâmetros de entrada estão incorretos.</span><span class="sxs-lookup"><span data-stu-id="0c098-136">One or more input parameters is incorrect.</span></span><br/>                  |
| <dl> <span data-ttu-id="0c098-137"><dt>**ERRO \_ de \_ corrupção interna do BD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c098-137"><dt>**ERROR\_INTERNAL\_DB\_CORRUPTION**</dt></span></span> </dl> | <span data-ttu-id="0c098-138">Não foram encontradas entradas de dados para a entrada EXE.</span><span class="sxs-lookup"><span data-stu-id="0c098-138">No data entries were found for the EXE entry.</span></span><br/>               |
| <dl> <span data-ttu-id="0c098-139"><dt>**ERRO \_ de \_ buffer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="0c098-139"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>     | <span data-ttu-id="0c098-140">O buffer não é grande o suficiente para conter as entradas de dados.</span><span class="sxs-lookup"><span data-stu-id="0c098-140">The buffer is not large enough to contain the data entries.</span></span><br/> |
| <dl> <span data-ttu-id="0c098-141"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c098-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>      | <span data-ttu-id="0c098-142">Falha na alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="0c098-142">The memory allocation failed.</span></span><br/>                               |
| <dl> <span data-ttu-id="0c098-143"><dt>**ERRO \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="0c098-143"><dt>**ERROR\_NOT\_FOUND**</dt></span></span> </dl>               | <span data-ttu-id="0c098-144">Uma entrada de dados com o nome *lpszDataName* não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0c098-144">A data entry with the name *lpszDataName* was not found.</span></span><br/>    |
| <dl> <span data-ttu-id="0c098-145"><dt>**êxito do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c098-145"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>                  | <span data-ttu-id="0c098-146">A função foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="0c098-146">The function completed successfully.</span></span><br/>                        |



 

## <a name="requirements"></a><span data-ttu-id="0c098-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c098-147">Requirements</span></span>



| <span data-ttu-id="0c098-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c098-148">Requirement</span></span> | <span data-ttu-id="0c098-149">Valor</span><span class="sxs-lookup"><span data-stu-id="0c098-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c098-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c098-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0c098-151">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c098-151">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c098-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c098-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0c098-153">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c098-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0c098-154">DLL</span><span class="sxs-lookup"><span data-stu-id="0c098-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c098-155"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c098-155"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




