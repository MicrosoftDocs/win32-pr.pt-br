---
title: Transação de XTYP_UNREGISTER (ddeml. h)
description: Uma função de retorno de chamada de troca dinâmica de dados (DDE), DdeCallback, recebe a \_ transação de CANcelamento de registro XTYP sempre que um aplicativo de servidor de biblioteca de gerenciamento de troca dinâmica de dados (ddeml) usa a função DdeNameService para cancelar o registro de um nome de serviço ou sempre que um aplicativo não ddeml que dá suporte ao tópico do sistema é encerrado.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Troca de dados de transação XTYP_UNREGISTER
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644992"
---
# <a name="xtyp_unregister-transaction"></a><span data-ttu-id="35fed-104">XTYP \_ Cancelar registro da transação</span><span class="sxs-lookup"><span data-stu-id="35fed-104">XTYP\_UNREGISTER transaction</span></span>

<span data-ttu-id="35fed-105">Uma função de retorno de chamada de troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ cancelamento de registro XTYP** sempre que um aplicativo de servidor de biblioteca de gerenciamento de troca dinâmica de dados (ddeml) usa a função [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para cancelar o registro de um nome de serviço ou sempre que um aplicativo não ddeml que dá suporte ao tópico do sistema é encerrado.</span><span class="sxs-lookup"><span data-stu-id="35fed-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_UNREGISTER** transaction whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to unregister a service name, or whenever a non-DDEML application that supports the System topic is terminated.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="35fed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35fed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fed-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="35fed-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-108">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="35fed-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="35fed-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="35fed-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="35fed-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="35fed-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="35fed-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="35fed-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="35fed-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="35fed-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-114">Um identificador para o nome do serviço base que está sendo cancelado.</span><span class="sxs-lookup"><span data-stu-id="35fed-114">A handle to the base service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="35fed-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="35fed-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-116">Um identificador para o nome do serviço específico da instância que está sendo cancelado.</span><span class="sxs-lookup"><span data-stu-id="35fed-116">A handle to the instance-specific service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="35fed-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="35fed-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="35fed-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="35fed-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="35fed-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="35fed-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="35fed-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="35fed-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="35fed-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="35fed-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35fed-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="35fed-123">Remarks</span></span>

<span data-ttu-id="35fed-124">Essa transação será filtrada se o aplicativo tiver especificado o sinalizador **CBF \_ ignorar \_ registros** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="35fed-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="35fed-125">Um aplicativo não pode bloquear esse tipo de transação; o \_ código de retorno de bloco CBR é ignorado.</span><span class="sxs-lookup"><span data-stu-id="35fed-125">A application cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

<span data-ttu-id="35fed-126">Um aplicativo deve usar o parâmetro *hsz1* para remover o nome do serviço da lista de servidores disponíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="35fed-126">An application should use the *hsz1* parameter to remove the service name from the list of servers available to the user.</span></span> <span data-ttu-id="35fed-127">Um aplicativo deve usar o parâmetro *hsz2* para identificar qual instância de aplicativo foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="35fed-127">An application should use the *hsz2* parameter to identify which application instance has terminated.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fed-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35fed-128">Requirements</span></span>



| <span data-ttu-id="35fed-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="35fed-129">Requirement</span></span> | <span data-ttu-id="35fed-130">Valor</span><span class="sxs-lookup"><span data-stu-id="35fed-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fed-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35fed-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35fed-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="35fed-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="35fed-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35fed-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35fed-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="35fed-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="35fed-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="35fed-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fed-136"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35fed-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fed-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="35fed-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="35fed-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="35fed-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35fed-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="35fed-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="35fed-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="35fed-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="35fed-141">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="35fed-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35fed-142">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="35fed-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

