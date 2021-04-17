---
description: Dite a autoridade do pacote de aplicativos.
ms.assetid: 047439EA-789B-41CF-87C2-66CFB3F20908
title: Constantes de SID do contêiner de aplicativo (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300b5ed110bbdc88d32efb76b20f5ec0f8454970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751610"
---
# <a name="app-container-sid-constants"></a><span data-ttu-id="d5b5e-103">Constantes de SID do contêiner de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d5b5e-103">App Container SID Constants</span></span>

<span data-ttu-id="d5b5e-104">As constantes de SID específicas do contêiner de aplicativo ditam a autoridade do pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d5b5e-104">The app container specific SID constants dictate the application package authority.</span></span> <span data-ttu-id="d5b5e-105">Embora um desenvolvedor possa usar essas constantes diretamente, a maioria dos desenvolvedores não precisa definir esses SIDs de contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5b5e-105">While a developer can use these constants directly, most developers do not need to define these app container SIDs.</span></span>

<dl> <span data-ttu-id="d5b5e-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**Segurança \_ do \_ \_ Autoridade do pacote de aplicativo** () Security {0,0,0,0,0,15} <span id="SECURITY_APP_PACKAGE_BASE_RID"></span> <span id="security_app_package_base_rid"></span> **\_ app \_ Package \_ base \_ RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span> <span id="security_builtin_app_package_rid_count"></span> **segurança \_ BuiltIn \_ app \_ pacote \_ RID \_ Count** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span> <span id="security_app_package_rid_count"></span> **segurança \_ app \_ Package pacote \_ RID \_ Count** (8L) segurança do <span id="SECURITY_CAPABILITY_BASE_RID"></span> <span id="security_capability_base_rid"></span> **recurso de segurança \_ \_ base \_ RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span> <span id="security_builtin_capability_rid_count"></span> **Security \_ BuiltIn \_ Capability \_ \_ contagem de RID** (2L) Security recurso de <span id="SECURITY_CAPABILITY_RID_COUNT"></span> <span id="security_capability_rid_count"></span> **segurança \_ \_ \_ contagem de RID** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span> <span id="security_builtin_package_any_package"></span> **Security \_ BuiltIn \_ Package \_ qualquer \_ pacote** (0x00000001l)</span><span class="sxs-lookup"><span data-stu-id="d5b5e-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**SECURITY\_APP\_PACKAGE\_AUTHORITY** ({0,0,0,0,0,15}) <span id="SECURITY_APP_PACKAGE_BASE_RID"></span><span id="security_app_package_base_rid"></span>**SECURITY\_APP\_PACKAGE\_BASE\_RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span><span id="security_builtin_app_package_rid_count"></span>**SECURITY\_BUILTIN\_APP\_PACKAGE\_RID\_COUNT** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span><span id="security_app_package_rid_count"></span>**SECURITY\_APP\_PACKAGE\_RID\_COUNT** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span><span id="security_capability_base_rid"></span>**SECURITY\_CAPABILITY\_BASE\_RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span><span id="security_builtin_capability_rid_count"></span>**SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT** (2L) <span id="SECURITY_CAPABILITY_RID_COUNT"></span><span id="security_capability_rid_count"></span>**SECURITY\_CAPABILITY\_RID\_COUNT** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span><span id="security_builtin_package_any_package"></span>**SECURITY\_BUILTIN\_PACKAGE\_ANY\_PACKAGE** (0x00000001L)</span></span>
</dl>

## <a name="requirements"></a><span data-ttu-id="d5b5e-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5b5e-107">Requirements</span></span>



| <span data-ttu-id="d5b5e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5b5e-108">Requirement</span></span> | <span data-ttu-id="d5b5e-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d5b5e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b5e-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5b5e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b5e-111">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d5b5e-111">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d5b5e-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5b5e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b5e-113">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d5b5e-113">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5b5e-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5b5e-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5b5e-115"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5b5e-115"><dt>Winnt.h</dt></span></span> </dl> |



 

 




