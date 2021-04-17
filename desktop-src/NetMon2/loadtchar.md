---
description: A função LoadTCHAR é chamada por monitores para definir uma variável de cadeia de caracteres para uma cadeia de caracteres Obtida de uma cadeia de caracteres de configuração HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Função LoadTCHAR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790011"
---
# <a name="loadtchar-function"></a><span data-ttu-id="d3340-103">Função LoadTCHAR</span><span class="sxs-lookup"><span data-stu-id="d3340-103">LoadTCHAR function</span></span>

<span data-ttu-id="d3340-104">A função **LoadTCHAR** é chamada por monitores para definir uma variável de cadeia de caracteres para uma cadeia de caracteres Obtida de uma cadeia de caracteres de configuração html.</span><span class="sxs-lookup"><span data-stu-id="d3340-104">The **LoadTCHAR** function is called by monitors to set a string variable to a string taken from an HTML configuration string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3340-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3340-105">Syntax</span></span>


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a><span data-ttu-id="d3340-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3340-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3340-107">*pConfig* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3340-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3340-108">Ponteiro para a cadeia de caracteres de configuração HTML passado para o monitor pelo método [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="d3340-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d3340-109">*pVarName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3340-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3340-110">Ponteiro para o nome da variável na cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="d3340-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="d3340-111">*ppszString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d3340-111">*ppszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3340-112">Ponteiro para um ponteiro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d3340-112">Pointer to a string pointer.</span></span> <span data-ttu-id="d3340-113">Se o nome de variável solicitado for encontrado, a cadeia de caracteres será alocada e atribuída a esse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="d3340-113">If the requested variable name is found, the string is allocated and assigned to this pointer.</span></span> <span data-ttu-id="d3340-114">É responsabilidade do usuário liberar a memória associada à cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d3340-114">It is the user's responsibly to free the memory associated with the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3340-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3340-115">Return value</span></span>

<span data-ttu-id="d3340-116">Se a função for bem-sucedida (se o nome da variável tiver sido encontrado e tiver uma cadeia de caracteres que não seja de comprimento zero), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="d3340-116">If the function is successful (if the variable name was found and had a non-zero-length string), the return value is **TRUE**.</span></span>

<span data-ttu-id="d3340-117">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="d3340-117">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3340-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3340-118">Requirements</span></span>



| <span data-ttu-id="d3340-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3340-119">Requirement</span></span> | <span data-ttu-id="d3340-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d3340-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3340-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3340-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d3340-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3340-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d3340-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3340-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d3340-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3340-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d3340-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d3340-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3340-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3340-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d3340-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3340-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3340-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3340-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d3340-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d3340-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3340-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3340-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




