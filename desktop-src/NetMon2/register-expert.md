---
description: O especialista deve implementar a função de especialista em registro. Monitor de Rede chama a função de especialista de registro para obter informações sobre o especialista.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrar função de retorno de chamada de especialista (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827861"
---
# <a name="register-expert-callback-function"></a><span data-ttu-id="189a5-104">Registrar função de retorno de chamada de especialista</span><span class="sxs-lookup"><span data-stu-id="189a5-104">Register Expert callback function</span></span>

<span data-ttu-id="189a5-105">O especialista deve implementar a função de especialista em **registro** .</span><span class="sxs-lookup"><span data-stu-id="189a5-105">The expert must implement the **Register** expert function.</span></span> <span data-ttu-id="189a5-106">Monitor de Rede chama a função de especialista de **registro** para obter informações sobre o especialista.</span><span class="sxs-lookup"><span data-stu-id="189a5-106">Network Monitor calls the **Register** expert function to obtain information about the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="189a5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="189a5-107">Syntax</span></span>


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a><span data-ttu-id="189a5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="189a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="189a5-109">*pExpertInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="189a5-109">*pExpertInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="189a5-110">Ponteiro para uma estrutura [**EXPERTENUMINFO**](expertenuminfo.md) que monitor de rede aloca.</span><span class="sxs-lookup"><span data-stu-id="189a5-110">Pointer to an [**EXPERTENUMINFO**](expertenuminfo.md) structure that Network Monitor allocates.</span></span> <span data-ttu-id="189a5-111">O especialista preenche a estrutura com todas as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="189a5-111">The expert fills in the structure with all requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="189a5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="189a5-112">Return value</span></span>

<span data-ttu-id="189a5-113">Se a função for bem-sucedida, o valor de retorno será **true** e a função retornará as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="189a5-113">If the function is successful, the return value is **TRUE**, and the function returns the requested information.</span></span>

<span data-ttu-id="189a5-114">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="189a5-114">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="189a5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="189a5-115">Remarks</span></span>

<span data-ttu-id="189a5-116">O membro da **versão** da estrutura [**EXPERTENUMINFO**](expertenuminfo.md) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="189a5-116">The **Version** member of the [**EXPERTENUMINFO**](expertenuminfo.md) structure must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="189a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="189a5-117">Requirements</span></span>



| <span data-ttu-id="189a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="189a5-118">Requirement</span></span> | <span data-ttu-id="189a5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="189a5-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="189a5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="189a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="189a5-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="189a5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="189a5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="189a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="189a5-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="189a5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="189a5-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="189a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="189a5-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="189a5-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




