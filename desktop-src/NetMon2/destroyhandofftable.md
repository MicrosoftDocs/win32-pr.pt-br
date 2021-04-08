---
description: A função DestroyHandoffTable destrói uma tabela de entrega criada com createentregatable.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Função DestroyHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921629"
---
# <a name="destroyhandofftable-function"></a><span data-ttu-id="49242-103">Função DestroyHandoffTable</span><span class="sxs-lookup"><span data-stu-id="49242-103">DestroyHandoffTable function</span></span>

<span data-ttu-id="49242-104">A função **DestroyHandoffTable** destrói uma tabela de entrega criada com **createentregatable**.</span><span class="sxs-lookup"><span data-stu-id="49242-104">The **DestroyHandoffTable** function destroys a handoff table created with **CreateHandoffTable**.</span></span>

## <a name="syntax"></a><span data-ttu-id="49242-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49242-105">Syntax</span></span>


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a><span data-ttu-id="49242-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49242-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49242-107">*hTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49242-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49242-108">Identificador para a tabela de entrega destruída.</span><span class="sxs-lookup"><span data-stu-id="49242-108">Handle to the destroyed handoff table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49242-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49242-109">Return value</span></span>

<span data-ttu-id="49242-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="49242-110">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="49242-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49242-111">Requirements</span></span>



| <span data-ttu-id="49242-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="49242-112">Requirement</span></span> | <span data-ttu-id="49242-113">Valor</span><span class="sxs-lookup"><span data-stu-id="49242-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49242-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49242-114">Minimum supported client</span></span><br/> | <span data-ttu-id="49242-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49242-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="49242-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49242-116">Minimum supported server</span></span><br/> | <span data-ttu-id="49242-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49242-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="49242-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49242-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="49242-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="49242-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="49242-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49242-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="49242-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49242-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="49242-122">DLL</span><span class="sxs-lookup"><span data-stu-id="49242-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49242-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49242-123"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




