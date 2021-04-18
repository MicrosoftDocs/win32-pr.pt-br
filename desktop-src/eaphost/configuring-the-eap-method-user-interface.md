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
# <a name="configuring-the-eap-method-user-interface"></a>Configurando a interface do usuário do método EAP

Este tópico explica como configurar o suplicante fornecendo uma configuração de método EAP para EAPHost.

Para que um suplicante execute uma autenticação baseada em EAP usando o EAPHost, um suplicante deve fornecer uma configuração de método EAP para EAPHost por meio da função [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .

1.  Para obter a configuração do método EAP, um suplicante normalmente consulta o EAPHost usando [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) para aprender o conjunto completo de métodos EAP que estão disponíveis e instalados no computador local. A lista de métodos normalmente é apresentada ao usuário em uma caixa de combinação ou outro controle de interface do usuário que permite ao usuário selecionar o método desejado.
    > [!Note]  
    > O suplicante pode optar por filtrar a lista exibida de métodos com base nos bits de propriedade de método indicados no **\_ método EAP \_ info. eapProperties**. Alguns métodos podem não ser apropriados para as características de segurança do transporte fornecido pelo suplicante, por exemplo.

     

2.  Depois que o controle da interface do usuário é populado com o conjunto de métodos EAP possíveis, o usuário seleciona o método que deseja configurar. Normalmente, o suplicante fornece um botão de **configuração** ou **Propriedades** para que o usuário acesse as propriedades de configuração do método EAP selecionado.
    > [!Note]
    > O suplicante está ciente de que há propriedades configuráveis pelo usuário com base no **eapPropSupportsConfig** bit sendo habilitado no **\_ método EAP \_ info. eapProperties**.
    >
    > Para obter mais informações, consulte [**Propriedades do método EAP**](eap-method-properties.md).

     

3.  Quando o usuário clica no controle de interface do usuário apropriado, o suplicante chama [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passando para a função o valor de **HWND** para a própria interface do usuário do suplicante, a estrutura de [**\_ \_ tipo de método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtida da consulta para a estrutura de [**\_ \_ informações do método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) e outros parâmetros necessários.
4.  Chamar [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invoca uma interface do usuário de configuração própria do método EAP. No retorno de **EapHostPeerInvokeConfigUI**, a função retornará um blob de configuração do método EAP como um parâmetro out.
5.  O suplicante armazena o BLOB de configuração, juntamente com a estrutura do [**\_ \_ tipo de método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) para uso com [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).
6.  O método preciso para armazenar o BLOB elementos é inteiramente o suplicante. No entanto, o suplicante sempre deve armazenar a configuração de maneira adequada e segura apropriada para dados de configuração de autenticação do sistema e do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando o suporte do In-Band NAP para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementando o suporte a NAP para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferindo dados entre os métodos suplicante e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes do EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




