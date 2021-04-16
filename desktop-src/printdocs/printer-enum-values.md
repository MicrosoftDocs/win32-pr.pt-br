---
description: A estrutura de valores de enumeração da impressora \_ \_ especifica o nome do valor, o tipo e os dados para um valor de configuração de impressora retornado pela função EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Estrutura de PRINTER_ENUM_VALUES (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772541"
---
# <a name="printer_enum_values-structure"></a><span data-ttu-id="9d0ce-103">Estrutura de valores de \_ enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="9d0ce-103">PRINTER\_ENUM\_VALUES structure</span></span>

<span data-ttu-id="9d0ce-104">A estrutura de **\_ \_ valores de enumeração da impressora** especifica o nome do valor, o tipo e os dados para um valor de configuração de impressora retornado pela função [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0ce-104">The **PRINTER\_ENUM\_VALUES** structure specifies the value name, type, and data for a printer configuration value returned by the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d0ce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d0ce-105">Syntax</span></span>


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a><span data-ttu-id="9d0ce-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9d0ce-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d0ce-107">**Valores principais**</span><span class="sxs-lookup"><span data-stu-id="9d0ce-107">**pValueName**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ce-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-108">Pointer to a null-terminated string that specifies the name of the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="9d0ce-109">**cbValueName**</span><span class="sxs-lookup"><span data-stu-id="9d0ce-109">**cbValueName**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ce-110">O número de bytes **no membro de valor de espaço** , incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-110">The number of bytes in the **pValueName** member, including the terminating NULL character.</span></span>

</dd> <dt>

<span data-ttu-id="9d0ce-111">**dwType**</span><span class="sxs-lookup"><span data-stu-id="9d0ce-111">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ce-112">Um código que indica o tipo de dados apontado pelo membro **pData** .</span><span class="sxs-lookup"><span data-stu-id="9d0ce-112">A code indicating the type of data pointed to by the **pData** member.</span></span> <span data-ttu-id="9d0ce-113">Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="9d0ce-113">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="9d0ce-114">**pData**</span><span class="sxs-lookup"><span data-stu-id="9d0ce-114">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ce-115">Ponteiro para um buffer que contém os dados para o valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="9d0ce-115">Pointer to a buffer containing the data for the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="9d0ce-116">**cbData**</span><span class="sxs-lookup"><span data-stu-id="9d0ce-116">**cbData**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ce-117">O número de bytes recuperados no buffer **pData** .</span><span class="sxs-lookup"><span data-stu-id="9d0ce-117">The number of bytes retrieved in the **pData** buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d0ce-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d0ce-118">Requirements</span></span>



| <span data-ttu-id="9d0ce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d0ce-119">Requirement</span></span> | <span data-ttu-id="9d0ce-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9d0ce-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0ce-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d0ce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d0ce-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d0ce-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9d0ce-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d0ce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d0ce-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d0ce-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d0ce-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9d0ce-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d0ce-126"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d0ce-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9d0ce-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9d0ce-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d0ce-128">**\_ \_ \_ VALUESW de enumeração de impressora** (Unicode) e **\_ \_ \_ valores de enum de impressora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9d0ce-128">**\_PRINTER\_ENUM\_VALUESW** (Unicode) and **\_PRINTER\_ENUM\_VALUESA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9d0ce-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d0ce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d0ce-130">Impressão</span><span class="sxs-lookup"><span data-stu-id="9d0ce-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9d0ce-131">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="9d0ce-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9d0ce-132">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="9d0ce-132">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> </dl>

 

