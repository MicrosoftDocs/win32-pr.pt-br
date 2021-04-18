---
title: Constantes de sessão
description: As constantes de sessão na \_ \_ Enumeração WSManSessionFlags especificam a autenticação e outras informações para chamadas de WSMan. CreateSession ou IWSMan CreateSession que se conectam a um computador remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793826"
---
# <a name="session-constants"></a><span data-ttu-id="9e8db-103">Constantes de sessão</span><span class="sxs-lookup"><span data-stu-id="9e8db-103">Session Constants</span></span>

<span data-ttu-id="9e8db-104">As constantes de sessão na enumeração **\_ \_ WSManSessionFlags** especificam a autenticação e outras informações para as chamadas [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectam a um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="9e8db-104">The session constants in the **\_\_WSManSessionFlags** enumeration specify authentication and other information for [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span> <span data-ttu-id="9e8db-105">Essas constantes também estão fortemente relacionadas aos comutadores da ferramenta de linha de comando do **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="9e8db-105">These constants are also closely related to **Winrm** command-line tool switches.</span></span>

## <a name="using-session-constants"></a><span data-ttu-id="9e8db-106">Usando constantes de sessão</span><span class="sxs-lookup"><span data-stu-id="9e8db-106">Using Session Constants</span></span>

<span data-ttu-id="9e8db-107">Você pode definir os sinalizadores de sessão para a chamada para [**WSMan. CreateSession**](wsman-createsession.md) de duas maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="9e8db-107">You can set the Session flags for the call to [**WSMan.CreateSession**](wsman-createsession.md) in two different ways.</span></span> <span data-ttu-id="9e8db-108">Uma é mais curta e mais simples.</span><span class="sxs-lookup"><span data-stu-id="9e8db-108">One is shorter and simpler.</span></span> <span data-ttu-id="9e8db-109">A maneira mais longa, como é mostrado no exemplo a seguir, é localizar o valor do sinalizador que você deseja usar e criar uma constante em seu script com esse valor.</span><span class="sxs-lookup"><span data-stu-id="9e8db-109">The longer way, as is shown in the following example, is to locate the value of the flag you want to use and create a constant in your script with that value.</span></span> <span data-ttu-id="9e8db-110">Em seguida, a constante é usada para definir o valor do parâmetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="9e8db-110">Then the constant is used to set the value of the *iFlags* parameter.</span></span>

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

<span data-ttu-id="9e8db-111">A maneira recomendada, conforme mostrado no exemplo a seguir, é usar o método de objeto [**WSMan**](wsman.md) associado ao sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9e8db-111">The recommended way, as shown in the following example, is to use the [**WSMan**](wsman.md) object method associated with the flag.</span></span>

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span data-ttu-id="9e8db-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes de autenticação**](authentication-constants.md)</span><span class="sxs-lookup"><span data-stu-id="9e8db-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentication Constants**](authentication-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="9e8db-113">Especifique o método de autenticação e como lidar com servidores de certificado.</span><span class="sxs-lookup"><span data-stu-id="9e8db-113">Specify the authentication method and how to handle certificate servers.</span></span>

</dd> <dt>

<span data-ttu-id="9e8db-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Outras constantes de sessão**](other-session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="9e8db-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Other Session Constants**](other-session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="9e8db-115">Especifique a codificação, a criptografia e a porta do nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e8db-115">Specify the encoding, encryption, and service principal name port.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9e8db-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e8db-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e8db-117">Constantes e enumerações do WinRM</span><span class="sxs-lookup"><span data-stu-id="9e8db-117">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="9e8db-118">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="9e8db-118">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="9e8db-119">Autenticação para conexões remotas</span><span class="sxs-lookup"><span data-stu-id="9e8db-119">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> </dl>

 

 




