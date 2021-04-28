---
description: CPL_INQUIRE mensagem enviada à função CPlApplet de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.
title: Mensagem de CPL_INQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104464"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="fe7e9-103">CPL \_ mensagem de consulta</span><span class="sxs-lookup"><span data-stu-id="fe7e9-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="fe7e9-104">Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe7e9-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe7e9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe7e9-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="fe7e9-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="fe7e9-107">O número da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-107">The dialog box number.</span></span> <span data-ttu-id="fe7e9-108">Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="fe7e9-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="fe7e9-109">*lpcpli*</span><span class="sxs-lookup"><span data-stu-id="fe7e9-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="fe7e9-110">O endereço de uma estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) .</span><span class="sxs-lookup"><span data-stu-id="fe7e9-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="fe7e9-111">O aplicativo deve preencher essa estrutura com identificadores de recurso para o ícone, nome curto, descrição e qualquer valor definido pelo usuário associado à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe7e9-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fe7e9-112">Return value</span></span>

<span data-ttu-id="fe7e9-113">Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe7e9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe7e9-114">Remarks</span></span>

<span data-ttu-id="fe7e9-115">O painel de controle envia a mensagem de **\_ consulta de CPL** uma vez para cada caixa de diálogo com suporte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="fe7e9-116">O painel de controle também envia uma mensagem [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) para cada caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="fe7e9-117">Essas mensagens são enviadas imediatamente após a mensagem de [**\_ sqlcount do CPL**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="fe7e9-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="fe7e9-118">No entanto, o sistema não garante a ordem na qual as mensagens **CPL \_ inquire** e **CPL \_ NEWINQUIRE** são enviadas.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="fe7e9-119">Você pode executar a inicialização para a caixa de diálogo ao receber a **CPL de \_ consulta**.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="fe7e9-120">Se você precisar alocar memória, faça isso em resposta à mensagem [**CPL de \_ inicialização**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="fe7e9-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="fe7e9-121">A mensagem [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) retorna informações em um formato que o sistema não pode armazenar em cache.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="fe7e9-122">Por esse motivo, a maioria das funções [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve processar a **CPL de \_ consulta** e ignorar o **CPL \_ NEWINQUIRE**.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="fe7e9-123">Os únicos aplicativos que devem usar [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) são aqueles que precisam alterar seu ícone ou cadeias de caracteres de exibição com base no estado do computador.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="fe7e9-124">Nesse caso, o manipulador **de \_ consultas de CPL** deve especificar o \_ valor de res dinâmico CPL \_ para os membros **idIcon**, **idname** ou **IdInfo** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , em vez de especificar um identificador de recurso válido.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="fe7e9-125">Isso faz com que o painel de controle envie a mensagem **CPL \_ NEWINQUIRE** sempre que precisa do ícone e cadeias de caracteres de exibição, permitindo que você especifique informações com base no estado atual do computador.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="fe7e9-126">Isso é significativamente mais lento do que usar informações armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="fe7e9-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe7e9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe7e9-127">Requirements</span></span>



| <span data-ttu-id="fe7e9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe7e9-128">Requirement</span></span> | <span data-ttu-id="fe7e9-129">Valor</span><span class="sxs-lookup"><span data-stu-id="fe7e9-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fe7e9-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe7e9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fe7e9-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fe7e9-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fe7e9-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe7e9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fe7e9-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe7e9-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fe7e9-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe7e9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe7e9-135"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe7e9-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
