---
title: Função RtmCloseEnumerationHandle (RTM. h)
description: O RtmCloseEnumerationHandle encerra uma enumeração especificada e libera os recursos associados.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- Função RtmCloseEnumerationHandle RAS
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009513"
---
# <a name="rtmcloseenumerationhandle-function"></a><span data-ttu-id="1a450-104">Função RtmCloseEnumerationHandle</span><span class="sxs-lookup"><span data-stu-id="1a450-104">RtmCloseEnumerationHandle function</span></span>

<span data-ttu-id="1a450-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1a450-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1a450-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="1a450-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1a450-107">O **RtmCloseEnumerationHandle** encerra uma enumeração especificada e libera os recursos associados.</span><span class="sxs-lookup"><span data-stu-id="1a450-107">The **RtmCloseEnumerationHandle** terminates a specified enumeration and frees the associated resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a450-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a450-108">Syntax</span></span>


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a><span data-ttu-id="1a450-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a450-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a450-110">*EnumerationHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a450-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a450-111">Identificador para a enumeração terminar.</span><span class="sxs-lookup"><span data-stu-id="1a450-111">Handle to the enumeration to terminate.</span></span> <span data-ttu-id="1a450-112">Obtenha esse identificador chamando [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="1a450-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a450-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a450-113">Return value</span></span>

<span data-ttu-id="1a450-114">Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.</span><span class="sxs-lookup"><span data-stu-id="1a450-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="1a450-115">Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a450-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="1a450-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1a450-116">Value</span></span>                                                                                                       | <span data-ttu-id="1a450-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a450-117">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a450-118"><dt>**\_identificador inválido do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a450-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="1a450-119">O parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="1a450-119">The parameter is not valid.</span></span><br/>                                  |
| <dl> <span data-ttu-id="1a450-120"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a450-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="1a450-121">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="1a450-121">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a450-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a450-122">Requirements</span></span>



| <span data-ttu-id="1a450-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a450-123">Requirement</span></span> | <span data-ttu-id="1a450-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1a450-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a450-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a450-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a450-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1a450-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1a450-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a450-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a450-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a450-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1a450-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1a450-129">End of server support</span></span><br/>    | <span data-ttu-id="1a450-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a450-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="1a450-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a450-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a450-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a450-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a450-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a450-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a450-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a450-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a450-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1a450-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a450-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a450-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a450-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a450-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a450-138">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="1a450-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1a450-139">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="1a450-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="1a450-140">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="1a450-140">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="1a450-141">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="1a450-141">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





