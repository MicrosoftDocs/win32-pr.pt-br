---
description: A função loadipaddresss é chamada pelo monitor para preencher uma lista de endereços IP com endereços extraídos de uma variável de cadeia de caracteres de configuração HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Função loadipaddresss (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759357"
---
# <a name="loadipaddresses-function"></a><span data-ttu-id="31185-103">Função loadipaddresss</span><span class="sxs-lookup"><span data-stu-id="31185-103">LoadIPAddresses function</span></span>

<span data-ttu-id="31185-104">A função **Loadipaddresss** é chamada pelo monitor para preencher uma lista de endereços IP com endereços extraídos de uma variável de cadeia de caracteres de configuração html.</span><span class="sxs-lookup"><span data-stu-id="31185-104">The **LoadIPAddresses** function is called by the monitor to fill in an IP address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="31185-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31185-105">Syntax</span></span>


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="31185-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31185-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31185-107">*pConfig* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31185-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31185-108">Ponteiro para a cadeia de caracteres de configuração HTML passado para o monitor pelo método [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="31185-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="31185-109">*pVarName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31185-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31185-110">Ponteiro para o nome da variável na cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="31185-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="31185-111">*ppAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31185-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31185-112">Ponteiro para um ponteiro para uma matriz de endereços.</span><span class="sxs-lookup"><span data-stu-id="31185-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="31185-113">Se a variável especificada em *pVarName* for encontrada e tiver um comprimento diferente de zero, a função alocará espaço suficiente e armazenará todos os endereços IP como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="31185-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space and stores all the IP addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="31185-114">*pNumAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31185-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31185-115">Ponteiro para a variável **DWORD** que é definido como o número de endereços IP obtidos da cadeia de caracteres de configuração.</span><span class="sxs-lookup"><span data-stu-id="31185-115">Pointer to the **DWORD** variable that is set to the number of IP addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31185-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31185-116">Return value</span></span>

<span data-ttu-id="31185-117">Se a função for bem-sucedida (o nome da variável foi encontrado e tiver uma cadeia de caracteres que não seja de comprimento zero que representou os endereços IP), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="31185-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IP addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="31185-118">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="31185-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="31185-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="31185-119">Remarks</span></span>

<span data-ttu-id="31185-120">Os endereços IP devem estar no formato x. x. x. x (por exemplo, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="31185-120">The IP addresses must be in x.x.x.x format (for example, 127.0.0.1).</span></span>

## <a name="requirements"></a><span data-ttu-id="31185-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31185-121">Requirements</span></span>



| <span data-ttu-id="31185-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31185-122">Requirement</span></span> | <span data-ttu-id="31185-123">Valor</span><span class="sxs-lookup"><span data-stu-id="31185-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31185-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31185-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31185-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31185-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="31185-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31185-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31185-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31185-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="31185-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31185-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="31185-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="31185-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="31185-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31185-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="31185-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31185-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="31185-132">DLL</span><span class="sxs-lookup"><span data-stu-id="31185-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31185-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31185-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




