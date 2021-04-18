---
description: Especifica o tipo de credenciais usadas para autenticação.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Elemento AuthMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760233"
---
# <a name="authmode-onex-element"></a><span data-ttu-id="3a8b0-103">Elemento AuthMode (OneX)</span><span class="sxs-lookup"><span data-stu-id="3a8b0-103">authMode (OneX) Element</span></span>

<span data-ttu-id="3a8b0-104">O elemento AuthMode (OneX) especifica o tipo de credenciais usadas para autenticação.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-104">The authMode (OneX) element specifies the type of credentials used for authentication.</span></span> <span data-ttu-id="3a8b0-105">A tabela a seguir descreve os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="3a8b0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="3a8b0-106">Value</span></span>         | <span data-ttu-id="3a8b0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a8b0-107">Description</span></span>                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8b0-108">machineOrUser</span><span class="sxs-lookup"><span data-stu-id="3a8b0-108">machineOrUser</span></span> | <span data-ttu-id="3a8b0-109">Use as credenciais do computador ou do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-109">Use machine or user credentials.</span></span> <span data-ttu-id="3a8b0-110">Quando um usuário faz logon, as credenciais do usuário são usadas para autenticação.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-110">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="3a8b0-111">Quando nenhum usuário está conectado, as credenciais do computador são usadas.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-111">When no user is logged on, machine credentials are used.</span></span> |
| <span data-ttu-id="3a8b0-112">computador</span><span class="sxs-lookup"><span data-stu-id="3a8b0-112">machine</span></span>       | <span data-ttu-id="3a8b0-113">Use somente as credenciais do computador.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-113">Use machine credentials only.</span></span>                                                                                                                                           |
| <span data-ttu-id="3a8b0-114">usuário</span><span class="sxs-lookup"><span data-stu-id="3a8b0-114">user</span></span>          | <span data-ttu-id="3a8b0-115">Usar somente as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-115">Use user credentials only.</span></span>                                                                                                                                              |
| <span data-ttu-id="3a8b0-116">guest</span><span class="sxs-lookup"><span data-stu-id="3a8b0-116">guest</span></span>         | <span data-ttu-id="3a8b0-117">Use somente credenciais de convidado (vazias).</span><span class="sxs-lookup"><span data-stu-id="3a8b0-117">Use guest (empty) credentials only.</span></span>                                                                                                                                     |



 

<span data-ttu-id="3a8b0-118">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-118">This element is optional.</span></span> <span data-ttu-id="3a8b0-119">Quando AuthMode não é especificado em um perfil, é usado um valor de `machineOrUser` .</span><span class="sxs-lookup"><span data-stu-id="3a8b0-119">When authMode is not specified in a profile, a value of `machineOrUser` is used.</span></span>

<span data-ttu-id="3a8b0-120">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="3a8b0-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="3a8b0-121">O elemento **AuthMode** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3a8b0-121">The **authMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a8b0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a8b0-122">Remarks</span></span>

<span data-ttu-id="3a8b0-123">Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="3a8b0-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="3a8b0-124">Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="3a8b0-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a8b0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a8b0-125">Requirements</span></span>



| <span data-ttu-id="3a8b0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a8b0-126">Requirement</span></span> | <span data-ttu-id="3a8b0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3a8b0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a8b0-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a8b0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a8b0-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a8b0-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a8b0-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a8b0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a8b0-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a8b0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a8b0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a8b0-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a8b0-133">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="3a8b0-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3a8b0-134">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="3a8b0-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="3a8b0-135">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="3a8b0-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3a8b0-136">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="3a8b0-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
