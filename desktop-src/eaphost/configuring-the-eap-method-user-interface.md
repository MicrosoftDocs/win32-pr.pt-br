---
title: Configurando o método EAP Interface do Usuário
description: Explica como configurar o suplicant fornecendo uma configuração de método EAP para EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6709e68bf20d8f38d3685f66e45313083e70e46b1a8a0bb0675616bdb4e8bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086700"
---
# <a name="configuring-the-eap-method-user-interface"></a>Configurando o método EAP Interface do Usuário

Este tópico explica como configurar o suplicant fornecendo uma configuração de método EAP para EAPHost.

Para um suplente executar uma autenticação baseada em EAP usando EAPHost, um suplicant deve fornecer uma configuração de método EAP para EAPHost por meio da [**função EapHostPeerBeginSession.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)

1.  Para obter a configuração do método EAP, um suplicant normalmente consulta EAPHost usando [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) para aprender o conjunto completo de métodos EAP que estão disponíveis e instalados no computador local. A lista de métodos normalmente é apresentada ao usuário em uma caixa de combinação ou outro controle de interface do usuário que permite que o usuário selecione o método que deseja.
    > [!Note]  
    > O suplílico pode optar por filtrar a lista exibida de métodos com base nos bits de propriedade do método indicados em **EAP \_ METHOD \_ INFO.eapProperties**. Alguns métodos podem não ser apropriados para as características de segurança do transporte fornecido pelo suplicant, por exemplo.

     

2.  Depois que o controle de interface do usuário for preenchido com o conjunto de métodos de EAP possíveis, o usuário selecionará o método que deseja configurar. Normalmente, o componente fornece um  botão Configuração ou **Propriedades** para o usuário acessar as propriedades de configuração do método EAP selecionado.
    > [!Note]
    > O suplicant está ciente de que há propriedades configuráveis pelo usuário com base no bit **eapPropSupportsConfig** que está sendo habilitado em **EAP \_ METHOD \_ INFO.eapProperties**.
    >
    > Para obter mais informações, consulte [**Propriedades do método EAP**](eap-method-properties.md).

     

3.  Quando o usuário clica no controle de interface do usuário apropriado, o suplente chama [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passando para a função o valor **HWND** para a própria interface do usuário do suplicant, a estrutura DE TIPO DE MÉTODO [**EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtida da consulta para a estrutura DE INFORMAÇÕES DO MÉTODO [**EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) e outros parâmetros necessários.
4.  Chamar [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invoca a própria interface do usuário de configuração de um método EAP. No retorno de **EapHostPeerInvokeConfigUI**, a função retornará um BLOB de configuração de método EAP como um parâmetro de saída.
5.  O supplicant armazena o BLOB de configuração, juntamente com a estrutura [**EAP \_ METHOD \_ TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) para uso com [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).
6.  O método preciso para armazenar o BLOB de configuração é totalmente de acordo com o suplílico. No entanto, o suplente sempre deve armazenar a configuração de maneira adequada e segura adequada para os dados de configuração de autenticação do sistema e do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando In-Band nap para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementando o suporte nap para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferindo dados entre os métodos Supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




