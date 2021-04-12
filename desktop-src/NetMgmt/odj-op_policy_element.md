---
title: OP_POLICY_ELEMENT
description: Definição de IDL de OP_POLICY_ELEMENT
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104294650"
---
# <a name="op_policy_element-structure"></a><span data-ttu-id="d09d1-103">Estrutura de OP_POLICY_ELEMENT</span><span class="sxs-lookup"><span data-stu-id="d09d1-103">OP_POLICY_ELEMENT structure</span></span>

<span data-ttu-id="d09d1-104">Define uma chave do registro e um nome de valor, tipo e valor que devem ser configurados sob essa chave.</span><span class="sxs-lookup"><span data-stu-id="d09d1-104">Defines a registry key and a value name, type, and value that should be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d09d1-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a><span data-ttu-id="d09d1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d09d1-106">Members</span></span>

### <a name="pkeypath"></a><span data-ttu-id="d09d1-107">pKeyPath</span><span class="sxs-lookup"><span data-stu-id="d09d1-107">pKeyPath</span></span>

<span data-ttu-id="d09d1-108">Contém o caminho da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="d09d1-108">Contains the path of the registry key.</span></span>

### <a name="pvaluename"></a><span data-ttu-id="d09d1-109">Valores principais</span><span class="sxs-lookup"><span data-stu-id="d09d1-109">pValueName</span></span>

<span data-ttu-id="d09d1-110">Contém o nome do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="d09d1-110">Contains the name of the registry value.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="d09d1-111">ulValueType</span><span class="sxs-lookup"><span data-stu-id="d09d1-111">ulValueType</span></span>

<span data-ttu-id="d09d1-112">Contém um dos valores dos [tipos de valor do registro](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="d09d1-112">Contains one of the values from [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

### <a name="cbvaluedata"></a><span data-ttu-id="d09d1-113">cbValueData</span><span class="sxs-lookup"><span data-stu-id="d09d1-113">cbValueData</span></span>

<span data-ttu-id="d09d1-114">Contém o tamanho de pValueData em bytes.</span><span class="sxs-lookup"><span data-stu-id="d09d1-114">Contains the size of pValueData in bytes.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="d09d1-115">ulValueType</span><span class="sxs-lookup"><span data-stu-id="d09d1-115">ulValueType</span></span>

<span data-ttu-id="d09d1-116">Contém o valor do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="d09d1-116">Contains the value of the registry value.</span></span>

## <a name="see-also"></a><span data-ttu-id="d09d1-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d09d1-117">See also</span></span>

[<span data-ttu-id="d09d1-118">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="d09d1-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)