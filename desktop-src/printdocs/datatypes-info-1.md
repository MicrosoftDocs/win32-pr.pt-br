---
description: A estrutura informações de tipos de \_ \_ dados 1 contém informações sobre o tipo de dado usado para registrar um trabalho de impressão.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Estrutura de DATATYPES_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169469"
---
# <a name="datatypes_info_1-structure"></a><span data-ttu-id="754a9-103">Estrutura de informações de tipos de dados \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="754a9-103">DATATYPES\_INFO\_1 structure</span></span>

<span data-ttu-id="754a9-104">A estrutura informações de tipos de dados **\_ \_ 1** contém informações sobre o tipo de dado usado para registrar um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="754a9-104">The **DATATYPES\_INFO\_1** structure contains information about the data type used to record a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="754a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="754a9-105">Syntax</span></span>


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a><span data-ttu-id="754a9-106">Membros</span><span class="sxs-lookup"><span data-stu-id="754a9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="754a9-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="754a9-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="754a9-108">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o tipo de dados usado para gravar um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="754a9-108">Pointer to a null-terminated string that identifies the data type used to record a print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="754a9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="754a9-109">Requirements</span></span>



| <span data-ttu-id="754a9-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="754a9-110">Requirement</span></span> | <span data-ttu-id="754a9-111">Valor</span><span class="sxs-lookup"><span data-stu-id="754a9-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="754a9-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="754a9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="754a9-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="754a9-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="754a9-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="754a9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="754a9-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="754a9-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="754a9-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="754a9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="754a9-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="754a9-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="754a9-118">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="754a9-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="754a9-119">Informações de **\_ tipos \_ de \_ 1W** (Unicode) e **\_ informações de tipos de DataType \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="754a9-119">**\_DATATYPES\_INFO\_1W** (Unicode) and **\_DATATYPES\_INFO\_1A** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="754a9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="754a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="754a9-121">Impressão</span><span class="sxs-lookup"><span data-stu-id="754a9-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="754a9-122">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="754a9-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="754a9-123">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="754a9-123">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




