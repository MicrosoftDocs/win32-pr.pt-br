---
description: Esses tipos de dados podem ser usados para especificar o tipo de um valor de registro.
title: Tipos de dados do registro (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104990483"
---
# <a name="registry-data-types"></a><span data-ttu-id="f6612-103">Tipos de dados do registro</span><span class="sxs-lookup"><span data-stu-id="f6612-103">Registry Data Types</span></span>

<span data-ttu-id="f6612-104">Esses tipos de dados podem ser usados para especificar o tipo de um valor de registro.</span><span class="sxs-lookup"><span data-stu-id="f6612-104">These data types can be used to specify the type of a registry value.</span></span>



| <span data-ttu-id="f6612-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f6612-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="f6612-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6612-106">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <span data-ttu-id="f6612-107"><dt>**\_binário reg**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-107"><dt>**REG\_BINARY**</dt></span></span> </dl>                                          | <span data-ttu-id="f6612-108">Dados binários em qualquer formulário.</span><span class="sxs-lookup"><span data-stu-id="f6612-108">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <span data-ttu-id="f6612-109"><dt>**REG \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-109"><dt>**REG\_DWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="f6612-110">32-número de bits.</span><span class="sxs-lookup"><span data-stu-id="f6612-110">32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <span data-ttu-id="f6612-111"><dt>**REG \_ QWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-111"><dt>**REG\_QWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="f6612-112">64-número de bits.</span><span class="sxs-lookup"><span data-stu-id="f6612-112">64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <span data-ttu-id="f6612-113"><dt>**REG \_ DWORD de valor \_ pequeno \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-113"><dt>**REG\_DWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="f6612-114">32-número de bits no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="f6612-114">32-bit number in little-endian format.</span></span> <span data-ttu-id="f6612-115">Isso é equivalente a **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f6612-115">This is equivalent to **REG\_DWORD**.</span></span><br/> <span data-ttu-id="f6612-116">No formato little-endian, um valor multibyte é armazenado na memória do byte mais baixo (o "pequeno fim") para o byte mais alto.</span><span class="sxs-lookup"><span data-stu-id="f6612-116">In little-endian format, a multibyte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="f6612-117">Por exemplo, o valor 0x12345678 é armazenado como (0x78 0x56 0x34 0x12) no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="f6612-117">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span><br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <span data-ttu-id="f6612-118"><dt>**REG \_ QWORD \_ Little \_ ENDIAN**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-118"><dt>**REG\_QWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="f6612-119">Um número de 64 bits no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="f6612-119">A 64-bit number in little-endian format.</span></span> <span data-ttu-id="f6612-120">Isso é equivalente a **reg \_ QWORD**.</span><span class="sxs-lookup"><span data-stu-id="f6612-120">This is equivalent to **REG\_QWORD**.</span></span> <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <span data-ttu-id="f6612-121"><dt>**REG \_ DWORD \_ Big \_ ENDIAN**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-121"><dt>**REG\_DWORD\_BIG\_ENDIAN**</dt></span></span> </dl>          | <span data-ttu-id="f6612-122">32-número de bits no formato big-endian.</span><span class="sxs-lookup"><span data-stu-id="f6612-122">32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="f6612-123">No formato big endian, um valor multibyte é armazenado na memória do byte mais alto (o "Big end") para o byte mais baixo.</span><span class="sxs-lookup"><span data-stu-id="f6612-123">In big-endian format, a multibyte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="f6612-124">Por exemplo, o valor 0x12345678 é armazenado como (0x12 0x34 0x56 0x78) no formato big endian.</span><span class="sxs-lookup"><span data-stu-id="f6612-124">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span><br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <span data-ttu-id="f6612-125"><dt>**REG \_ expande \_ sz**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-125"><dt>**REG\_EXPAND\_SZ**</dt></span></span> </dl>                                | <span data-ttu-id="f6612-126">Cadeia de caracteres terminada em nulo que contém referências não expandidas a variáveis de ambiente (por exemplo, "% PATH%").</span><span class="sxs-lookup"><span data-stu-id="f6612-126">Null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="f6612-127">Será uma cadeia de caracteres Unicode ou ANSI, dependendo se você usar as funções Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="f6612-127">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <span data-ttu-id="f6612-128"><dt>**\_link reg**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-128"><dt>**REG\_LINK**</dt></span></span> </dl>                                                | <span data-ttu-id="f6612-129">Link simbólico Unicode.</span><span class="sxs-lookup"><span data-stu-id="f6612-129">Unicode symbolic link.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <span data-ttu-id="f6612-130"><dt>**REG \_ multi \_ sz**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-130"><dt>**REG\_MULTI\_SZ**</dt></span></span> </dl>                                   | <span data-ttu-id="f6612-131">Matriz de cadeias de caracteres terminadas em nulo que são terminadas por dois caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="f6612-131">Array of null-terminated strings that are terminated by two null characters.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <span data-ttu-id="f6612-132"><dt>**REG \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-132"><dt>**REG\_NONE**</dt></span></span> </dl>                                                | <span data-ttu-id="f6612-133">Nenhum tipo de valor definido.</span><span class="sxs-lookup"><span data-stu-id="f6612-133">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <span data-ttu-id="f6612-134"><dt>**\_lista de recursos do reg \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-134"><dt>**REG\_RESOURCE\_LIST**</dt></span></span> </dl>                    | <span data-ttu-id="f6612-135">Lista de recursos de driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6612-135">Device-driver resource list.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <span data-ttu-id="f6612-136"><dt>**REG \_ sz**</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-136"><dt>**REG\_SZ**</dt></span></span> </dl>                                                      | <span data-ttu-id="f6612-137">Cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f6612-137">Null-terminated string.</span></span> <span data-ttu-id="f6612-138">Será uma cadeia de caracteres Unicode ou ANSI, dependendo se você usar as funções Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="f6612-138">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="f6612-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6612-139">Requirements</span></span>



| <span data-ttu-id="f6612-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6612-140">Requirement</span></span> | <span data-ttu-id="f6612-141">Valor</span><span class="sxs-lookup"><span data-stu-id="f6612-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6612-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6612-142">Header</span></span><br/> | <dl> <span data-ttu-id="f6612-143"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6612-143"><dt>Winnt.h</dt></span></span> </dl> |



 

 




