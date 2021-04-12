---
description: Chama a biblioteca para obter o estado de segurança relativo ao host, e script ou msi a ser usado.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Função WldpGetLockdownPolicy (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500903"
---
# <a name="wldpgetlockdownpolicy-function"></a><span data-ttu-id="fea08-103">Função WldpGetLockdownPolicy</span><span class="sxs-lookup"><span data-stu-id="fea08-103">WldpGetLockdownPolicy function</span></span>

<span data-ttu-id="fea08-104">Chama a biblioteca para obter o estado de segurança relativo ao host, e script ou msi a ser usado.</span><span class="sxs-lookup"><span data-stu-id="fea08-104">Calls the library to get the security state relative to the host, and script or msi to be used.</span></span> <span data-ttu-id="fea08-105">A função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="fea08-105">The function has no associated import library.</span></span> <span data-ttu-id="fea08-106">Você deve usar as funções LoadLibrary e GetProcAddress para vincular dinamicamente a wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="fea08-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="fea08-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fea08-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fea08-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fea08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea08-109">*hostInformation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fea08-109">*hostInformation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fea08-110">Uma estrutura de [**\_ \_ informações de host WLDP**](wldp-host-information.md) que identifica o host e o arquivo de origem a serem avaliados.</span><span class="sxs-lookup"><span data-stu-id="fea08-110">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host and source file to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="fea08-111">*lockdownstate* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fea08-111">*lockdownState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fea08-112">Fornece o valor seguro da política resultante.</span><span class="sxs-lookup"><span data-stu-id="fea08-112">Provides the resulting policy secure value.</span></span> <span data-ttu-id="fea08-113">Que! WLDP_LOCKDOWN_IS_OFF, então UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fea08-113">If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled.</span></span> <span data-ttu-id="fea08-114">Você também pode verificar WLDP_LOCKDOWN_IS_AUDIT e WLDP_LOCKDOWN_IS_ENFORCE para determinar se uma política está no modo auditar ou impor.</span><span class="sxs-lookup"><span data-stu-id="fea08-114">You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.</span></span>
</dd> <dt>

<span data-ttu-id="fea08-115">*lockdownFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fea08-115">*lockdownFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea08-116">Os seguintes valores de sinalizador são definidos WLDP \_ flags \_ SKIPSIGNATUREVALIDATION 0x00000100 – quando definido, ignore a validação de SaferIdentifyLevel, o que irá ignorar se um script está assinado.</span><span class="sxs-lookup"><span data-stu-id="fea08-116">The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea08-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fea08-117">Return value</span></span>

<span data-ttu-id="fea08-118">Esse método retornará S \_ OK, se for bem-sucedido ou um código de falha.</span><span class="sxs-lookup"><span data-stu-id="fea08-118">This method returns S\_OK if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fea08-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fea08-119">Remarks</span></span>

<span data-ttu-id="fea08-120">Quando chamado com WLDP \_ host \_ Information. SZSOURCE = NULL, a política genérica para o host é retornada.</span><span class="sxs-lookup"><span data-stu-id="fea08-120">When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.</span></span>

<span data-ttu-id="fea08-121">Quando chamado com WLDP \_ host \_ Information. DWHOSTID = WLDP \_ host \_ ID \_ global, WLDP \_ host \_ Information. szSource deve ser NULL e a função retornará a política global do sistema.</span><span class="sxs-lookup"><span data-stu-id="fea08-121">When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.</span></span>

<span data-ttu-id="fea08-122">Os \_ sinalizadores SKIPSIGNATUREVALIDATION WLDP dwFlag \_ podem ser usados para ignorar a validação de SaferIdentifyLevel (), o que irá ignorar se um script está assinado.</span><span class="sxs-lookup"><span data-stu-id="fea08-122">The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea08-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fea08-123">Requirements</span></span>



| <span data-ttu-id="fea08-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fea08-124">Requirement</span></span> | <span data-ttu-id="fea08-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fea08-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fea08-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fea08-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fea08-127">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fea08-127">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fea08-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fea08-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fea08-129">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="fea08-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fea08-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fea08-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea08-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea08-131"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fea08-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fea08-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fea08-133"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fea08-133"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




