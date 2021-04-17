---
description: Fornece uma linha no painel superior do Visualizador de Eventos que serve como um contêiner para todos os dados possíveis inseridos em uma coluna.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Estrutura NMCOLUMNVARIANT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748425"
---
# <a name="nmcolumnvariant-structure"></a><span data-ttu-id="36c93-103">Estrutura NMCOLUMNVARIANT</span><span class="sxs-lookup"><span data-stu-id="36c93-103">NMCOLUMNVARIANT structure</span></span>

<span data-ttu-id="36c93-104">A estrutura **NMCOLUMNVARIANT** fornece uma linha no painel superior do Visualizador de eventos que serve como um contêiner para todos os dados possíveis inseridos em uma coluna.</span><span class="sxs-lookup"><span data-stu-id="36c93-104">The **NMCOLUMNVARIANT** structure provides a line in the top pane of the Event Viewer that serves as a container for all possible data inserted into a column.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c93-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36c93-105">Syntax</span></span>


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a><span data-ttu-id="36c93-106">Membros</span><span class="sxs-lookup"><span data-stu-id="36c93-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="36c93-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36c93-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-108">Um valor do tipo de enumeração [**NMCOLUMNTYPE**](nmcolumntype.md) .</span><span class="sxs-lookup"><span data-stu-id="36c93-108">A value from the [**NMCOLUMNTYPE**](nmcolumntype.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="36c93-109">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36c93-110">**Uint8Val**</span><span class="sxs-lookup"><span data-stu-id="36c93-110">**Uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-111">valor inteiro sem sinal de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="36c93-111">8-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-112">**Sint8Val**</span><span class="sxs-lookup"><span data-stu-id="36c93-112">**Sint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-113">valor inteiro com sinal de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="36c93-113">8-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-114">**Uint16Val**</span><span class="sxs-lookup"><span data-stu-id="36c93-114">**Uint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-115">valor inteiro sem sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="36c93-115">16-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-116">**Sint16Val**</span><span class="sxs-lookup"><span data-stu-id="36c93-116">**Sint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-117">valor inteiro com sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="36c93-117">16-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-118">**Uint32Val**</span><span class="sxs-lookup"><span data-stu-id="36c93-118">**Uint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-119">valor inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="36c93-119">32-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-120">**Sint32Val**</span><span class="sxs-lookup"><span data-stu-id="36c93-120">**Sint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-121">valor inteiro de 32 bits assinado.</span><span class="sxs-lookup"><span data-stu-id="36c93-121">32-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-122">**Float64Val**</span><span class="sxs-lookup"><span data-stu-id="36c93-122">**Float64Val**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-123">valor float de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="36c93-123">64-bit float value.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-124">**FrameVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-124">**FrameVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-125">Número do quadro.</span><span class="sxs-lookup"><span data-stu-id="36c93-125">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-126">**YesNoVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-126">**YesNoVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-127">Exibe Sim ou não.</span><span class="sxs-lookup"><span data-stu-id="36c93-127">Displays Yes or No.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-128">**OnOffVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-128">**OnOffVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-129">Exibe ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="36c93-129">Displays On or Off.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-130">**TrueFalseVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-130">**TrueFalseVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-131">Exibe verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="36c93-131">Displays True or False.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-132">**MACAddrVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-132">**MACAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-133">Endereço MAC.</span><span class="sxs-lookup"><span data-stu-id="36c93-133">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-134">**IPXAddrVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-134">**IPXAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-135">Endereço IPX.</span><span class="sxs-lookup"><span data-stu-id="36c93-135">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-136">**IPAddrVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-136">**IPAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-137">Endereço IP.</span><span class="sxs-lookup"><span data-stu-id="36c93-137">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-138">**VarTimeVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-138">**VarTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-139">Hora da variante.</span><span class="sxs-lookup"><span data-stu-id="36c93-139">Variant time.</span></span> <span data-ttu-id="36c93-140">Use **VariantTimetoSystemTime** para converter em hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="36c93-140">Use **VariantTimetoSystemTime** to convert to system time.</span></span>

</dd> <dt>

<span data-ttu-id="36c93-141">**pStringVal**</span><span class="sxs-lookup"><span data-stu-id="36c93-141">**pStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="36c93-142">Ponteiro para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="36c93-142">Pointer to a string.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36c93-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36c93-143">Requirements</span></span>



| <span data-ttu-id="36c93-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="36c93-144">Requirement</span></span> | <span data-ttu-id="36c93-145">Valor</span><span class="sxs-lookup"><span data-stu-id="36c93-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36c93-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36c93-146">Minimum supported client</span></span><br/> | <span data-ttu-id="36c93-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36c93-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="36c93-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36c93-148">Minimum supported server</span></span><br/> | <span data-ttu-id="36c93-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36c93-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36c93-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="36c93-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="36c93-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c93-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c93-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="36c93-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c93-153">**NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="36c93-153">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)
</dt> </dl>

 

 




