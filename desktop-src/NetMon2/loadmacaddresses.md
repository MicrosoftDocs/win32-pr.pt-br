---
description: A função LoadMACAddresses é chamada pelo monitor para preencher uma lista de endereços MAC com endereços extraídos de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Função LoadMACAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501894"
---
# <a name="loadmacaddresses-function"></a><span data-ttu-id="794b3-103">Função LoadMACAddresses</span><span class="sxs-lookup"><span data-stu-id="794b3-103">LoadMACAddresses function</span></span>

<span data-ttu-id="794b3-104">A função **LoadMACAddresses** é chamada pelo monitor para preencher uma lista de endereços MAC com endereços extraídos de uma variável de cadeia de caracteres de configuração html.</span><span class="sxs-lookup"><span data-stu-id="794b3-104">The **LoadMACAddresses** function is called by the monitor to fill in a MAC address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="794b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="794b3-105">Syntax</span></span>


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="794b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="794b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="794b3-107">*pConfig* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="794b3-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794b3-108">Ponteiro para a cadeia de caracteres de configuração HTML passado para o monitor pelo método [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="794b3-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="794b3-109">*pVarName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="794b3-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794b3-110">Ponteiro para o nome da variável na cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="794b3-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="794b3-111">*ppAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="794b3-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794b3-112">Ponteiro para um ponteiro para uma matriz de endereços.</span><span class="sxs-lookup"><span data-stu-id="794b3-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="794b3-113">Se a variável especificada em *pVarName* for encontrada e tiver um comprimento diferente de zero, a função alocará espaço suficiente (usando **HeapAllocMemory**) e armazenará todos os endereços MAC como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="794b3-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space (by using **HeapAllocMemory**) and stores all the MAC addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="794b3-114">*pNumAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="794b3-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794b3-115">Ponteiro para a variável **DWORD** que é definido como o número de endereços MAC obtidos da cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="794b3-115">Pointer to the **DWORD** variable that is set to the number of MAC addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="794b3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="794b3-116">Return value</span></span>

<span data-ttu-id="794b3-117">Se a função for bem-sucedida, (o nome da variável foi encontrado e tinha uma cadeia de comprimento diferente de zero que representava endereços MAC), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="794b3-117">If the function is successful, (the variable name was found and had a non-zero-length string that represented MAC addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="794b3-118">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="794b3-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="794b3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="794b3-119">Requirements</span></span>



| <span data-ttu-id="794b3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="794b3-120">Requirement</span></span> | <span data-ttu-id="794b3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="794b3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="794b3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="794b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="794b3-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="794b3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="794b3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="794b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="794b3-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="794b3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="794b3-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="794b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="794b3-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="794b3-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="794b3-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="794b3-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="794b3-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="794b3-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="794b3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="794b3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="794b3-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="794b3-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




