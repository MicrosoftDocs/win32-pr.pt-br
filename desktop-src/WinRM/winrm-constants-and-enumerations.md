---
title: Constantes e enumerações do WinRM
description: Gerenciamento Remoto do Windows tem sinalizadores de bits usados na criação de sessões e enumerações, e para tipos de acesso e autenticação para um servidor proxy.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0789d440ff0f88cc037e0dc9e544ca559c1af5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005821"
---
# <a name="winrm-constants-and-enumerations"></a><span data-ttu-id="06754-103">Constantes e enumerações do WinRM</span><span class="sxs-lookup"><span data-stu-id="06754-103">WinRM Constants and Enumerations</span></span>

<span data-ttu-id="06754-104">Gerenciamento Remoto do Windows tem sinalizadores de bits usados na criação de sessões e enumerações, e para tipos de acesso e autenticação para um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="06754-104">Windows Remote Management has bit flags used in creating sessions and enumerations, and for access types and authentication to a proxy server.</span></span> <span data-ttu-id="06754-105">A lista a seguir lista os diferentes sinalizadores de bits.</span><span class="sxs-lookup"><span data-stu-id="06754-105">The following list lists the different bit flags.</span></span>

<dl> <dt>

<span data-ttu-id="06754-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Constantes de sessão](session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="06754-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Session Constants](session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="06754-107">Sinalizadores usados no parâmetro *flags* dos métodos [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) .</span><span class="sxs-lookup"><span data-stu-id="06754-107">Flags used in *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) methods.</span></span>

</dd> <dt>

<span data-ttu-id="06754-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Constantes de enumeração**](enumeration-constants.md)</span><span class="sxs-lookup"><span data-stu-id="06754-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumeration Constants**](enumeration-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="06754-109">Sinalizadores usados no parâmetro *flags* de chamada para [**Session. Enumerate**](session-enumerate.md) ou [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="06754-109">Flags used in *flags* parameter of call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="06754-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span><span class="sxs-lookup"><span data-stu-id="06754-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span></span>
</dt> <dd>

<span data-ttu-id="06754-111">Sinalizadores usados no parâmetro *authenticationMechanism* da chamada para [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span><span class="sxs-lookup"><span data-stu-id="06754-111">Flags used in *authenticationMechanism* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> <dt>

<span data-ttu-id="06754-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span><span class="sxs-lookup"><span data-stu-id="06754-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span></span>
</dt> <dd>

<span data-ttu-id="06754-113">Sinalizadores usados no parâmetro *accessType* de chamada para [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span><span class="sxs-lookup"><span data-stu-id="06754-113">Flags used in *accessType* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="06754-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06754-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06754-115">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="06754-115">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="06754-116">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="06754-116">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="06754-117">**IWSMan:: CreateSession**</span><span class="sxs-lookup"><span data-stu-id="06754-117">**IWSMan::CreateSession**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[<span data-ttu-id="06754-118">**IWSManConnectionOptionsEx2:: SetProxy**</span><span class="sxs-lookup"><span data-stu-id="06754-118">**IWSManConnectionOptionsEx2::SetProxy**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




