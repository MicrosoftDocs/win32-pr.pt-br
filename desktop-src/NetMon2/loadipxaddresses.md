---
description: A função LoadIPXAddresses é chamada pelo monitor para preencher uma lista de endereços IPX Obtida de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Função LoadIPXAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171286"
---
# <a name="loadipxaddresses-function"></a><span data-ttu-id="f4590-103">Função LoadIPXAddresses</span><span class="sxs-lookup"><span data-stu-id="f4590-103">LoadIPXAddresses function</span></span>

<span data-ttu-id="f4590-104">A função **LoadIPXAddresses** é chamada pelo monitor para preencher uma lista de endereços IPX Obtida de uma variável de cadeia de caracteres de configuração html.</span><span class="sxs-lookup"><span data-stu-id="f4590-104">The **LoadIPXAddresses** function is called by the monitor to fill in an IPX address list taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4590-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4590-105">Syntax</span></span>


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="f4590-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4590-107">*pConfig* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4590-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4590-108">Ponteiro para a cadeia de caracteres de configuração HTML passado para o monitor pelo método [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="f4590-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f4590-109">*pVarName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4590-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4590-110">Ponteiro para o nome da variável na cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="f4590-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="f4590-111">*ppAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f4590-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4590-112">Ponteiro para um ponteiro para uma matriz de endereços.</span><span class="sxs-lookup"><span data-stu-id="f4590-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="f4590-113">Se a variável especificada em *pVarName* for encontrada e tiver um comprimento diferente de zero, o espaço suficiente será alocado (usando **HeapAllocMemory**) e todos os endereços IPX serão armazenados como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="f4590-113">If the variable specified in *pVarName* is found and has a non-zero-length, sufficient space is allocated (by using **HeapAllocMemory**), and all the IPX addresses are stored as an array.</span></span>

</dd> <dt>

<span data-ttu-id="f4590-114">*pNumAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f4590-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4590-115">Ponteiro para a variável **DWORD** que é definido como o número de endereços IPX extraídos da cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="f4590-115">Pointer to the **DWORD** variable that is set to the number of IPX addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4590-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4590-116">Return value</span></span>

<span data-ttu-id="f4590-117">Se a função for bem-sucedida (o nome da variável foi encontrado e tiver uma cadeia de caracteres que não seja de comprimento zero que representou endereços IPX), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="f4590-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IPX addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="f4590-118">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="f4590-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4590-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4590-119">Requirements</span></span>



| <span data-ttu-id="f4590-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4590-120">Requirement</span></span> | <span data-ttu-id="f4590-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f4590-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f4590-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4590-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4590-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4590-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f4590-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4590-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4590-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4590-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f4590-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f4590-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4590-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4590-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f4590-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4590-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4590-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4590-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f4590-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f4590-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4590-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4590-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




