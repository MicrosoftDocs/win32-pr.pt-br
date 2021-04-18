---
description: A estrutura de HANDOFFENTRY de PF \_ define um protocolo que monitor de rede adiciona ao conjunto de entrega de um analisador.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Estrutura de PF_HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758589"
---
# <a name="pf_handoffentry-structure"></a><span data-ttu-id="7f454-103">Estrutura de HANDOFFENTRY de PF \_</span><span class="sxs-lookup"><span data-stu-id="7f454-103">PF\_HANDOFFENTRY structure</span></span>

<span data-ttu-id="7f454-104">A estrutura de **\_ HANDOFFENTRY de PF** define um protocolo que monitor de rede adiciona ao conjunto de entrega de um analisador.</span><span class="sxs-lookup"><span data-stu-id="7f454-104">The **PF\_HANDOFFENTRY** structure defines a protocol that Network Monitor adds to the handoff set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f454-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f454-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="7f454-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7f454-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f454-107">**szIniFile**</span><span class="sxs-lookup"><span data-stu-id="7f454-107">**szIniFile**</span></span>
</dt> <dd>

<span data-ttu-id="7f454-108">Nome do arquivo INI associado ao protocolo.</span><span class="sxs-lookup"><span data-stu-id="7f454-108">Name of the INI file associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7f454-109">**szIniSection**</span><span class="sxs-lookup"><span data-stu-id="7f454-109">**szIniSection**</span></span>
</dt> <dd>

<span data-ttu-id="7f454-110">Rótulo de seção dentro do arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="7f454-110">Section label within the INI file.</span></span>

</dd> <dt>

<span data-ttu-id="7f454-111">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="7f454-111">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="7f454-112">Nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="7f454-112">Name of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7f454-113">**dwHandOffValue**</span><span class="sxs-lookup"><span data-stu-id="7f454-113">**dwHandOffValue**</span></span>
</dt> <dd>

<span data-ttu-id="7f454-114">Valor associado ao protocolo.</span><span class="sxs-lookup"><span data-stu-id="7f454-114">Value associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7f454-115">**ValueFormatBase**</span><span class="sxs-lookup"><span data-stu-id="7f454-115">**ValueFormatBase**</span></span>
</dt> <dd>

<span data-ttu-id="7f454-116">A base numérica do valor do protocolo que é especificado em **dwHandOffValue**.</span><span class="sxs-lookup"><span data-stu-id="7f454-116">Numeric base of the protocol value that is specified in **dwHandOffValue**.</span></span> <span data-ttu-id="7f454-117">A função **ValueFormatBase** deve ser definida como uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7f454-117">The **ValueFormatBase** function must be set to one of the following:</span></span>



| <span data-ttu-id="7f454-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7f454-118">Value</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="7f454-119">Significado</span><span class="sxs-lookup"><span data-stu-id="7f454-119">Meaning</span></span>                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <span data-ttu-id="7f454-120"><dt>**BASE do formato do valor de entrega \_ \_ \_ \_ desconhecida**</dt></span><span class="sxs-lookup"><span data-stu-id="7f454-120"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="7f454-121">Base desconhecida</span><span class="sxs-lookup"><span data-stu-id="7f454-121">Unknown base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <span data-ttu-id="7f454-122"><dt>**\_ \_ decimal base de formato de valor de \_ entrega \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f454-122"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_DECIMAL**</dt></span></span> </dl> | <span data-ttu-id="7f454-123">Base decimal</span><span class="sxs-lookup"><span data-stu-id="7f454-123">Decimal base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <span data-ttu-id="7f454-124"><dt>**formato de valor de entrega \_ \_ \_ \_ hex base**</dt></span><span class="sxs-lookup"><span data-stu-id="7f454-124"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_HEX**</dt></span></span> </dl>             | <span data-ttu-id="7f454-125">Base hexadecimal</span><span class="sxs-lookup"><span data-stu-id="7f454-125">Hexadecimal base</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f454-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f454-126">Remarks</span></span>

<span data-ttu-id="7f454-127">Uma matriz das estruturas **\_ HANDOFFENTRY do PF** é usada na estrutura [do \_ entregador de PF](pf-handoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="7f454-127">An array of the **PF\_HANDOFFENTRY** structures is used in the [PF\_HANDOFFSET](pf-handoffset.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f454-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f454-128">Requirements</span></span>



| <span data-ttu-id="7f454-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f454-129">Requirement</span></span> | <span data-ttu-id="7f454-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7f454-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f454-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f454-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7f454-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f454-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7f454-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f454-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7f454-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f454-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f454-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7f454-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f454-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f454-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f454-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f454-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f454-138">teleentregador de PF \_</span><span class="sxs-lookup"><span data-stu-id="7f454-138">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> </dl>

 

 




