---
description: Inclui configurações possíveis para a política de logon automático.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Enumeração WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782576"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a><span data-ttu-id="4a1a1-103">Enumeração WinHttpRequestAutoLogonPolicy</span><span class="sxs-lookup"><span data-stu-id="4a1a1-103">WinHttpRequestAutoLogonPolicy enumeration</span></span>

<span data-ttu-id="4a1a1-104">A enumeração **WinHttpRequestAutoLogonPolicy** inclui possíveis configurações para a [política de logon automática](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="4a1a1-104">The **WinHttpRequestAutoLogonPolicy** enumeration includes possible settings for the [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a1a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a1a1-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a><span data-ttu-id="4a1a1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="4a1a1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4a1a1-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ sempre**</span><span class="sxs-lookup"><span data-stu-id="4a1a1-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy\_Always**</span></span>
</dt> <dd>

<span data-ttu-id="4a1a1-108">Um logon autenticado, usando as credenciais padrão, é executado para todas as solicitações.</span><span class="sxs-lookup"><span data-stu-id="4a1a1-108">An authenticated log on, using the default credentials, is performed for all requests.</span></span>

</dd> <dt>

<span data-ttu-id="4a1a1-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**</span><span class="sxs-lookup"><span data-stu-id="4a1a1-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy\_OnlyIfBypassProxy**</span></span>
</dt> <dd>

<span data-ttu-id="4a1a1-110">Um logon autenticado, usando as credenciais padrão, é executado somente para solicitações na intranet local.</span><span class="sxs-lookup"><span data-stu-id="4a1a1-110">An authenticated log on, using the default credentials, is performed only for requests on the local intranet.</span></span> <span data-ttu-id="4a1a1-111">A intranet local é considerada como qualquer servidor na lista de bypass de proxy na configuração de proxy atual.</span><span class="sxs-lookup"><span data-stu-id="4a1a1-111">The local intranet is considered to be any server on the proxy bypass list in the current proxy configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4a1a1-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ nunca**</span><span class="sxs-lookup"><span data-stu-id="4a1a1-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy\_Never**</span></span>
</dt> <dd>

<span data-ttu-id="4a1a1-113">A autenticação não é usada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4a1a1-113">Authentication is not used automatically.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a1a1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a1a1-114">Remarks</span></span>

<span data-ttu-id="4a1a1-115">Para definir a política de logon automático, chame o método [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) e especifique uma das constantes anteriores.</span><span class="sxs-lookup"><span data-stu-id="4a1a1-115">To set the automatic logon policy, call the [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) method and specify one of the preceding constants.</span></span>

> [!Note]  
> <span data-ttu-id="4a1a1-116">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4a1a1-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a1a1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a1a1-117">Requirements</span></span>



| <span data-ttu-id="4a1a1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a1a1-118">Requirement</span></span> | <span data-ttu-id="4a1a1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4a1a1-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1a1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a1a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a1a1-121">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="4a1a1-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4a1a1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a1a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a1a1-123">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="4a1a1-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4a1a1-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4a1a1-124">Redistributable</span></span><br/>          | <span data-ttu-id="4a1a1-125">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4a1a1-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4a1a1-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="4a1a1-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a1a1-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a1a1-127"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a1a1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a1a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1a1-129">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4a1a1-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




