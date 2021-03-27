---
description: Converte caracteres minúsculos em um buffer em caracteres maiúsculos.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Função CharUpperBuffWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501437"
---
# <a name="charupperbuffwrapw-function"></a><span data-ttu-id="c3667-103">Função CharUpperBuffWrapW</span><span class="sxs-lookup"><span data-stu-id="c3667-103">CharUpperBuffWrapW function</span></span>

<span data-ttu-id="c3667-104">\[O **CharUpperBuffWrapW** está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3667-104">\[**CharUpperBuffWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="c3667-105">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c3667-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="c3667-106">Você deve usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) em seu lugar.\]</span><span class="sxs-lookup"><span data-stu-id="c3667-106">You should use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in its place.\]</span></span>

<span data-ttu-id="c3667-107">Converte caracteres minúsculos em um buffer em caracteres maiúsculos.</span><span class="sxs-lookup"><span data-stu-id="c3667-107">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="c3667-108">A função converte os caracteres em vigor.</span><span class="sxs-lookup"><span data-stu-id="c3667-108">The function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="c3667-109">**CharUpperBuffWrapW** é um wrapper para a função **CharUpperBuffW** .</span><span class="sxs-lookup"><span data-stu-id="c3667-109">**CharUpperBuffWrapW** is a wrapper for the **CharUpperBuffW** function.</span></span> <span data-ttu-id="c3667-110">Consulte a página [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="c3667-110">See the [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c3667-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3667-111">Syntax</span></span>


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a><span data-ttu-id="c3667-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3667-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3667-113">*PCH* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3667-113">*pch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3667-114">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c3667-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="c3667-115">Um ponteiro para um buffer que contém um ou mais caracteres Unicode a serem processados.</span><span class="sxs-lookup"><span data-stu-id="c3667-115">A pointer to a buffer that contains one or more Unicode characters to process.</span></span>

</dd> <dt>

<span data-ttu-id="c3667-116">*cchLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3667-116">*cchLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3667-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c3667-117">Type: **DWORD**</span></span>

<span data-ttu-id="c3667-118">Especifica o tamanho, em caracteres, do buffer apontado por *PCH*.</span><span class="sxs-lookup"><span data-stu-id="c3667-118">Specifies the size, in characters, of the buffer pointed to by *pch*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3667-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3667-119">Return value</span></span>

<span data-ttu-id="c3667-120">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c3667-120">Type: **DWORD**</span></span>

<span data-ttu-id="c3667-121">O número de caracteres processados.</span><span class="sxs-lookup"><span data-stu-id="c3667-121">The number of characters processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3667-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3667-122">Remarks</span></span>

<span data-ttu-id="c3667-123">O método preferencial é usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="c3667-123">The preferred method is to use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="c3667-124">**CharUpperBuffWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 44.</span><span class="sxs-lookup"><span data-stu-id="c3667-124">**CharUpperBuffWrapW** must be called directly from Shlwapi.dll, using ordinal 44.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3667-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3667-125">Requirements</span></span>



| <span data-ttu-id="c3667-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3667-126">Requirement</span></span> | <span data-ttu-id="c3667-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c3667-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3667-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3667-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c3667-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c3667-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3667-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3667-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c3667-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3667-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c3667-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c3667-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3667-133"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c3667-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3667-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3667-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3667-135">**CharUpperBuff**</span><span class="sxs-lookup"><span data-stu-id="c3667-135">**CharUpperBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
