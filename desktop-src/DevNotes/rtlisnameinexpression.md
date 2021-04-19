---
description: Determina se uma cadeia de caracteres Unicode corresponde ao padrão especificado.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: Função RtlIsNameInExpression
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755274"
---
# <a name="rtlisnameinexpression-function"></a><span data-ttu-id="14b05-103">Função RtlIsNameInExpression</span><span class="sxs-lookup"><span data-stu-id="14b05-103">RtlIsNameInExpression function</span></span>

<span data-ttu-id="14b05-104">Determina se uma cadeia de caracteres Unicode corresponde ao padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="14b05-104">Determines whether a Unicode string matches the specified pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b05-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14b05-105">Syntax</span></span>


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a><span data-ttu-id="14b05-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14b05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b05-107">*Expressão* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="14b05-107">*Expression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b05-108">Um ponteiro para a cadeia de caracteres de padrão.</span><span class="sxs-lookup"><span data-stu-id="14b05-108">A pointer to the pattern string.</span></span> <span data-ttu-id="14b05-109">Essa cadeia de caracteres pode conter caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="14b05-109">This string can contain wildcard characters.</span></span> <span data-ttu-id="14b05-110">Se o parâmetro *IgnoreCase* for true, a cadeia de caracteres deverá conter apenas caracteres maiúsculos.</span><span class="sxs-lookup"><span data-stu-id="14b05-110">If the *IgnoreCase* parameter is TRUE, the string must contain only uppercase characters.</span></span>

</dd> <dt>

<span data-ttu-id="14b05-111">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="14b05-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b05-112">Um ponteiro para a cadeia de caracteres a ser comparado com o padrão.</span><span class="sxs-lookup"><span data-stu-id="14b05-112">A pointer to the string to be compared against the pattern.</span></span> <span data-ttu-id="14b05-113">Esta cadeia de caracteres não pode conter caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="14b05-113">This string cannot contain wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="14b05-114">*IgnoreCase* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14b05-114">*IgnoreCase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b05-115">**True** para correspondência que não diferencia maiúsculas de minúsculas ou **false** para correspondência que diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="14b05-115">**TRUE** for case-insensitive matching, or **FALSE** for case-sensitive matching.</span></span>

</dd> <dt>

<span data-ttu-id="14b05-116">*Upcase* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="14b05-116">*UpcaseTable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14b05-117">Um ponteiro opcional para uma tabela de caracteres maiúsculos a ser usado para correspondência que não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="14b05-117">An optional pointer to an uppercase character table to use for case-insensitive matching.</span></span> <span data-ttu-id="14b05-118">Se esse parâmetro for NULL, a tabela de caracteres maiúsculos do sistema padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="14b05-118">If this parameter is NULL, the default system uppercase character table is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b05-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14b05-119">Return value</span></span>

<span data-ttu-id="14b05-120">Retornará **true** se a cadeia de caracteres corresponder ao padrão.</span><span class="sxs-lookup"><span data-stu-id="14b05-120">Returns **TRUE** if the string matches the pattern.</span></span> <span data-ttu-id="14b05-121">Se a cadeia de caracteres não corresponder ao padrão, essa função retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="14b05-121">If the string does not match the pattern, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b05-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="14b05-122">Remarks</span></span>

<span data-ttu-id="14b05-123">Esta função não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="14b05-123">This function has no associated header file.</span></span> <span data-ttu-id="14b05-124">A biblioteca de importação associada, ntdll. lib, está disponível no Microsoft Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="14b05-124">The associated import library, Ntdll.lib, is available in the Microsoft Windows Driver Kit (WDK).</span></span> <span data-ttu-id="14b05-125">Você também pode chamar essa função usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="14b05-125">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b05-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14b05-126">Requirements</span></span>



| <span data-ttu-id="14b05-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b05-127">Requirement</span></span> | <span data-ttu-id="14b05-128">Valor</span><span class="sxs-lookup"><span data-stu-id="14b05-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14b05-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14b05-129">Minimum supported client</span></span><br/> | <span data-ttu-id="14b05-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="14b05-130">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="14b05-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14b05-131">Minimum supported server</span></span><br/> | <span data-ttu-id="14b05-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="14b05-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14b05-133">DLL</span><span class="sxs-lookup"><span data-stu-id="14b05-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14b05-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b05-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
