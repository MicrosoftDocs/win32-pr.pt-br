---
description: A função IsValidDevmode verifica se o conteúdo de uma estrutura DEVMODE é válido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Função IsValidDevmode (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105816034"
---
# <a name="isvaliddevmode-function"></a><span data-ttu-id="77465-103">Função IsValidDevmode</span><span class="sxs-lookup"><span data-stu-id="77465-103">IsValidDevmode function</span></span>

<span data-ttu-id="77465-104">A função **IsValidDevmode** verifica se o conteúdo de uma estrutura DEVMODE é válido.</span><span class="sxs-lookup"><span data-stu-id="77465-104">The **IsValidDevmode** function verifies that the contents of a DEVMODE structure are valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="77465-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77465-105">Syntax</span></span>


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a><span data-ttu-id="77465-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77465-107">*pDevmode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77465-107">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77465-108">Um ponteiro para o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) a ser validado.</span><span class="sxs-lookup"><span data-stu-id="77465-108">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to validate.</span></span>

</dd> <dt>

<span data-ttu-id="77465-109">*DevmodeSize*</span><span class="sxs-lookup"><span data-stu-id="77465-109">*DevmodeSize*</span></span> 
</dt> <dd>

<span data-ttu-id="77465-110">O tamanho em bytes do buffer de bytes de entrada.</span><span class="sxs-lookup"><span data-stu-id="77465-110">The size in bytes of the input byte buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77465-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77465-111">Return value</span></span>

<span data-ttu-id="77465-112">**True**, se o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) for estruturalmente válido.</span><span class="sxs-lookup"><span data-stu-id="77465-112">**TRUE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is structurally valid.</span></span> <span data-ttu-id="77465-113">Se forem encontrados erros secundários, a função os corrigirá e retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="77465-113">If minor errors are found the function will fix them and return **TRUE**.</span></span>

<span data-ttu-id="77465-114">**False**, se o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) tiver um ou mais problemas estruturais significativos.</span><span class="sxs-lookup"><span data-stu-id="77465-114">**FALSE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) has one or more significant structural problems.</span></span> <span data-ttu-id="77465-115">Por exemplo, seu membro **dmSize** está desalinhado ou especifica um buffer muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="77465-115">For example, its **dmSize** member is misaligned or specifies a buffer that is too small.</span></span> <span data-ttu-id="77465-116">Além disso, **false** se **pDevmode** for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="77465-116">Also, **FALSE** if **pDevmode** is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="77465-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="77465-117">Remarks</span></span>

<span data-ttu-id="77465-118">Nenhum campo de driver de impressora privada do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) está marcado, somente os campos públicos.</span><span class="sxs-lookup"><span data-stu-id="77465-118">No private printer driver fields of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) are checked, only the public fields.</span></span>

<span data-ttu-id="77465-119">Os chamadores devem usar **dmSize** + **dmDriverExtra** para **DevmodeSize** somente se puderem garantir que o tamanho do buffer de entrada seja pelo menos tão grande.</span><span class="sxs-lookup"><span data-stu-id="77465-119">Callers should use **dmSize**+**dmDriverExtra** for **DevmodeSize** only if they can guarantee that the input buffer size is at least that big.</span></span> <span data-ttu-id="77465-120">Como o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) geralmente é um dado não confiável, os valores que estão no buffer de entrada nos deslocamentos **dmSize** e **dmDriverExtra** também são não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="77465-120">Since the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is generally untrusted data, the values that are in the input buffer at the **dmSize** and **dmDriverExtra** offsets are also untrusted.</span></span>

<span data-ttu-id="77465-121">Essa função é executável no contexto de LUA (Least-Privileged User Account).</span><span class="sxs-lookup"><span data-stu-id="77465-121">This function is executable in Least-Privileged User Account (LUA) context.</span></span>

## <a name="requirements"></a><span data-ttu-id="77465-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77465-122">Requirements</span></span>



| <span data-ttu-id="77465-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="77465-123">Requirement</span></span> | <span data-ttu-id="77465-124">Valor</span><span class="sxs-lookup"><span data-stu-id="77465-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77465-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77465-125">Minimum supported client</span></span><br/> | <span data-ttu-id="77465-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="77465-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="77465-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77465-127">Minimum supported server</span></span><br/> | <span data-ttu-id="77465-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77465-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77465-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77465-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="77465-130"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="77465-130"><dt>Winspool.h</dt></span></span> </dl>   |
| <span data-ttu-id="77465-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77465-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="77465-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77465-132"><dt>Winspool.lib</dt></span></span> </dl> |
| <span data-ttu-id="77465-133">DLL</span><span class="sxs-lookup"><span data-stu-id="77465-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77465-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="77465-134"><dt>Winspool.drv</dt></span></span> </dl> |
| <span data-ttu-id="77465-135">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="77465-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="77465-136">**IsValidDevmodeW** (Unicode) e **IsValidDevmodeA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="77465-136">**IsValidDevmodeW** (Unicode) and **IsValidDevmodeA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="77465-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="77465-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77465-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="77465-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="77465-139">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="77465-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="77465-140">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="77465-140">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




