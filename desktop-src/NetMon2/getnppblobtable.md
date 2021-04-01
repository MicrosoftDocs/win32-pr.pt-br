---
description: A função GetNPPBlobTable recupera uma tabela de BLOB NPP que representa as NICs de registro no computador local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Função GetNPPBlobTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828963"
---
# <a name="getnppblobtable-function"></a><span data-ttu-id="e0b13-103">Função GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="e0b13-103">GetNPPBlobTable function</span></span>

<span data-ttu-id="e0b13-104">A função **GetNPPBlobTable** recupera uma tabela de blob NPP que representa as NICs de registro no computador local.</span><span class="sxs-lookup"><span data-stu-id="e0b13-104">The **GetNPPBlobTable** function retrieves an NPP BLOB table that represents the register NICs on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b13-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0b13-105">Syntax</span></span>


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a><span data-ttu-id="e0b13-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0b13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b13-107">*hFilterBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0b13-107">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b13-108">Identificador para um BLOB de filtro que limita os BLOBs NPP retornados na tabela.</span><span class="sxs-lookup"><span data-stu-id="e0b13-108">Handle to a filter BLOB that limits the NPP BLOBs returned in the table.</span></span>

</dd> <dt>

<span data-ttu-id="e0b13-109">*ppBlobTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0b13-109">*ppBlobTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b13-110">Ponteiro para uma estrutura de [ \_ tabela de blob](blob-table.md) que contém pelo menos um ponteiro de BLOB.</span><span class="sxs-lookup"><span data-stu-id="e0b13-110">Pointer to a [BLOB\_TABLE](blob-table.md) structure that contains at least one BLOB pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b13-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0b13-111">Return value</span></span>

<span data-ttu-id="e0b13-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e0b13-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e0b13-113">Se a função não for bem-sucedida, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="e0b13-113">If the function is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e0b13-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0b13-114">Return code</span></span>                                                                                                | <span data-ttu-id="e0b13-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0b13-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0b13-116"><dt>**NMERR \_ não \_ NPP \_ dll**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b13-116"><dt>**NMERR\_NO\_NPP\_DLL**</dt></span></span> </dl>         | <span data-ttu-id="e0b13-117">Nenhuma dll foi encontrada no diretório NPP</span><span class="sxs-lookup"><span data-stu-id="e0b13-117">No DLLs were found in the NPP directory.</span></span><br/>                    |
| <dl> <span data-ttu-id="e0b13-118"><dt>**NMERR \_ não \_ há \_ DLLs NPP válidas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b13-118"><dt>**NMERR\_NO\_VALID\_NPP\_DLLS**</dt></span></span> </dl> | <span data-ttu-id="e0b13-119">Nenhuma das DLLs no diretório NPP era uma DLL NPP válida.</span><span class="sxs-lookup"><span data-stu-id="e0b13-119">None of the DLLs in the NPP directory were valid NPP DLLs.</span></span><br/>  |
| <dl> <span data-ttu-id="e0b13-120"><dt>**NMERR \_ nenhum \_ \_ NPPS correspondente**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b13-120"><dt>**NMERR\_NO\_MATCHING\_NPPS**</dt></span></span> </dl>   | <span data-ttu-id="e0b13-121">BLOBs NPP foram descobertos, mas nenhum passou no teste de filtro.</span><span class="sxs-lookup"><span data-stu-id="e0b13-121">NPP BLOBs were discovered, but none passed the filter test.</span></span><br/> |
| <dl> <span data-ttu-id="e0b13-122"><dt>**NMERR \_ fora \_ do \_ memorandor**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b13-122"><dt>**NMERR\_OUT\_OF\_MEMOR**</dt></span></span> </dl>       | <span data-ttu-id="e0b13-123">Monitor de Rede não pôde alocar memória.</span><span class="sxs-lookup"><span data-stu-id="e0b13-123">Network Monitor was not able to allocate memory.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="e0b13-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0b13-124">Remarks</span></span>

<span data-ttu-id="e0b13-125">O BLOB nomeado por *hFilterBlob* também pode ser um blob especial.</span><span class="sxs-lookup"><span data-stu-id="e0b13-125">The BLOB named by *hFilterBlob* can also be a special BLOB.</span></span>

<span data-ttu-id="e0b13-126">Se você definir o sinalizador no BLOB de filtro como **true**, a tabela de blob retornada também poderá incluir BLOBs especiais.</span><span class="sxs-lookup"><span data-stu-id="e0b13-126">If you set the flag in the filter BLOB to **TRUE**, the returned BLOB table can also include special BLOBs .</span></span>

<span data-ttu-id="e0b13-127">Se o BLOB nomeado por *hFilterBlob* for um blob especial, a interface do usuário do monitor de rede tentará processá-lo.</span><span class="sxs-lookup"><span data-stu-id="e0b13-127">If the BLOB named by *hFilterBlob* is a special BLOB, the Network Monitor UI will attempt to process it.</span></span> <span data-ttu-id="e0b13-128">Por exemplo, suponha que uma chamada anterior retorne um BLOB especial do NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="e0b13-128">For example, suppose that a previous call returns a special BLOB from the remote NPP.</span></span> <span data-ttu-id="e0b13-129">O aplicativo insere a marca necessária, nome do computador \_ .</span><span class="sxs-lookup"><span data-stu-id="e0b13-129">The application inserts the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="e0b13-130">Em seguida, o Finder passa esse BLOB para o NPP remoto, que retorna uma tabela dos BLOBs NPP associados ao nome do computador.</span><span class="sxs-lookup"><span data-stu-id="e0b13-130">The finder then passes this BLOB to the remote NPP, which then returns a table of the NPP BLOBs associated with the machine name.</span></span>

<span data-ttu-id="e0b13-131">Para destruir todos os BLOBs retornados e a tabela de BLOBs, o chamador é responsável por chamar a função **DestroyBlob** .</span><span class="sxs-lookup"><span data-stu-id="e0b13-131">To destroy all returned BLOBs and the BLOB table, the caller is responsible for calling the **DestroyBlob** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b13-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0b13-132">Requirements</span></span>



| <span data-ttu-id="e0b13-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b13-133">Requirement</span></span> | <span data-ttu-id="e0b13-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b13-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b13-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0b13-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b13-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0b13-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e0b13-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0b13-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b13-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0b13-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0b13-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0b13-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0b13-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b13-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e0b13-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0b13-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0b13-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0b13-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e0b13-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b13-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b13-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b13-144"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




