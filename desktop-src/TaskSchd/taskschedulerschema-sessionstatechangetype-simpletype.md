---
title: Tipo simples de sessionStateChangeType
description: Define valores para o tipo de Terminal Server alteração de estado de sessão que você pode usar para disparar uma tarefa a ser iniciada.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Agendador de Tarefas tipo simples de sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455700"
---
# <a name="sessionstatechangetype-simple-type"></a><span data-ttu-id="c1841-104">Tipo simples de sessionStateChangeType</span><span class="sxs-lookup"><span data-stu-id="c1841-104">sessionStateChangeType Simple Type</span></span>

<span data-ttu-id="c1841-105">Define valores para o tipo de Terminal Server alteração de estado de sessão que você pode usar para disparar uma tarefa a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="c1841-105">Defines values for the kind of Terminal Server session state change you can use to trigger a task to start.</span></span>

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="c1841-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="c1841-106">Enumeration values</span></span>

<span data-ttu-id="c1841-107">O tipo simples **sessionStateChangeType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1841-107">The **sessionStateChangeType** simple type defines the following values.</span></span>



| <span data-ttu-id="c1841-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c1841-108">Value</span></span>             | <span data-ttu-id="c1841-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1841-109">Description</span></span>                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1841-110">ConsoleConnect</span><span class="sxs-lookup"><span data-stu-id="c1841-110">ConsoleConnect</span></span>    | <span data-ttu-id="c1841-111">Terminal Server alteração de estado da conexão do console.</span><span class="sxs-lookup"><span data-stu-id="c1841-111">Terminal Server console connection state change.</span></span> <span data-ttu-id="c1841-112">Por exemplo, quando você se conecta a uma sessão de usuário no computador local, alternando os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="c1841-112">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                            |
| <span data-ttu-id="c1841-113">ConsoleDisconnect</span><span class="sxs-lookup"><span data-stu-id="c1841-113">ConsoleDisconnect</span></span> | <span data-ttu-id="c1841-114">Alteração do estado de desconexão do Console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="c1841-114">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="c1841-115">Por exemplo, quando você se desconecta a uma sessão de usuário no computador local, alternando os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="c1841-115">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span> <br/>                      |
| <span data-ttu-id="c1841-116">RemoteConnect</span><span class="sxs-lookup"><span data-stu-id="c1841-116">RemoteConnect</span></span>     | <span data-ttu-id="c1841-117">Terminal Server alteração de estado da conexão remota.</span><span class="sxs-lookup"><span data-stu-id="c1841-117">Terminal Server remote connection state change.</span></span> <span data-ttu-id="c1841-118">Por exemplo, quando um usuário se conecta a uma sessão de usuário usando o programa Conexão de Área de Trabalho Remota de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="c1841-118">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span> <br/>            |
| <span data-ttu-id="c1841-119">RemoteDisconnect</span><span class="sxs-lookup"><span data-stu-id="c1841-119">RemoteDisconnect</span></span>  | <span data-ttu-id="c1841-120">Terminal Server alteração de estado de desconexão remota.</span><span class="sxs-lookup"><span data-stu-id="c1841-120">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="c1841-121">Por exemplo, quando um usuário se desconecta de uma sessão de usuário enquanto usa o programa de Conexão de Área de Trabalho Remota de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="c1841-121">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span> <br/> |
| <span data-ttu-id="c1841-122">SessionLock</span><span class="sxs-lookup"><span data-stu-id="c1841-122">SessionLock</span></span>       | <span data-ttu-id="c1841-123">Alteração de estado bloqueado da sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="c1841-123">Terminal Server session locked state change.</span></span> <span data-ttu-id="c1841-124">Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c1841-124">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                       |
| <span data-ttu-id="c1841-125">SessionUnlock</span><span class="sxs-lookup"><span data-stu-id="c1841-125">SessionUnlock</span></span>     | <span data-ttu-id="c1841-126">Alteração de estado desbloqueado da sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="c1841-126">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="c1841-127">Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="c1841-127">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                    |



## <a name="requirements"></a><span data-ttu-id="c1841-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1841-128">Requirements</span></span>



| <span data-ttu-id="c1841-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1841-129">Requirement</span></span> | <span data-ttu-id="c1841-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c1841-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1841-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1841-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c1841-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1841-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1841-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1841-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c1841-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1841-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





