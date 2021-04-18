---
title: Configurando a interface do usuário do método EAP
description: Explica como configurar o suplicante fornecendo uma configuração de método EAP para EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105766498"
---
# <a name="configuring-the-eap-method-user-interface"></a><span data-ttu-id="221da-103">Configurando a interface do usuário do método EAP</span><span class="sxs-lookup"><span data-stu-id="221da-103">Configuring the EAP Method User Interface</span></span>

<span data-ttu-id="221da-104">Este tópico explica como configurar o suplicante fornecendo uma configuração de método EAP para EAPHost.</span><span class="sxs-lookup"><span data-stu-id="221da-104">This topic explains how to configure the supplicant by supplying an EAP method configuration to EAPHost.</span></span>

<span data-ttu-id="221da-105">Para que um suplicante execute uma autenticação baseada em EAP usando o EAPHost, um suplicante deve fornecer uma configuração de método EAP para EAPHost por meio da função [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .</span><span class="sxs-lookup"><span data-stu-id="221da-105">For a supplicant to perform an EAP-based authentication using EAPHost, a supplicant must supply an EAP method configuration to EAPHost through the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) function.</span></span>

1.  <span data-ttu-id="221da-106">Para obter a configuração do método EAP, um suplicante normalmente consulta o EAPHost usando [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) para aprender o conjunto completo de métodos EAP que estão disponíveis e instalados no computador local.</span><span class="sxs-lookup"><span data-stu-id="221da-106">To obtain the EAP method configuration, a supplicant typically queries EAPHost using [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) to learn the complete set of EAP methods that are available and installed on the local machine.</span></span> <span data-ttu-id="221da-107">A lista de métodos normalmente é apresentada ao usuário em uma caixa de combinação ou outro controle de interface do usuário que permite ao usuário selecionar o método desejado.</span><span class="sxs-lookup"><span data-stu-id="221da-107">The list of methods is typically presented to the user in a combination box or other UI control that allows the user to select the method they want.</span></span>
    > [!Note]  
    > <span data-ttu-id="221da-108">O suplicante pode optar por filtrar a lista exibida de métodos com base nos bits de propriedade de método indicados no **\_ método EAP \_ info. eapProperties**.</span><span class="sxs-lookup"><span data-stu-id="221da-108">The supplicant may choose to filter the displayed list of methods based on the method property bits indicated in **EAP\_METHOD\_INFO.eapProperties**.</span></span> <span data-ttu-id="221da-109">Alguns métodos podem não ser apropriados para as características de segurança do transporte fornecido pelo suplicante, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="221da-109">Some methods may not be appropriate for the security characteristics of the transport provided by the supplicant, for example.</span></span>

     

2.  <span data-ttu-id="221da-110">Depois que o controle da interface do usuário é populado com o conjunto de métodos EAP possíveis, o usuário seleciona o método que deseja configurar.</span><span class="sxs-lookup"><span data-stu-id="221da-110">Once the UI control is populated with the set of possible EAP methods, the user selects the method they want to configure.</span></span> <span data-ttu-id="221da-111">Normalmente, o suplicante fornece um botão de **configuração** ou **Propriedades** para que o usuário acesse as propriedades de configuração do método EAP selecionado.</span><span class="sxs-lookup"><span data-stu-id="221da-111">Typically, the supplicant provides a **Configuration** or **Properties** button for the user to access configuration properties of the selected EAP method.</span></span>
    > [!Note]
    > <span data-ttu-id="221da-112">O suplicante está ciente de que há propriedades configuráveis pelo usuário com base no **eapPropSupportsConfig** bit sendo habilitado no **\_ método EAP \_ info. eapProperties**.</span><span class="sxs-lookup"><span data-stu-id="221da-112">The supplicant is aware that there are user-configurable properties based on the **eapPropSupportsConfig** bit being enabled in **EAP\_METHOD\_INFO.eapProperties**.</span></span>
    >
    > <span data-ttu-id="221da-113">Para obter mais informações, consulte [**Propriedades do método EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="221da-113">For more information, see [**EAP Method Properties**](eap-method-properties.md).</span></span>

     

3.  <span data-ttu-id="221da-114">Quando o usuário clica no controle de interface do usuário apropriado, o suplicante chama [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passando para a função o valor de **HWND** para a própria interface do usuário do suplicante, a estrutura de [**\_ \_ tipo de método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtida da consulta para a estrutura de [**\_ \_ informações do método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) e outros parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="221da-114">When the user clicks the appropriate UI control, the supplicant calls [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passing into the function the **HWND** value for the supplicant's own UI, the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure obtained from the query to [**EAP\_METHOD\_INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) structure and other required parameters.</span></span>
4.  <span data-ttu-id="221da-115">Chamar [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invoca uma interface do usuário de configuração própria do método EAP.</span><span class="sxs-lookup"><span data-stu-id="221da-115">Calling [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invokes an EAP method's own configuration UI.</span></span> <span data-ttu-id="221da-116">No retorno de **EapHostPeerInvokeConfigUI**, a função retornará um blob de configuração do método EAP como um parâmetro out.</span><span class="sxs-lookup"><span data-stu-id="221da-116">On return from **EapHostPeerInvokeConfigUI**, the function will return an EAP method configuration BLOB as an out-parameter.</span></span>
5.  <span data-ttu-id="221da-117">O suplicante armazena o BLOB de configuração, juntamente com a estrutura do [**\_ \_ tipo de método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) para uso com [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="221da-117">The supplicant stores the configuration BLOB, along with the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure for use with [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>
6.  <span data-ttu-id="221da-118">O método preciso para armazenar o BLOB elementos é inteiramente o suplicante.</span><span class="sxs-lookup"><span data-stu-id="221da-118">The precise method for storing the configuraiton BLOB is entirely up to the supplicant.</span></span> <span data-ttu-id="221da-119">No entanto, o suplicante sempre deve armazenar a configuração de maneira adequada e segura apropriada para dados de configuração de autenticação do sistema e do usuário.</span><span class="sxs-lookup"><span data-stu-id="221da-119">However, the supplicant should always store the configuration in a suitable, secure manner appropriate for system and user authentication configuration data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="221da-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="221da-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="221da-121">Habilitando Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="221da-121">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="221da-122">Implementando o suporte do In-Band NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="221da-122">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="221da-123">Implementando o suporte a NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="221da-123">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="221da-124">Transferindo dados entre os métodos suplicante e EAP</span><span class="sxs-lookup"><span data-stu-id="221da-124">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="221da-125">Suplicantes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="221da-125">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




