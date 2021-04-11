---
title: Transação de XTYP_REGISTER (ddeml. h)
description: Uma função de retorno de chamada de troca dinâmica de dados (DDE), DdeCallback, recebe o \_ tipo de transação de registro XTYP sempre que um aplicativo de servidor de biblioteca de gerenciamento de troca dinâmica de dados (ddeml) usa a função DdeNameService para registrar um nome de serviço ou sempre que um aplicativo não ddeml que dá suporte ao tópico System é iniciado.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- Troca de dados de transação XTYP_REGISTER
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454967"
---
# <a name="xtyp_register-transaction"></a><span data-ttu-id="5759c-104">XTYP \_ registrar transação</span><span class="sxs-lookup"><span data-stu-id="5759c-104">XTYP\_REGISTER transaction</span></span>

<span data-ttu-id="5759c-105">Uma função de retorno de chamada de troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe o tipo de transação de **\_ registro XTYP** sempre que um aplicativo de servidor de biblioteca de gerenciamento de troca dinâmica de dados (ddeml) usa a função [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar um nome de serviço ou sempre que um aplicativo não ddeml que dá suporte ao tópico System é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5759c-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_REGISTER** transaction type whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to register a service name, or whenever a non-DDEML application that supports the System topic is started.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="5759c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5759c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5759c-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="5759c-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-108">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="5759c-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5759c-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="5759c-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5759c-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5759c-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="5759c-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5759c-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5759c-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5759c-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-114">Um identificador para o nome do serviço base que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="5759c-114">A handle to the base service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="5759c-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5759c-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-116">Um identificador para o nome do serviço específico da instância que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="5759c-116">A handle to the instance-specific service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="5759c-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="5759c-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5759c-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5759c-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5759c-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5759c-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5759c-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5759c-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5759c-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5759c-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5759c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5759c-123">Remarks</span></span>

<span data-ttu-id="5759c-124">Essa transação será filtrada se o aplicativo tiver especificado o sinalizador **CBF \_ ignorar \_ registros** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="5759c-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="5759c-125">Um aplicativo não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="5759c-125">A application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

<span data-ttu-id="5759c-126">Um aplicativo deve usar o parâmetro *hsz1* para adicionar o nome do serviço à lista de servidores disponíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5759c-126">An application should use the *hsz1* parameter to add the service name to the list of servers available to the user.</span></span> <span data-ttu-id="5759c-127">Um aplicativo deve usar o parâmetro *hsz2* para identificar a instância do aplicativo iniciada.</span><span class="sxs-lookup"><span data-stu-id="5759c-127">An application should use the *hsz2* parameter to identify which application instance has started.</span></span>

## <a name="requirements"></a><span data-ttu-id="5759c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5759c-128">Requirements</span></span>



| <span data-ttu-id="5759c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5759c-129">Requirement</span></span> | <span data-ttu-id="5759c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5759c-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5759c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5759c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5759c-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5759c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5759c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5759c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5759c-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5759c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5759c-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5759c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5759c-136"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5759c-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5759c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5759c-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="5759c-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5759c-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5759c-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="5759c-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="5759c-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="5759c-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="5759c-141">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5759c-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5759c-142">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5759c-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

