---
description: A função loaddword é chamada pelo monitor para definir uma variável DWORD com um valor extraído de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Função loaddword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778537"
---
# <a name="loaddword-function"></a><span data-ttu-id="b073c-103">Função loaddword</span><span class="sxs-lookup"><span data-stu-id="b073c-103">LoadDWORD function</span></span>

<span data-ttu-id="b073c-104">A função **loaddword** é chamada pelo monitor para definir uma variável **DWORD** com um valor extraído de uma variável de cadeia de caracteres de configuração html.</span><span class="sxs-lookup"><span data-stu-id="b073c-104">The **LoadDWORD** function is called by the monitor to set a **DWORD** variable with a value taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b073c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b073c-105">Syntax</span></span>


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b073c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b073c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b073c-107">*pConfig* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b073c-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b073c-108">Ponteiro para a cadeia de caracteres de configuração HTML passado para o monitor pelo método [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="b073c-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b073c-109">*pVarName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b073c-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b073c-110">Ponteiro para o nome da variável na cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="b073c-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="b073c-111">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b073c-111">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b073c-112">Ponteiro para a variável **DWORD** que é definida como o valor da variável de cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="b073c-112">Pointer to the **DWORD** variable that is set to the value of the configuration string variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b073c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b073c-113">Return value</span></span>

<span data-ttu-id="b073c-114">Se a função for bem-sucedida (se o nome da variável tiver sido encontrado e tiver uma cadeia de caracteres que não seja de comprimento zero), o **DWORD** será inserido e o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="b073c-114">If the function is successful (if the variable name was found and had a non-zero-length string), the **DWORD** is inserted, and the return value is **TRUE**.</span></span>

<span data-ttu-id="b073c-115">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="b073c-115">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b073c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b073c-116">Requirements</span></span>



| <span data-ttu-id="b073c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b073c-117">Requirement</span></span> | <span data-ttu-id="b073c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b073c-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b073c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b073c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b073c-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b073c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b073c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b073c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b073c-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b073c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b073c-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b073c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b073c-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b073c-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b073c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b073c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b073c-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b073c-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b073c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b073c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b073c-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b073c-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




