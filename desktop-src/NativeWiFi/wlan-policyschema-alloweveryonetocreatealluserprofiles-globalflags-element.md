---
description: Especifica se qualquer usuário pode criar um perfil de todos os usuários.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501560"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a><span data-ttu-id="04990-103">Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)</span><span class="sxs-lookup"><span data-stu-id="04990-103">allowEveryoneToCreateAllUserProfiles (globalFlags) Element</span></span>

<span data-ttu-id="04990-104">O elemento **allowEveryoneToCreateAllUserProfiles** (globalFlags) especifica se qualquer usuário pode criar um perfil de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="04990-104">The **allowEveryoneToCreateAllUserProfiles** (globalFlags) element specifies whether any user can create an all-user profile.</span></span> <span data-ttu-id="04990-105">Um perfil de todos os usuários pode ser usado por qualquer usuário no computador para se conectar à rede sem fio associada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="04990-105">An all-user profile can be used by any user on the machine to connect to the wireless network associated with the profile.</span></span>

<span data-ttu-id="04990-106">Se **allowEveryoneToCreateAllUserProfiles** for true, qualquer usuário poderá criar um perfil de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="04990-106">If **allowEveryoneToCreateAllUserProfiles** is TRUE, than any user can create an all-user profile.</span></span> <span data-ttu-id="04990-107">Se **allowEveryoneToCreateAllUserProfiles** for false, nem todos os usuários poderão criar um perfil de todos-usuários e haverá uma DACL associada ao \_ objeto de segurança WLAN Secure \_ Adicionar \_ novo \_ todos os \_ \_ perfis de usuário que especifica os usuários ou grupos de usuário com permissão para criar perfis de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="04990-107">If **allowEveryoneToCreateAllUserProfiles** is FALSE, then not all users can create an all-user profile, and there is a DACL associated with the wlan\_secure\_add\_new\_all\_user\_profiles security object that specifies the users or user groups with permission to create all-user profiles.</span></span> <span data-ttu-id="04990-108">A DACL padrão especifica que somente os usuários que fizeram logon como um membro do grupo Administradores podem criar um perfil de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="04990-108">The default DACL specifies that only users that are logged on as a member of the Administrators group can create an all-user profile.</span></span> <span data-ttu-id="04990-109">As configurações de segurança padrão podem ser alteradas chamando [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="04990-109">The default security settings can be changed by calling [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span></span> <span data-ttu-id="04990-110">Para obter as configurações de segurança atuais, chame [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="04990-110">To get the current security settings, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="04990-111">Esse elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="04990-111">This element is mandatory.</span></span> <span data-ttu-id="04990-112">Quando um perfil é criado pelo serviço de configuração automática, esse elemento terá o valor padrão de TRUE.</span><span class="sxs-lookup"><span data-stu-id="04990-112">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

<span data-ttu-id="04990-113">O elemento **allowEveryoneToCreateAllUserProfiles** é definido pelo elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="04990-113">The **allowEveryoneToCreateAllUserProfiles** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="04990-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04990-114">Requirements</span></span>



| <span data-ttu-id="04990-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="04990-115">Requirement</span></span> | <span data-ttu-id="04990-116">Valor</span><span class="sxs-lookup"><span data-stu-id="04990-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04990-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04990-117">Minimum supported client</span></span><br/> | <span data-ttu-id="04990-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04990-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04990-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04990-119">Minimum supported server</span></span><br/> | <span data-ttu-id="04990-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04990-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04990-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="04990-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="04990-122">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="04990-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="04990-123">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="04990-123">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="04990-124">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="04990-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="04990-125">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="04990-125">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




