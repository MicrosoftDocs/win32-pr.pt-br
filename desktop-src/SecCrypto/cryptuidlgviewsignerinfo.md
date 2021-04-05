---
description: Exibe uma caixa de diálogo que contém as informações de signatário de uma mensagem assinada.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Função CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826985"
---
# <a name="cryptuidlgviewsignerinfo-function"></a><span data-ttu-id="92a18-103">Função CryptUIDlgViewSignerInfo</span><span class="sxs-lookup"><span data-stu-id="92a18-103">CryptUIDlgViewSignerInfo function</span></span>

<span data-ttu-id="92a18-104">\[A função **CryptUIDlgViewSignerInfo** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="92a18-104">\[The **CryptUIDlgViewSignerInfo** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="92a18-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="92a18-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="92a18-106">\]</span><span class="sxs-lookup"><span data-stu-id="92a18-106">\]</span></span>

<span data-ttu-id="92a18-107">A função **CryptUIDlgViewSignerInfo** exibe uma caixa de diálogo que contém as informações de signatário de uma mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="92a18-107">The **CryptUIDlgViewSignerInfo** function displays a dialog box that contains the signer information for a signed message.</span></span>

> [!Note]  
> <span data-ttu-id="92a18-108">Essa função não é declarada em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="92a18-108">This function is not declared in a published header file.</span></span> <span data-ttu-id="92a18-109">Para usar essa estrutura, declare-a no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="92a18-109">To use this structure, declare it in the exact format shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a18-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92a18-110">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="92a18-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92a18-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a18-112">*pcvsi* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92a18-112">*pcvsi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a18-113">Um ponteiro para uma estrutura de [**\_ \_ struct CRYPTUI VIEWSIGNERINFO**](cryptui-viewsignerinfo-struct.md) que contém as informações de signatário a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="92a18-113">A pointer to a [**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**](cryptui-viewsignerinfo-struct.md) structure that contains the signer information to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a18-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92a18-114">Return value</span></span>

<span data-ttu-id="92a18-115">Essa função retorna um valor diferente de zero em caso de êxito e zero em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="92a18-115">This function returns a nonzero value on success and zero on failure.</span></span> <span data-ttu-id="92a18-116">Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="92a18-116">For extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="92a18-117">Os códigos de erro possíveis retornados de [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="92a18-117">Possible error codes returned from [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) include, but are not limited to, the following.</span></span>



| <span data-ttu-id="92a18-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="92a18-118">Return code</span></span>                                                                                   | <span data-ttu-id="92a18-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="92a18-119">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="92a18-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="92a18-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="92a18-121">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="92a18-121">One or more arguments are not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="92a18-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="92a18-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="92a18-123">Ocorreu uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="92a18-123">A memory allocation failure occurred.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="92a18-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a18-124">Requirements</span></span>



| <span data-ttu-id="92a18-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a18-125">Requirement</span></span> | <span data-ttu-id="92a18-126">Valor</span><span class="sxs-lookup"><span data-stu-id="92a18-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a18-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92a18-127">Minimum supported client</span></span><br/> | <span data-ttu-id="92a18-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92a18-128">Windows XP \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="92a18-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92a18-129">Minimum supported server</span></span><br/> | <span data-ttu-id="92a18-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92a18-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92a18-131">Fim do suporte</span><span class="sxs-lookup"><span data-stu-id="92a18-131">End of support</span></span><br/> | <span data-ttu-id="92a18-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="92a18-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="92a18-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92a18-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="92a18-134"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92a18-134"><dt>Cryptui.lib</dt></span></span> </dl>      |
| <span data-ttu-id="92a18-135">DLL</span><span class="sxs-lookup"><span data-stu-id="92a18-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a18-136"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a18-136"><dt>Cryptui.dll</dt></span></span> </dl>      |
| <span data-ttu-id="92a18-137">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="92a18-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="92a18-138">**CryptUIDlgViewSignerInfoW** (Unicode) e **CryptUIDlgViewSignerInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="92a18-138">**CryptUIDlgViewSignerInfoW** (Unicode) and **CryptUIDlgViewSignerInfoA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92a18-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a18-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a18-140">**CRYPTUI \_ VIEWSIGNERINFO \_ struct**</span><span class="sxs-lookup"><span data-stu-id="92a18-140">**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**</span></span>](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
