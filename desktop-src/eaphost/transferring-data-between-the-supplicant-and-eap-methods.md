---
title: Transferindo dados entre os métodos suplicante e EAP
description: Saiba mais sobre como transferir dados entre os métodos suplicante e EAP. A transferência de dados entre métodos é realizada usando atributos de EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366723"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a><span data-ttu-id="0c0ab-104">Transferindo dados entre os métodos suplicante e EAP</span><span class="sxs-lookup"><span data-stu-id="0c0ab-104">Transferring Data Between the Supplicant and EAP Methods</span></span>

<span data-ttu-id="0c0ab-105">O uso de atributos de EAP permite que os dados sejam trocados entre suplicantes e métodos EAP.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-105">Using EAP attributes allows data to be exchanged between supplicants and EAP methods.</span></span>

## <a name="attribute-consumption"></a><span data-ttu-id="0c0ab-106">Consumo de atributo</span><span class="sxs-lookup"><span data-stu-id="0c0ab-106">Attribute Consumption</span></span>

<span data-ttu-id="0c0ab-107">O [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) CONSOME atributos EAP que são passados diretamente para o método EAP configurado.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consumes EAP attributes that are passed directly to the configured EAP method.</span></span> <span data-ttu-id="0c0ab-108">Da mesma forma, os métodos EAP são livres para retornar um código de ação que indica ao suplicante que os atributos estão disponíveis e que ele deve coletar os atributos usando [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="0c0ab-108">Similarly, EAP methods are free to return an action code that indicates to the supplicant that attributes are available and that it should collect the attributes using [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span></span>

<span data-ttu-id="0c0ab-109">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-109">For more information, see the following topics.</span></span>

-   <span data-ttu-id="0c0ab-110">[Códigos de ação suplicante de peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="0c0ab-110">[EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="0c0ab-111">[Códigos de motivo suplicante de peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span><span class="sxs-lookup"><span data-stu-id="0c0ab-111">[EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span></span>
-   <span data-ttu-id="0c0ab-112">[Códigos de ação do método de autenticador EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span><span class="sxs-lookup"><span data-stu-id="0c0ab-112">[EAP Authenticator Method Action Codes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span></span>

<span data-ttu-id="0c0ab-113">Os suplicantes são esperados para ignorar atributos que não reconhecem ou que não podem agir.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-113">Supplicants are expected to ignore attributes that they do not recognize or cannot act upon.</span></span> <span data-ttu-id="0c0ab-114">Usando [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) esses atributos ignorados são enviados de volta para o EAPHost e o método EAP.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-114">Using [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) these ignored attributes are sent back to EAPHost and the EAP method.</span></span>

## <a name="vendor-specific-attributes"></a><span data-ttu-id="0c0ab-115">Atributos específicos do fornecedor</span><span class="sxs-lookup"><span data-stu-id="0c0ab-115">Vendor Specific Attributes</span></span>

<span data-ttu-id="0c0ab-116">Usando o atributo EAP específico do fornecedor, os métodos EAP e os suplicantes podem se envolver na troca de dados para uma finalidade específica.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-116">By using the vendor-specific EAP attribute, EAP methods and supplicants can engage in data exchange for a specific purpose.</span></span> <span data-ttu-id="0c0ab-117">Atributos específicos do fornecedor são ignorados por suplicantes e métodos que não dão suporte ao atributo específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-117">Vendor-specific attributes are ignored by supplicants and methods that do not support the vendor-specific attribute.</span></span>

<span data-ttu-id="0c0ab-118">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c0ab-118">For more information, see the following topics.</span></span>

-   <span data-ttu-id="0c0ab-119">[Atributos EAP](about-eap-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0c0ab-119">[EAP Attributes](about-eap-attributes.md).</span></span>
-   <span data-ttu-id="0c0ab-120">[**EAP \_ \_tipo de atributo**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="0c0ab-120">[**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c0ab-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c0ab-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c0ab-122">Configurando a interface do usuário do método EAP</span><span class="sxs-lookup"><span data-stu-id="0c0ab-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="0c0ab-123">Habilitando Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="0c0ab-123">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="0c0ab-124">Implementando o suporte do In-Band NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="0c0ab-124">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="0c0ab-125">Implementando o suporte a NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="0c0ab-125">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="0c0ab-126">Suplicantes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="0c0ab-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




