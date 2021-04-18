---
description: Define um único objeto de um filtro de exibição.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Estrutura FILTERobject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757359"
---
# <a name="filterobject-structure"></a><span data-ttu-id="7f2cb-103">Estrutura de FILTERobject</span><span class="sxs-lookup"><span data-stu-id="7f2cb-103">FILTEROBJECT structure</span></span>

<span data-ttu-id="7f2cb-104">A estrutura **filterobject** define um único objeto de um filtro de exibição.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-104">The **FILTEROBJECT** structure defines a single object of a display filter.</span></span> <span data-ttu-id="7f2cb-105">A função [**FilterAddObject**](filteraddobject.md) usa **filterobject** para criar um filtro de exibição.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-105">The [**FilterAddObject**](filteraddobject.md) function uses **FILTEROBJECT** to build a display filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2cb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f2cb-106">Syntax</span></span>


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a><span data-ttu-id="7f2cb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7f2cb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f2cb-108">**Ação**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-108">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-109">Sinalizador que especifica a ação de **filterobject** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-109">Flag that specifies the **FILTEROBJECT** action.</span></span> <span data-ttu-id="7f2cb-110">Um sinalizador pode especificar uma propriedade, um valor ou um operador.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-110">A flag can specify a property, value, or operator.</span></span>

<span data-ttu-id="7f2cb-111">A tabela a seguir lista os sinalizadores de propriedade de membro de ação.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-111">The following table lists Action member property flags.</span></span>



| <span data-ttu-id="7f2cb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7f2cb-112">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="7f2cb-113">Significado</span><span class="sxs-lookup"><span data-stu-id="7f2cb-113">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <span data-ttu-id="7f2cb-114"><dt>**Propriedade FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-114"><dt>**FILTERACTION\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="7f2cb-115">Contém esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-115">Contains this property.</span></span><br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <span data-ttu-id="7f2cb-116"><dt>**FILTERaction \_ PROPERTYEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-116"><dt>**FILTERACTION\_PROPERTYEXIST**</dt></span></span> </dl> | <span data-ttu-id="7f2cb-117">Indica que uma propriedade de ação de filtro já está definida.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-117">Indicates that a filter action property is already defined.</span></span><br/> |



 

<span data-ttu-id="7f2cb-118">A tabela a seguir lista os sinalizadores de valor de membro da ação.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-118">The following table lists Action member value flags.</span></span>



| <span data-ttu-id="7f2cb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7f2cb-119">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="7f2cb-120">Significado</span><span class="sxs-lookup"><span data-stu-id="7f2cb-120">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <span data-ttu-id="7f2cb-121"><dt>**valor de FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-121"><dt>**FILTERACTION\_VALUE**</dt></span></span> </dl>                 | <span data-ttu-id="7f2cb-122">Contém esse valor.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-122">Contains this value.</span></span><br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <span data-ttu-id="7f2cb-123"><dt>**Cadeia de \_ caracteres filteraction**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-123"><dt>**FILTERACTION\_STRING**</dt></span></span> </dl>              | <span data-ttu-id="7f2cb-124">Contém esta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-124">Contains this string.</span></span><br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <span data-ttu-id="7f2cb-125"><dt>**matriz FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-125"><dt>**FILTERACTION\_ARRAY**</dt></span></span> </dl>                 | <span data-ttu-id="7f2cb-126">Contém esta matriz.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-126">Contains this array.</span></span><br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <span data-ttu-id="7f2cb-127"><dt>**FILTERaction \_ CONTAINSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-127"><dt>**FILTERACTION\_CONTAINSNC**</dt></span></span> </dl>  | <span data-ttu-id="7f2cb-128">Indica que uma propriedade contém uma subcadeia de caracteres que não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-128">Indicates that a property contains a case-insensitive substring.</span></span><br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <span data-ttu-id="7f2cb-129"><dt>**FILTERaction \_ contém**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-129"><dt>**FILTERACTION\_CONTAINS**</dt></span></span> </dl>        | <span data-ttu-id="7f2cb-130">Indica que uma propriedade contém uma subcadeia de caracteres que diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-130">Indicates that a property contains a case sensitive substring.</span></span><br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <span data-ttu-id="7f2cb-131"><dt>**Endereço FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-131"><dt>**FILTERACTION\_ADDRESS**</dt></span></span> </dl>           | <span data-ttu-id="7f2cb-132">Contém o endereço MAC.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-132">Contains the MAC address.</span></span><br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <span data-ttu-id="7f2cb-133"><dt>**FILTERaction \_ ADDRESSANY**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-133"><dt>**FILTERACTION\_ADDRESSANY**</dt></span></span> </dl>  | <span data-ttu-id="7f2cb-134">Corresponde a qualquer endereço MAC.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-134">Matches any MAC address.</span></span><br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <span data-ttu-id="7f2cb-135"><dt>**FILTERaction \_ de**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-135"><dt>**FILTERACTION\_FROM**</dt></span></span> </dl>                    | <span data-ttu-id="7f2cb-136">Indica o endereço **Mac de** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-136">Indicates the **From MAC** address.</span></span><br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <span data-ttu-id="7f2cb-137"><dt>**FILTERaction \_ para**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-137"><dt>**FILTERACTION\_TO**</dt></span></span> </dl>                          | <span data-ttu-id="7f2cb-138">Indica o endereço **Mac a** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-138">Indicates the **To MAC** address.</span></span><br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <span data-ttu-id="7f2cb-139"><dt>**FILTERaction \_ deto**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-139"><dt>**FILTERACTION\_FROMTO**</dt></span></span> </dl>              | <span data-ttu-id="7f2cb-140">Indica um emparelhamento de **/para** de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-140">Indicates a **From/To** pairing of MAC addresses.</span></span><br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <span data-ttu-id="7f2cb-141"><dt>**FILTERaction \_ LARGEINT**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-141"><dt>**FILTERACTION\_LARGEINT**</dt></span></span> </dl>        | <span data-ttu-id="7f2cb-142">Contém um inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-142">Contains a large integer.</span></span><br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <span data-ttu-id="7f2cb-143"><dt>**tempo de FILTROaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-143"><dt>**FILTERACTION\_TIME**</dt></span></span> </dl>                    | <span data-ttu-id="7f2cb-144">Contém uma estrutura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-144">Contains a **SYSTEMTIME** structure.</span></span><br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <span data-ttu-id="7f2cb-145"><dt>**FILTERaction \_ addr \_ ether**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-145"><dt>**FILTERACTION\_ADDR\_ETHER**</dt></span></span> </dl> | <span data-ttu-id="7f2cb-146">Contém um endereço MAC Ethernet.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-146">Contains an Ethernet MAC address.</span></span><br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <span data-ttu-id="7f2cb-147"><dt>**TOKEN de endereço de FILTERaction \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-147"><dt>**FILTERACTION\_ADDR\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="7f2cb-148">Contém um endereço MAC de token ring.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-148">Contains a token ring MAC address.</span></span><br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <span data-ttu-id="7f2cb-149"><dt>**o \_ endaction addr \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-149"><dt>**FILTERACTION\_ADDR\_FDDI**</dt></span></span> </dl>    | <span data-ttu-id="7f2cb-150">Contém um endereço MAC FDDI.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-150">Contains a FDDI MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <span data-ttu-id="7f2cb-151"><dt>**FILTRAR \_ endereço \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-151"><dt>**FILTERACTION\_ADDR\_IPX**</dt></span></span> </dl>       | <span data-ttu-id="7f2cb-152">Contém um endereço MAC IPX.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-152">Contains an IPX MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <span data-ttu-id="7f2cb-153"><dt>**IP de endereço de FILTERaction \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-153"><dt>**FILTERACTION\_ADDR\_IP**</dt></span></span> </dl>          | <span data-ttu-id="7f2cb-154">Contém um endereço MAC IP.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-154">Contains an IP MAC address.</span></span><br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <span data-ttu-id="7f2cb-155"><dt>**OID FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-155"><dt>**FILTERACTION\_OID**</dt></span></span> </dl>                       | <span data-ttu-id="7f2cb-156">Contém um OID (identificador de objeto).</span><span class="sxs-lookup"><span data-stu-id="7f2cb-156">Contains an Object Identifier (OID).</span></span><br/>                             |



 

<span data-ttu-id="7f2cb-157">A tabela a seguir lista os sinalizadores de operador de membro de ação.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-157">The following table lists Action member operator flags.</span></span>



| <span data-ttu-id="7f2cb-158">Valor</span><span class="sxs-lookup"><span data-stu-id="7f2cb-158">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="7f2cb-159">Significado</span><span class="sxs-lookup"><span data-stu-id="7f2cb-159">Meaning</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <span data-ttu-id="7f2cb-160"><dt>**FILTERaction \_ inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-160"><dt>**FILTERACTION\_INVALID**</dt></span></span> </dl>                           | <span data-ttu-id="7f2cb-161">Indica uma ação de filtro inválida.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-161">Indicates an invalid filter action.</span></span><br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <span data-ttu-id="7f2cb-162"><dt>**FILTERaction \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-162"><dt>**FILTERACTION\_AND**</dt></span></span> </dl>                                       | <span data-ttu-id="7f2cb-163">Indica uma instrução **and** lógica.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-163">Indicates a logical **AND** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <span data-ttu-id="7f2cb-164"><dt>**FILTERaction \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-164"><dt>**FILTERACTION\_OR**</dt></span></span> </dl>                                          | <span data-ttu-id="7f2cb-165">Indica uma instrução **or** lógica.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-165">Indicates a logical **OR** statement.</span></span><br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <span data-ttu-id="7f2cb-166"><dt>**XOR FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-166"><dt>**FILTERACTION\_XOR**</dt></span></span> </dl>                                       | <span data-ttu-id="7f2cb-167">Indica uma instrução or exclusiva lógica **or** (XOR).</span><span class="sxs-lookup"><span data-stu-id="7f2cb-167">Indicates a logical exclusive **OR** (XOR) statement.</span></span><br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <span data-ttu-id="7f2cb-168"><dt>**FILTERaction \_ não**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-168"><dt>**FILTERACTION\_NOT**</dt></span></span> </dl>                                       | <span data-ttu-id="7f2cb-169">Indica uma instrução **not** lógica.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-169">Indicates a logical **NOT** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <span data-ttu-id="7f2cb-170"><dt>**FILTERaction \_ EQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-170"><dt>**FILTERACTION\_EQUALNC**</dt></span></span> </dl>                           | <span data-ttu-id="7f2cb-171">A ação do filtro é igual e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-171">Filter action is equal and case insensitive.</span></span><br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <span data-ttu-id="7f2cb-172"><dt>**FILTERaction \_ igual**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-172"><dt>**FILTERACTION\_EQUAL**</dt></span></span> </dl>                                 | <span data-ttu-id="7f2cb-173">A ação de filtro é igual e diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-173">Filter action is equal and case sensitive.</span></span><br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <span data-ttu-id="7f2cb-174"><dt>**FILTERaction \_ NOTEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-174"><dt>**FILTERACTION\_NOTEQUALNC**</dt></span></span> </dl>                  | <span data-ttu-id="7f2cb-175">A instrução not lógica é igual e **não** diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-175">Logical **NOT** statement is equal and case insensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <span data-ttu-id="7f2cb-176"><dt>**FILTERaction não \_ igual**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-176"><dt>**FILTERACTION\_NOTEQUAL**</dt></span></span> </dl>                        | <span data-ttu-id="7f2cb-177">A instrução **not** lógica é igual e diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-177">Logical **NOT** statement is equal and is case sensitive.</span></span><br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <span data-ttu-id="7f2cb-178"><dt>**FILTERaction \_ GREATERNC**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-178"><dt>**FILTERACTION\_GREATERNC**</dt></span></span> </dl>                     | <span data-ttu-id="7f2cb-179">A ação do filtro é maior que (>) e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-179">Filter action is greater than (>) and case insensitive.</span></span><br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <span data-ttu-id="7f2cb-180"><dt>**FILTERaction \_ maior**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-180"><dt>**FILTERACTION\_GREATER**</dt></span></span> </dl>                           | <span data-ttu-id="7f2cb-181">A ação do filtro é maior que (>) e diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-181">Filter action is greater than (>) and case sensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <span data-ttu-id="7f2cb-182"><dt>**FILTERaction \_ LESSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-182"><dt>**FILTERACTION\_LESSNC**</dt></span></span> </dl>                              | <span data-ttu-id="7f2cb-183">A ação de filtro é menor que (<) e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-183">Filter action is less than (<) and case insensitive.</span></span><br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <span data-ttu-id="7f2cb-184"><dt>**FILTERaction \_ menos**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-184"><dt>**FILTERACTION\_LESS**</dt></span></span> </dl>                                    | <span data-ttu-id="7f2cb-185">A ação de filtro é menor que (<) e diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-185">Filter action is less than (<) and case sensitive.</span></span><br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <span data-ttu-id="7f2cb-186"><dt>**FILTERaction \_ GREATEREQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-186"><dt>**FILTERACTION\_GREATEREQUALNC**</dt></span></span> </dl>      | <span data-ttu-id="7f2cb-187">A ação do filtro é maior ou igual a (>=) e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-187">Filter action is greater than or equal to (>=) and case insensitive.</span></span><br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <span data-ttu-id="7f2cb-188"><dt>**FILTERaction \_ GREATEREQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-188"><dt>**FILTERACTION\_GREATEREQUAL**</dt></span></span> </dl>            | <span data-ttu-id="7f2cb-189">A ação do filtro é maior ou igual a (>=) e diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-189">Filter action is greater than or equal to (>=) and case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <span data-ttu-id="7f2cb-190"><dt>**FILTERaction \_ LESSEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-190"><dt>**FILTERACTION\_LESSEQUALNC**</dt></span></span> </dl>               | <span data-ttu-id="7f2cb-191">A ação de filtro é menor ou igual a (<=) e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-191">Filter action is less than or equal to (<=) and case insensitive.</span></span><br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <span data-ttu-id="7f2cb-192"><dt>**FILTERaction \_ LESSEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-192"><dt>**FILTERACTION\_LESSEQUAL**</dt></span></span> </dl>                     | <span data-ttu-id="7f2cb-193">A ação de filtro é menor ou igual a (<=) e diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-193">Filter action is less than or equal to (<=) and is case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <span data-ttu-id="7f2cb-194"><dt>**FILTERaction \_ mais**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-194"><dt>**FILTERACTION\_PLUS**</dt></span></span> </dl>                                    | <span data-ttu-id="7f2cb-195">Adicionar operador (+).</span><span class="sxs-lookup"><span data-stu-id="7f2cb-195">Add operator (+).</span></span><br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <span data-ttu-id="7f2cb-196"><dt>**FILTERaction \_ menos**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-196"><dt>**FILTERACTION\_MINUS**</dt></span></span> </dl>                                 | <span data-ttu-id="7f2cb-197">Operador de subtração (-).</span><span class="sxs-lookup"><span data-stu-id="7f2cb-197">Subtract operator (-).</span></span><br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <span data-ttu-id="7f2cb-198"><dt>**FILTERaction \_ AREBITSON**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-198"><dt>**FILTERACTION\_AREBITSON**</dt></span></span> </dl>                     | <span data-ttu-id="7f2cb-199">Indica uma operação bit-a-bit.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-199">Indicates a bitwise operation.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <span data-ttu-id="7f2cb-200"><dt>**FILTERaction \_ AREBITSOFF**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-200"><dt>**FILTERACTION\_AREBITSOFF**</dt></span></span> </dl>                  | <span data-ttu-id="7f2cb-201">Indica uma operação sem bits</span><span class="sxs-lookup"><span data-stu-id="7f2cb-201">Indicates a non-bitwise operation.</span></span><br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <span data-ttu-id="7f2cb-202"><dt>**FILTERaction \_ PROTOCOLSEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-202"><dt>**FILTERACTION\_PROTOCOLSEXIST**</dt></span></span> </dl>      | <span data-ttu-id="7f2cb-203">Indica que os protocolos selecionados existem.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-203">Indicates that the selected protocols exist.</span></span><br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <span data-ttu-id="7f2cb-204"><dt>**FILTERaction \_ PROTOCOLEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-204"><dt>**FILTERACTION\_PROTOCOLEXIST**</dt></span></span> </dl>         | <span data-ttu-id="7f2cb-205">Indica que o protocolo selecionado existe.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-205">Indicates that the selected protocol exists.</span></span><br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <span data-ttu-id="7f2cb-206"><dt>**FILTERaction \_ ARRAYEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-206"><dt>**FILTERACTION\_ARRAYEQUAL**</dt></span></span> </dl>                  | <span data-ttu-id="7f2cb-207">Indica que o conteúdo da matriz é igual.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-207">Indicates that array contents are equal.</span></span> <span data-ttu-id="7f2cb-208">O sinalizador deve ser usado com uma estrutura de **\_ matriz filteraction** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-208">The flag must be used with a **FILTERACTION\_ARRAY** structure.</span></span><br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <span data-ttu-id="7f2cb-209"><dt>**FILTERaction \_ DEREFPROPERTY**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-209"><dt>**FILTERACTION\_DEREFPROPERTY**</dt></span></span> </dl>         | <span data-ttu-id="7f2cb-210">Descreve uma correspondência de padrão em um deslocamento (em bytes) do protocolo.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-210">Describes a pattern match at an offset (in bytes), from the protocol.</span></span><br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <span data-ttu-id="7f2cb-211"><dt>**\_OID filteraction \_ contém**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-211"><dt>**FILTERACTION\_OID\_CONTAINS**</dt></span></span> </dl>           | <span data-ttu-id="7f2cb-212">Avalia uma subcadeia de caracteres dentro de um identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-212">Evaluates a substring within an object identifier.</span></span> <span data-ttu-id="7f2cb-213">A ação deve ser usada com a estrutura **\_ OID de filteraction** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-213">The action must be used with the **FILTERACTION\_OID** structure.</span></span><br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <span data-ttu-id="7f2cb-214"><dt>**o OID FILTERaction \_ \_ começa \_ com**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-214"><dt>**FILTERACTION\_OID\_BEGINS\_WITH**</dt></span></span> </dl> | <span data-ttu-id="7f2cb-215">Avalia uma subcadeia de caracteres que inicia um identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-215">Evaluates a substring that begins an object identifier.</span></span> <span data-ttu-id="7f2cb-216">O sinalizador deve ser usado com **\_ OID filteraction**.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-216">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <span data-ttu-id="7f2cb-217"><dt>**\_OID de filteraction \_ termina \_ com**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-217"><dt>**FILTERACTION\_OID\_ENDS\_WITH**</dt></span></span> </dl>       | <span data-ttu-id="7f2cb-218">Avalia uma subcadeia de caracteres que termina um identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-218">Evaluates a substring that ends an object identifier.</span></span> <span data-ttu-id="7f2cb-219">O sinalizador deve ser usado com **\_ OID filteraction**.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-219">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <span data-ttu-id="7f2cb-220"><dt>**Endereço de filtro de \_ \_ Vines**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-220"><dt>**FILTERACTION\_ADDR\_VINES**</dt></span></span> </dl>                 | <span data-ttu-id="7f2cb-221">Contém um endereço MAC de Vines.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-221">Contains a Vines MAC address.</span></span><br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <span data-ttu-id="7f2cb-222"><dt>**expressão FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-222"><dt>**FILTERACTION\_EXPRESSION**</dt></span></span> </dl>                  | <span data-ttu-id="7f2cb-223">Contém uma expressão de ação.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-223">Contains an action expression.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <span data-ttu-id="7f2cb-224"><dt>**BOOL FILTERaction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-224"><dt>**FILTERACTION\_BOOL**</dt></span></span> </dl>                                    | <span data-ttu-id="7f2cb-225">Contém um tipo de dados **bool** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-225">Contains a **BOOL** data type.</span></span><br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <span data-ttu-id="7f2cb-226"><dt>**\_Avançar direção do filtro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-226"><dt>**FILTER\_DIRECTION\_NEXT**</dt></span></span> </dl>                       | <span data-ttu-id="7f2cb-227">Controla a direção sequencial (próximo quadro) em um arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-227">Controls sequential direction (Next frame) within a capture file.</span></span><br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <span data-ttu-id="7f2cb-228"><dt>**direção do filtro \_ \_ anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-228"><dt>**FILTER\_DIRECTION\_PREV**</dt></span></span> </dl>                       | <span data-ttu-id="7f2cb-229">Controla a direção sequencial (quadro anterior) em um arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-229">Controls sequential direction (Previous frame) within a capture file.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="7f2cb-230">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-230">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-231">Identificador para uma chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-231">Handle to a property key.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-232">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-232">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-233">Valor de um objeto.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-233">Value of an object.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-234">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-234">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-235">Identificador para exibir o protocolo de filtro.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-235">Handle to display filter protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-236">**lpArray**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-236">**lpArray**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-237">Ponteiro para uma matriz.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-237">Pointer to an array.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-238">**lpProtocolTable**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-238">**lpProtocolTable**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-239">Ponteiro para uma lista de protocolos projetada para testar a existência de protocolo em um quadro.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-239">Pointer to a protocol list designed to test the existence of protocol in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-240">**lpAddress**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-240">**lpAddress**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-241">Ponteiro para o endereço do tipo de kernel.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-241">Pointer to the kernel type address.</span></span> <span data-ttu-id="7f2cb-242">Por exemplo, MAC ou IP.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-242">For example, MAC or IP.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-243">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-243">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-244">**DWORD** duplo usado em um aplicativo do Windows NT ou do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-244">Double **DWORD** used in a Windows NT or Windows 2000 application.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-245">**lpTime**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-245">**lpTime**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-246">Um ponteiro para uma estrutura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="7f2cb-246">A pointer to a **SYSTEMTIME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-247">**lpOID**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-247">**lpOID**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-248">Um ponteiro para a estrutura de OID ( **\_ identificador de objeto** ).</span><span class="sxs-lookup"><span data-stu-id="7f2cb-248">A pointer to the **OBJECT\_IDENTIFIER** (OID) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-249">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-249">**ByteCount**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-250">O número, em bytes, no quadro.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-250">The number, in bytes, in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-251">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-251">**ByteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-252">O valor de byte de deslocamento da estrutura FILTERobject usada para comparar matrizes.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-252">The offset byte value of the FILTEROBJECT structure used to compare arrays.</span></span>

</dd> <dt>

<span data-ttu-id="7f2cb-253">**pNext**</span><span class="sxs-lookup"><span data-stu-id="7f2cb-253">**pNext**</span></span>
</dt> <dd>

<span data-ttu-id="7f2cb-254">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7f2cb-254">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f2cb-255">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f2cb-255">Requirements</span></span>



| <span data-ttu-id="7f2cb-256">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f2cb-256">Requirement</span></span> | <span data-ttu-id="7f2cb-257">Valor</span><span class="sxs-lookup"><span data-stu-id="7f2cb-257">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2cb-258">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f2cb-258">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2cb-259">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f2cb-259">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7f2cb-260">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f2cb-260">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2cb-261">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f2cb-261">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f2cb-262">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7f2cb-262">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f2cb-263"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f2cb-263"><dt>Netmon.h</dt></span></span> </dl> |



 

 




