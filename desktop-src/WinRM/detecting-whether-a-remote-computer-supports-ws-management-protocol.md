---
title: Detectando se um computador remoto dá suporte ao protocolo WS-Management
description: Você pode usar os métodos Session. Identify ou IWSManSession. Identify para determinar se o computador remoto tem um serviço que dá suporte ao protocolo WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810865"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a><span data-ttu-id="d61e4-103">Detectando se um computador remoto dá suporte ao protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="d61e4-103">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>

<span data-ttu-id="d61e4-104">Você pode usar os métodos [**Session. Identify**](session-identify.md) ou [**IWSManSession. Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) para determinar se o computador remoto tem um serviço que dá suporte ao protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="d61e4-104">You can use the [**Session.Identify**](session-identify.md) or [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) methods to determine if the remote computer has a service that supports the WS-Management protocol.</span></span>

<span data-ttu-id="d61e4-105">Se um serviço de protocolo WS-Management estiver configurado no computador remoto e estiver ouvindo solicitações, o serviço poderá detectar uma solicitação de identificação pelo seguinte XML no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d61e4-105">If a WS-Management protocol service is configured on the remote computer and is listening for requests, the service can detect an Identify request by the following XML in the header.</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



<span data-ttu-id="d61e4-106">O serviço de protocolo WS-Management que recebe a solicitação retorna as informações contidas na lista a seguir, no corpo da mensagem:</span><span class="sxs-lookup"><span data-stu-id="d61e4-106">The WS-Management protocol service that receives the request returns the information, contained in the following list, in the body of the message:</span></span>

-   <span data-ttu-id="d61e4-107">A versão do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="d61e4-107">The WS-Management protocol version.</span></span> <span data-ttu-id="d61e4-108">Por exemplo, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span><span class="sxs-lookup"><span data-stu-id="d61e4-108">For example, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span></span>
-   <span data-ttu-id="d61e4-109">O fornecedor do produto, por exemplo, "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="d61e4-109">The product vendor, for example, "Microsoft Corporation".</span></span>
-   <span data-ttu-id="d61e4-110">A versão do produto.</span><span class="sxs-lookup"><span data-stu-id="d61e4-110">The product version.</span></span> <span data-ttu-id="d61e4-111">Se a solicitação for enviada com **WSManFlagUseNoAuthentication** no parâmetro *flags* , nenhuma informação de versão do produto será retornada.</span><span class="sxs-lookup"><span data-stu-id="d61e4-111">If the request is sent with **WSManFlagUseNoAuthentication** in the *flags* parameter, then no product version information is returned.</span></span> <span data-ttu-id="d61e4-112">Se a solicitação for enviada com a autenticação padrão em vigor ou com outro modo de autenticação especificado, as informações de versão do produto poderão ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="d61e4-112">If the request is sent with either the default authentication in effect or with another authentication mode specified, then the product version information can be returned.</span></span>

<span data-ttu-id="d61e4-113">A solicitação para detectar se o computador remoto tem um serviço de protocolo configurado e de escuta WS-Management pode ser executado no início de um script com outras operações.</span><span class="sxs-lookup"><span data-stu-id="d61e4-113">The request to detect whether the remote computer has a configured and listening WS-Management protocol service can be performed at the beginning of a script with other operations.</span></span> <span data-ttu-id="d61e4-114">Isso verificará se o computador de destino ou os computadores podem responder a outras solicitações de protocolo de WS-Management.</span><span class="sxs-lookup"><span data-stu-id="d61e4-114">This will verify that the target computer or computers can respond to further WS-Management protocol requests.</span></span> <span data-ttu-id="d61e4-115">A verificação também pode ser feita em um script separado.</span><span class="sxs-lookup"><span data-stu-id="d61e4-115">The verification also can be done in a separate script.</span></span>

<span data-ttu-id="d61e4-116">**Para detectar um serviço de protocolo WS-Management**</span><span class="sxs-lookup"><span data-stu-id="d61e4-116">**To detect a WS-Management protocol service**</span></span>

1.  <span data-ttu-id="d61e4-117">Crie um objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="d61e4-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="d61e4-118">Determine se a solicitação deve ser enviada autenticada ou não autenticada e defina o parâmetro *flags* adequadamente na chamada para [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="d61e4-118">Determine whether the request should be sent authenticated or unauthenticated and set the *flags* parameter accordingly in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  <span data-ttu-id="d61e4-119">Chame [**Session. Identify**](session-identify.md).</span><span class="sxs-lookup"><span data-stu-id="d61e4-119">Call [**Session.Identify**](session-identify.md).</span></span>

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a><span data-ttu-id="d61e4-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d61e4-120">Examples</span></span>

<span data-ttu-id="d61e4-121">O exemplo de código VBScript a seguir envia uma solicitação de identificação não autenticada para o computador remoto chamado "Remote1" no mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="d61e4-121">The following VBScript code example sends an unauthenticated Identify request to the remote computer named "Remote1" in the same domain.</span></span>


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



<span data-ttu-id="d61e4-122">A resposta a seguir mostra o XML retornado pelo computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d61e4-122">The following response shows the XML returned by the remote computer.</span></span> <span data-ttu-id="d61e4-123">A versão do protocolo de WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") e o fornecedor do sistema operacional ("Microsoft Corporation") são especificados no XML retornado.</span><span class="sxs-lookup"><span data-stu-id="d61e4-123">The WS-Management protocol version ("https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd") and the operating system vendor ("Microsoft Corporation") are specified in the returned XML.</span></span> <span data-ttu-id="d61e4-124">Como a mensagem é enviada não autenticada, a versão do produto não é retornada pelo serviço de Gerenciamento Remoto do Windows.</span><span class="sxs-lookup"><span data-stu-id="d61e4-124">Because the message is sent unauthenticated, the product version is not returned by the Windows Remote Management service.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



<span data-ttu-id="d61e4-125">O exemplo de código VBScript a seguir envia uma solicitação de identificação autenticada para o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d61e4-125">The following VBScript code example sends an authenticated Identify request to the remote computer.</span></span>


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



<span data-ttu-id="d61e4-126">Como a solicitação foi enviada com a autenticação, as informações de versão são retornadas.</span><span class="sxs-lookup"><span data-stu-id="d61e4-126">Because the request was sent with authentication, the version information is returned.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a><span data-ttu-id="d61e4-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d61e4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d61e4-128">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="d61e4-128">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="d61e4-129">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="d61e4-129">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="d61e4-130">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="d61e4-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




