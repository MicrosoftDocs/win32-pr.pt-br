---
description: Compara dois tokens de acesso e determina se eles são equivalentes em relação a uma chamada para a função AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Função NtCompareTokens (Ntseapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750574"
---
# <a name="ntcomparetokens-function"></a><span data-ttu-id="c0cbe-103">Função NtCompareTokens</span><span class="sxs-lookup"><span data-stu-id="c0cbe-103">NtCompareTokens function</span></span>

<span data-ttu-id="c0cbe-104">A função **NtCompareTokens** compara dois [*tokens de acesso*](/windows/desktop/SecGloss/a-gly) e determina se eles são equivalentes em relação a uma chamada para a função [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .</span><span class="sxs-lookup"><span data-stu-id="c0cbe-104">The **NtCompareTokens** function compares two [*access tokens*](/windows/desktop/SecGloss/a-gly) and determines whether they are equivalent with respect to a call to the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0cbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0cbe-105">Syntax</span></span>


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a><span data-ttu-id="c0cbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0cbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0cbe-107">*FirstTokenHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0cbe-107">*FirstTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0cbe-108">Um identificador para o primeiro token de acesso a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-108">A handle to the first access token to compare.</span></span> <span data-ttu-id="c0cbe-109">O token deve estar aberto para acesso de **\_ consulta de token** .</span><span class="sxs-lookup"><span data-stu-id="c0cbe-109">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="c0cbe-110">*SecondTokenHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0cbe-110">*SecondTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0cbe-111">Um identificador para o segundo token de acesso a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-111">A handle to the second access token to compare.</span></span> <span data-ttu-id="c0cbe-112">O token deve estar aberto para acesso de **\_ consulta de token** .</span><span class="sxs-lookup"><span data-stu-id="c0cbe-112">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="c0cbe-113">*Igual* \[ a fora\]</span><span class="sxs-lookup"><span data-stu-id="c0cbe-113">*Equal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0cbe-114">Um ponteiro para uma variável que recebe um valor que indica se os tokens representados pelos parâmetros *FirstTokenHandle* e *SecondTokenHandle* são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-114">A pointer to a variable that receives a value that indicates whether the tokens represented by the *FirstTokenHandle* and *SecondTokenHandle* parameters are equivalent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0cbe-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0cbe-115">Return value</span></span>

<span data-ttu-id="c0cbe-116">Se a função for bem-sucedida, a função retornará o STATUS \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-116">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="c0cbe-117">Se a função falhar, ela retornará um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="c0cbe-117">If the function fails, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0cbe-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0cbe-118">Remarks</span></span>

<span data-ttu-id="c0cbe-119">Dois tokens de controle de acesso são considerados equivalentes se todas as condições a seguir forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="c0cbe-119">Two access control tokens are considered to be equivalent if all of the following conditions are true:</span></span>

-   <span data-ttu-id="c0cbe-120">Todo Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) que está presente em um dos tokens também está presente no outro token.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-120">Every [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) that is present in either token is also present in the other token.</span></span>
-   <span data-ttu-id="c0cbe-121">Nem ambos os tokens são restritos.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-121">Neither or both of the tokens are restricted.</span></span>
-   <span data-ttu-id="c0cbe-122">Se ambos os tokens forem restritos, cada SID restrito em um token também será restringido no outro token.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-122">If both tokens are restricted, every SID that is restricted in one token is also restricted in the other token.</span></span>
-   <span data-ttu-id="c0cbe-123">Todos os privilégios presentes em um dos tokens também estão presentes no outro token.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-123">Every privilege present in either token is also present in the other token.</span></span>

<span data-ttu-id="c0cbe-124">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c0cbe-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0cbe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0cbe-125">Requirements</span></span>



| <span data-ttu-id="c0cbe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0cbe-126">Requirement</span></span> | <span data-ttu-id="c0cbe-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c0cbe-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cbe-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0cbe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c0cbe-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c0cbe-129">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0cbe-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0cbe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c0cbe-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0cbe-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c0cbe-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0cbe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0cbe-133"><dt>Ntseapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0cbe-133"><dt>Ntseapi.h</dt></span></span> </dl> |
| <span data-ttu-id="c0cbe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c0cbe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0cbe-135"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0cbe-135"><dt>Ntdll.dll</dt></span></span> </dl> |



 

