---
title: Tipo simples de Logontype
description: Define os valores possíveis do elemento Logontype.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- tipo simples de Logontype Agendador de Tarefas
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086067"
---
# <a name="logontype-simple-type"></a><span data-ttu-id="b0245-104">Tipo simples de Logontype</span><span class="sxs-lookup"><span data-stu-id="b0245-104">logonType Simple Type</span></span>

<span data-ttu-id="b0245-105">Define os valores possíveis do elemento [**Logontype**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b0245-105">Defines the possible values of the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="b0245-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="b0245-106">Enumeration values</span></span>

<span data-ttu-id="b0245-107">O tipo simples de **Logontype** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0245-107">The **logonType** simple type defines the following values.</span></span>



| <span data-ttu-id="b0245-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b0245-108">Value</span></span>                      | <span data-ttu-id="b0245-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0245-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0245-110">S4U</span><span class="sxs-lookup"><span data-stu-id="b0245-110">S4U</span></span>                        | <span data-ttu-id="b0245-111">O usuário deve fazer logon usando um logon S4U (serviço para usuário).</span><span class="sxs-lookup"><span data-stu-id="b0245-111">User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="b0245-112">Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.</span><span class="sxs-lookup"><span data-stu-id="b0245-112">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="b0245-113">Senha</span><span class="sxs-lookup"><span data-stu-id="b0245-113">Password</span></span>                   | <span data-ttu-id="b0245-114">O usuário deve fazer logon usando uma senha.</span><span class="sxs-lookup"><span data-stu-id="b0245-114">User must log on using a password.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b0245-115">InteractiveToken</span><span class="sxs-lookup"><span data-stu-id="b0245-115">InteractiveToken</span></span>           | <span data-ttu-id="b0245-116">O usuário já deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="b0245-116">User must already be logged on.</span></span> <span data-ttu-id="b0245-117">A tarefa será executada somente em uma sessão interativa existente.</span><span class="sxs-lookup"><span data-stu-id="b0245-117">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b0245-118">InteractiveTokenOrPassword</span><span class="sxs-lookup"><span data-stu-id="b0245-118">InteractiveTokenOrPassword</span></span> | <span data-ttu-id="b0245-119">Não está mais em uso; atualmente idêntica à senha.</span><span class="sxs-lookup"><span data-stu-id="b0245-119">No longer in use; currently identical to Password.</span></span><br/> <span data-ttu-id="b0245-120">**Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista e Windows server 2008:** A tarefa será executada em uma sessão interativa existente ou o usuário deverá fazer logon usando uma senha.</span><span class="sxs-lookup"><span data-stu-id="b0245-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:** The task will be run in an existing interactive session or the user must log on using a password.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b0245-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0245-121">Requirements</span></span>



| <span data-ttu-id="b0245-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0245-122">Requirement</span></span> | <span data-ttu-id="b0245-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b0245-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0245-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0245-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0245-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0245-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b0245-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0245-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0245-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0245-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0245-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0245-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0245-129">Tipos simples de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b0245-129">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b0245-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b0245-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





