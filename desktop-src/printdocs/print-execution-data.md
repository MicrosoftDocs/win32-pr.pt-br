---
description: Contém o contexto de execução do driver de impressora que chama GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Estrutura de PRINT_EXECUTION_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170879"
---
# <a name="print_execution_data-structure"></a><span data-ttu-id="cda3b-103">Estrutura de dados de \_ execução de impressão \_</span><span class="sxs-lookup"><span data-stu-id="cda3b-103">PRINT\_EXECUTION\_DATA structure</span></span>

<span data-ttu-id="cda3b-104">Contém o contexto de execução do driver de impressora que chama [**GetPrintExecutionData**](getprintexecutiondata.md).</span><span class="sxs-lookup"><span data-stu-id="cda3b-104">Contains the execution context of the printer driver that calls [**GetPrintExecutionData**](getprintexecutiondata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cda3b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cda3b-105">Syntax</span></span>


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a><span data-ttu-id="cda3b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cda3b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cda3b-107">**contexto**</span><span class="sxs-lookup"><span data-stu-id="cda3b-107">**context**</span></span>
</dt> <dd>

<span data-ttu-id="cda3b-108">O valor do [**\_ \_ contexto de execução de impressão**](print-execution-context.md) que representa o contexto de execução atual do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="cda3b-108">The [**PRINT\_EXECUTION\_CONTEXT**](print-execution-context.md) value that represents the current execution context of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="cda3b-109">**clientAppPID**</span><span class="sxs-lookup"><span data-stu-id="cda3b-109">**clientAppPID**</span></span>
</dt> <dd>

<span data-ttu-id="cda3b-110">Se o valor do **contexto** for **o \_ contexto de execução de impressão \_ \_ WOW64**, **clientAppPID** identificará o aplicativo cliente em cujo nome o processo de splwow64.exe carregou o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="cda3b-110">If the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** identifies the client application on whose behalf the splwow64.exe process loaded the printer driver.</span></span> <span data-ttu-id="cda3b-111">Se o valor do **contexto** não for **o \_ contexto de execução de impressão \_ \_ WOW64**, **clientAppPID** será zero.</span><span class="sxs-lookup"><span data-stu-id="cda3b-111">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, **clientAppPID** is zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cda3b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cda3b-112">Requirements</span></span>



| <span data-ttu-id="cda3b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda3b-113">Requirement</span></span> | <span data-ttu-id="cda3b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cda3b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cda3b-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cda3b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cda3b-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cda3b-116">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="cda3b-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cda3b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cda3b-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="cda3b-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="cda3b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cda3b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda3b-120"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cda3b-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda3b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cda3b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda3b-122">**GetPrintExecutionData**</span><span class="sxs-lookup"><span data-stu-id="cda3b-122">**GetPrintExecutionData**</span></span>](getprintexecutiondata.md)
</dt> <dt>

[<span data-ttu-id="cda3b-123">**\_contexto de execução de impressão \_**</span><span class="sxs-lookup"><span data-stu-id="cda3b-123">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> </dl>

 

 




