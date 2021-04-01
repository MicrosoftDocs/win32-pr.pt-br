---
description: O especialista implementa a função DllMain. O sistema operacional chama DllMain para obter um identificador para uma instância do especialista.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Função de retorno de chamada de especialista de DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828965"
---
# <a name="dllmain-expert-callback-function"></a><span data-ttu-id="f78b0-104">Função de retorno de chamada de especialista de DllMain</span><span class="sxs-lookup"><span data-stu-id="f78b0-104">DllMain Expert callback function</span></span>

<span data-ttu-id="f78b0-105">O especialista implementa a função [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="f78b0-105">The expert implements the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> <span data-ttu-id="f78b0-106">O sistema operacional chama **DllMain** para obter um identificador para uma instância do especialista.</span><span class="sxs-lookup"><span data-stu-id="f78b0-106">The operating system calls **DllMain** to obtain a handle to an instance of the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="f78b0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f78b0-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="f78b0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f78b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f78b0-109">*HINSTANCE* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f78b0-109">*hInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f78b0-110">Manipule a uma instância do especialista.</span><span class="sxs-lookup"><span data-stu-id="f78b0-110">Handle to an instance of the expert.</span></span>

<span data-ttu-id="f78b0-111">Se o especialista usar a interface do usuário Monitor de Rede, o valor *HINSTANCE* deverá ser armazenado em uma variável global.</span><span class="sxs-lookup"><span data-stu-id="f78b0-111">If the expert uses the Network Monitor user interface, the *hInstance* value must be stored in a global variable.</span></span> <span data-ttu-id="f78b0-112">Essa abordagem é necessária somente quando o valor do parâmetro *ulReason* é definido como dll de \_ processo \_ Attach.</span><span class="sxs-lookup"><span data-stu-id="f78b0-112">This approach is necessary only when the value of the *ulReason* parameter is set to DLL\_PROCESS\_ATTACH.</span></span>

</dd> <dt>

<span data-ttu-id="f78b0-113">*ulReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f78b0-113">*ulReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78b0-114">Indicador de por que a função foi chamada.</span><span class="sxs-lookup"><span data-stu-id="f78b0-114">Indicator of why the function was called.</span></span> <span data-ttu-id="f78b0-115">Um valor de \_ anexação do processo de dll \_ , (que se aplica quando a dll é carregada pela primeira vez) indica que o especialista deve salvar o valor *HINSTANCE* em uma variável global.</span><span class="sxs-lookup"><span data-stu-id="f78b0-115">A value of DLL\_PROCESS\_ATTACH, (which applies when the DLL is first loaded) indicates that the expert should save the *hInstance* value in a global variable.</span></span>

<span data-ttu-id="f78b0-116">Com qualquer outro valor, todas as chamadas para a função [**DllMain**](/windows/desktop/Dlls/dllmain) podem ser ignoradas.</span><span class="sxs-lookup"><span data-stu-id="f78b0-116">With any other value, all calls to the [**DllMain**](/windows/desktop/Dlls/dllmain) function can be ignored.</span></span> <span data-ttu-id="f78b0-117">Para obter uma lista de todos os sinalizadores possíveis definidos pelo sistema operacional, consulte **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="f78b0-117">For a list of all possible flags set by the operating system, see **DLLMain**.</span></span>

</dd> <dt>

<span data-ttu-id="f78b0-118">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="f78b0-118">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="f78b0-119">O parâmetro não está em uso.</span><span class="sxs-lookup"><span data-stu-id="f78b0-119">Parameter is not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f78b0-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f78b0-120">Return value</span></span>

<span data-ttu-id="f78b0-121">Se a função for bem-sucedida, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="f78b0-121">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="f78b0-122">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="f78b0-122">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f78b0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f78b0-123">Remarks</span></span>

<span data-ttu-id="f78b0-124">O sistema operacional chama a função de especialista de **DllMain** quando um processo carrega ou descarrega a DLL de especialista.</span><span class="sxs-lookup"><span data-stu-id="f78b0-124">The operating system calls the **DllMain** expert function when a process loads or unloads the expert DLL.</span></span> <span data-ttu-id="f78b0-125">A função de especialista de **DllMain** deve ser exportada somente se o especialista tiver uma interface do usuário para exibir a configuração ou os resultados e, em seguida, apenas para retornar o valor apropriado de *HINSTANCE* .</span><span class="sxs-lookup"><span data-stu-id="f78b0-125">The **DllMain** expert function must be exported only if the expert has a user interface for viewing either configuration or results, and then only to return the proper *hInstance* value.</span></span>

<span data-ttu-id="f78b0-126">A função de especialista de **DllMain** é baseada na função [**DllMain**](/windows/desktop/Dlls/dllmain) da biblioteca de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="f78b0-126">The **DllMain** expert function is based on the dynamic link library [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f78b0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f78b0-127">Requirements</span></span>



| <span data-ttu-id="f78b0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f78b0-128">Requirement</span></span> | <span data-ttu-id="f78b0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f78b0-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f78b0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f78b0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f78b0-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f78b0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f78b0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f78b0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f78b0-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f78b0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f78b0-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f78b0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f78b0-135"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="f78b0-135"><dt>Process.h</dt></span></span> </dl> |



 

