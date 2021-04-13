---
title: Elemento Server (sendEmailType)
description: Contém o servidor de email usado para enviar a mensagem de email.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Elemento de servidor Agendador de Tarefas
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369335"
---
# <a name="server-sendemailtype-element"></a><span data-ttu-id="e411b-104">Elemento Server (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="e411b-104">Server (sendEmailType) Element</span></span>

<span data-ttu-id="e411b-105">Contém o servidor de email usado para enviar a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e411b-105">Contains the email server used to send the email message.</span></span>

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

<span data-ttu-id="e411b-106">O elemento **Server** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e411b-106">The **Server** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e411b-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e411b-107">Parent element</span></span>



| <span data-ttu-id="e411b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e411b-108">Element</span></span>                                                                              | <span data-ttu-id="e411b-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e411b-109">Derived from</span></span>                                                           | <span data-ttu-id="e411b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e411b-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e411b-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="e411b-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="e411b-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="e411b-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="e411b-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e411b-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e411b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e411b-114">Remarks</span></span>

<span data-ttu-id="e411b-115">Para desenvolvimento em C++, consulte [**Propriedade Server de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span><span class="sxs-lookup"><span data-stu-id="e411b-115">For C++ development, see [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span></span>

<span data-ttu-id="e411b-116">Para desenvolvimento de script, consulte [**emailaction. Server**](emailaction-server.md).</span><span class="sxs-lookup"><span data-stu-id="e411b-116">For script development, see [**EmailAction.Server**](emailaction-server.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e411b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e411b-117">Requirements</span></span>



| <span data-ttu-id="e411b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e411b-118">Requirement</span></span> | <span data-ttu-id="e411b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e411b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e411b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e411b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e411b-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e411b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e411b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e411b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e411b-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e411b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





