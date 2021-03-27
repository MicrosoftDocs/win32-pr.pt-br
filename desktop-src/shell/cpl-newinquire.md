---
description: Enviado para a função CPlApplet de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.
title: Mensagem de CPL_NEWINQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967349"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="9e6ea-103">CPL \_ mensagem NEWINQUIRE</span><span class="sxs-lookup"><span data-stu-id="9e6ea-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="9e6ea-104">Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e6ea-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e6ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e6ea-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="9e6ea-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="9e6ea-107">O número da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-107">The dialog box number.</span></span> <span data-ttu-id="9e6ea-108">Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="9e6ea-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="9e6ea-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="9e6ea-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="9e6ea-110">O endereço de uma estrutura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9e6ea-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="9e6ea-111">O aplicativo do painel de controle deve preencher essa estrutura com informações sobre a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e6ea-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e6ea-112">Return value</span></span>

<span data-ttu-id="9e6ea-113">Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6ea-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e6ea-114">Remarks</span></span>

<span data-ttu-id="9e6ea-115">Para melhorar o desempenho, a maioria dos aplicativos deve ignorar o **CPL \_ NEWINQUIRE** e processar a mensagem de [**\_ consulta do CPL**](cpl-inquire.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6ea-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="9e6ea-116">O painel de controle envia a mensagem **CPL \_ NEWINQUIRE** uma vez para cada caixa de diálogo com suporte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="9e6ea-117">O painel de controle também envia uma mensagem de [**\_ consulta de CPL**](cpl-inquire.md) para cada caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="9e6ea-118">Essas mensagens são enviadas imediatamente após a mensagem de [**\_ sqlcount do CPL**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6ea-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="9e6ea-119">No entanto, o sistema não garante a ordem na qual as mensagens **CPL \_ inquire** e **CPL \_ NEWINQUIRE** são enviadas.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="9e6ea-120">Você pode executar a inicialização para a caixa de diálogo ao receber a [**CPL de \_ consulta**](cpl-inquire.md).</span><span class="sxs-lookup"><span data-stu-id="9e6ea-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="9e6ea-121">Se você precisar alocar memória, faça isso em resposta à mensagem [**CPL de \_ inicialização**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="9e6ea-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="9e6ea-122">[**CPL \_ A consulta**](cpl-inquire.md) é a mensagem preferida.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="9e6ea-123">Isso ocorre porque o **CPL \_ NEWINQUIRE** retorna informações em um formato que o sistema não pode armazenar em cache.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="9e6ea-124">Consequentemente, os aplicativos que process **CPL \_ NEWINQUIRE** devem ser carregados cada vez que o painel de controle precisar das informações, resultando em uma redução significativa no desempenho.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="9e6ea-125">Os únicos aplicativos que devem usar **CPL \_ NEWINQUIRE** são aqueles que precisam alterar seu ícone ou cadeias de caracteres de exibição com base no estado do computador.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="9e6ea-126">Nesse caso, o manipulador [**de \_ consultas de CPL**](cpl-inquire.md) deve especificar o \_ valor de res dinâmico CPL \_ para os membros **idIcon**, **idname** ou **IdInfo** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , em vez de especificar um identificador de recurso válido.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="9e6ea-127">Isso faz com que o painel de controle envie a mensagem **CPL \_ NEWINQUIRE** sempre que precisa do ícone e cadeias de caracteres de exibição, permitindo que você especifique informações com base no estado atual do computador.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="9e6ea-128">É claro que isso é significativamente mais lento do que o uso de informações armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6ea-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e6ea-129">Requirements</span></span>



| <span data-ttu-id="9e6ea-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e6ea-130">Requirement</span></span> | <span data-ttu-id="9e6ea-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9e6ea-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9e6ea-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e6ea-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6ea-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9e6ea-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9e6ea-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e6ea-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6ea-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e6ea-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9e6ea-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9e6ea-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e6ea-137"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e6ea-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
