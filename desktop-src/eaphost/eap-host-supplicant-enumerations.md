---
title: Enumerações do suplicante EAPHost
description: Saiba mais sobre enumerações de API suplicante do EAPHost, como EapHostPeerMethodResultReason e estado de isolamento \_ .
ms.assetid: ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e214682a9b94c98db5981a0df8c2b8619814f1e5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823978"
---
# <a name="eaphost-supplicant-enumerations"></a><span data-ttu-id="2a957-103">Enumerações do suplicante EAPHost</span><span class="sxs-lookup"><span data-stu-id="2a957-103">EAPHost Supplicant Enumerations</span></span>

<span data-ttu-id="2a957-104">As enumerações de API suplicante do EAPHost são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="2a957-104">The EAPHost Supplicant API enumerations are as follows.</span></span>



| <span data-ttu-id="2a957-105">Enumeração</span><span class="sxs-lookup"><span data-stu-id="2a957-105">Enumeration</span></span>                                                                  | <span data-ttu-id="2a957-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a957-106">Description</span></span>                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a957-107">**\_tipo de \_ dados de interface do usuário interativa EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2a957-107">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)     | <span data-ttu-id="2a957-108">Especifica o conjunto de tipos de dados de contexto de interface do usuário interativa fornecidos para determinadas chamadas à API do suplicante.</span><span class="sxs-lookup"><span data-stu-id="2a957-108">Specifies the set of types of interactive user interface context data supplied to certain supplicant API calls.</span></span>    |
| [<span data-ttu-id="2a957-109">**\_tipo de \_ Propriedade do método EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2a957-109">**EAP\_METHOD\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_type)              | <span data-ttu-id="2a957-110">Windows 7 ou posterior: especifica o tipo de Propriedade do método.</span><span class="sxs-lookup"><span data-stu-id="2a957-110">Windows 7 or later: Specifies the method property type.</span></span>                                                            |
| [<span data-ttu-id="2a957-111">**\_tipo de \_ valor da Propriedade do método EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2a957-111">**EAP\_METHOD\_PROPERTY\_VALUE\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_value_type) | <span data-ttu-id="2a957-112">Windows 7 ou posterior: especifica o tipo de dados de um valor de propriedade de método.</span><span class="sxs-lookup"><span data-stu-id="2a957-112">Windows 7 or later: Specifies the data type of a method property value.</span></span>                                            |
| [<span data-ttu-id="2a957-113">**\_status de autenticação do EAPHost \_**</span><span class="sxs-lookup"><span data-stu-id="2a957-113">**EAPHOST\_AUTH\_STATUS**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphost_auth_status)                         | <span data-ttu-id="2a957-114">Define o conjunto de valores de status de sessão de autenticação EAP possíveis.</span><span class="sxs-lookup"><span data-stu-id="2a957-114">Defines the set of possible EAP authentication session status values.</span></span>                                              |
| [<span data-ttu-id="2a957-115">**EapHostPeerAuthParams**</span><span class="sxs-lookup"><span data-stu-id="2a957-115">**EapHostPeerAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)                       | <span data-ttu-id="2a957-116">Define o conjunto de possíveis valores de parâmetro de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2a957-116">Defines the set of possible authentication parameter values.</span></span>                                                       |
| [<span data-ttu-id="2a957-117">**EapHostPeerMethodResultReason**</span><span class="sxs-lookup"><span data-stu-id="2a957-117">**EapHostPeerMethodResultReason**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)       | <span data-ttu-id="2a957-118">Define o conjunto de possíveis motivos que descrevem os resultados retornados por um método EAP para um suplicante.</span><span class="sxs-lookup"><span data-stu-id="2a957-118">Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.</span></span>           |
| [<span data-ttu-id="2a957-119">**EapHostPeerResponseAction**</span><span class="sxs-lookup"><span data-stu-id="2a957-119">**EapHostPeerResponseAction**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)               | <span data-ttu-id="2a957-120">Define o conjunto de ações que um autenticador EAP ou método par pode indicar a um suplicante durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="2a957-120">Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.</span></span> |
| [<span data-ttu-id="2a957-121">**Estado de isolamento \_**</span><span class="sxs-lookup"><span data-stu-id="2a957-121">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)                                  | <span data-ttu-id="2a957-122">Define o conjunto de possíveis valores de status de isolamento de um computador.</span><span class="sxs-lookup"><span data-stu-id="2a957-122">Defines the set of possible isolation status values of a machine.</span></span>                                                  |



 

 

 




