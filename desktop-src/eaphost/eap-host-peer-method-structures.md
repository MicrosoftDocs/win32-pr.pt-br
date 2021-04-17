---
title: Estruturas de método de par do EAPHost
description: Saiba mais sobre estruturas de API do método par do EAPHost, como EapCertificateCredential e EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105785047"
---
# <a name="eaphost-peer-method-structures"></a><span data-ttu-id="dc421-103">Estruturas de método de par do EAPHost</span><span class="sxs-lookup"><span data-stu-id="dc421-103">EAPHost Peer Method Structures</span></span>

<span data-ttu-id="dc421-104">As estruturas de API do método par do EAPHost são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="dc421-104">The EAPHost Peer Method API structures are as follows.</span></span>



| <span data-ttu-id="dc421-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="dc421-105">Structure</span></span>                                                              | <span data-ttu-id="dc421-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc421-106">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc421-107">**EapCertificateCredential**</span><span class="sxs-lookup"><span data-stu-id="dc421-107">**EapCertificateCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | <span data-ttu-id="dc421-108">Contém informações sobre o certificado que o método EAP usa para autenticação.</span><span class="sxs-lookup"><span data-stu-id="dc421-108">Contains information about the certificate that the EAP method uses for authentication.</span></span>                                                                                                            |
| [<span data-ttu-id="dc421-109">**EapCredential**</span><span class="sxs-lookup"><span data-stu-id="dc421-109">**EapCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | <span data-ttu-id="dc421-110">Contém informações sobre o tipo de credenciais e as credenciais apropriadas.</span><span class="sxs-lookup"><span data-stu-id="dc421-110">Contains information about the credentials type and the appropriate credentials.</span></span> <span data-ttu-id="dc421-111">Isso é passado como uma entrada para a API [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) .</span><span class="sxs-lookup"><span data-stu-id="dc421-111">This is passed as an input to the [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) API.</span></span> |
| [<span data-ttu-id="dc421-112">**\_ \_ rotinas do método EAP peer \_**</span><span class="sxs-lookup"><span data-stu-id="dc421-112">**EAP\_PEER\_METHOD\_ROUTINES**</span></span>](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | <span data-ttu-id="dc421-113">Contém um conjunto de ponteiros de função para as APIs do método de par do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dc421-113">Contains a set of function pointers to the EAPHost Peer Method APIs.</span></span>                                                                                                                               |
| [<span data-ttu-id="dc421-114">**EapPeerMethodOutput**</span><span class="sxs-lookup"><span data-stu-id="dc421-114">**EapPeerMethodOutput**</span></span>](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | <span data-ttu-id="dc421-115">Contém as informações de ação retornadas por um método de par EAP.</span><span class="sxs-lookup"><span data-stu-id="dc421-115">Contains the action information returned by an EAP peer method.</span></span>                                                                                                                                    |
| [<span data-ttu-id="dc421-116">**EapPeerMethodResult**</span><span class="sxs-lookup"><span data-stu-id="dc421-116">**EapPeerMethodResult**</span></span>](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | <span data-ttu-id="dc421-117">Contém dados de resultado gerados por um método EAP durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="dc421-117">Contains result data generated by an EAP method during authentication.</span></span>                                                                                                                             |
| [<span data-ttu-id="dc421-118">**EapSimCredential**</span><span class="sxs-lookup"><span data-stu-id="dc421-118">**EapSimCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | <span data-ttu-id="dc421-119">Contém informações sobre o SIM que é usado pelo método EAP para autenticação.</span><span class="sxs-lookup"><span data-stu-id="dc421-119">Contains information about the SIM that is used by the EAP method for authentication.</span></span>                                                                                                              |
| [<span data-ttu-id="dc421-120">**EapUsernamePasswordCredential**</span><span class="sxs-lookup"><span data-stu-id="dc421-120">**EapUsernamePasswordCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | <span data-ttu-id="dc421-121">Contém o nome de usuário e a senha que são usados pelo método EAP para autenticar o usuário.</span><span class="sxs-lookup"><span data-stu-id="dc421-121">Contains the username and password that is used by the EAP method for authenticating the user.</span></span>                                                                                                     |



 

 

 




