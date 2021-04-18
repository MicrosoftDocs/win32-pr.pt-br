---
description: Fornece uma visão geral das alterações para os controles dos pais do Windows introduzidos no Windows 7.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: O que há de novo nos controles dos pais do Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8282021c81ee8611fb7206d75f7e6aab48ebf2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780704"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>O que há de novo nos controles dos pais do Windows 7

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Visão geral das alterações de controles dos pais para o Windows 7

A finalidade deste documento é apresentar uma visão geral das alterações nos controles dos pais do Windows introduzidos no Windows 7 e permitir que provedores de soluções de controle de pais de terceiros aproveitem essas alterações. Este documento pressupõe a familiaridade dos leitores com os controles dos pais para o Windows Vista e refletirá apenas as alterações feitas nessa funcionalidade no Windows 7 que são relevantes para o desenvolvimento de soluções de controle de pais de terceiros. Uma atualização completa da documentação do controle dos pais do Windows do MSDN será seguida em uma data posterior.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Principais decisões de design para as alterações de controle dos pais do Windows 7

As alterações nos controles dos pais introduzidas no Windows 7 continuam com a meta abrangente de promover a coexistência de soluções de controle de pais de terceiros com a funcionalidade integrada. As alterações são:

-   Remoção de relatórios de atividade e filtragem da Web da funcionalidade de controles dos pais na caixa. Os controles dos pais na caixa fornecem restrições offline implementadas pela Microsoft, como limites de tempo, restrições de aplicativos e restrições de jogos. A filtragem da Web, o relatório de atividades e outras funcionalidades podem ser fornecidos pela Microsoft ou por soluções de controle de pais de terceiros. Por exemplo, a solução de segurança da família Windows Live fornece filtragem da Web, gerenciamento remoto e monitoramento de atividades, bem como o gerenciamento de contatos para todos os aplicativos do Windows Live.
-   A habilitação de soluções de terceiros para substituir a interface do usuário de configuração do provedor in-box, ainda que dependa da implementação de tempo, do aplicativo e das restrições de jogo.
-   Permitir que soluções de terceiros sejam descobertas e habilitadas no computador por um pai ou guardião (conta de administrador).

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Os pais controlam as alterações de interface de usuário de nível superior no Windows 7

O Windows 7 traz as seguintes alterações para a interface do usuário de nível superior do painel de controle dos controles dos pais:

-   A seção controles adicionais é introduzida onde os controles que fornecem funcionalidade adicional, como filtragem da Web, relatórios de atividades e assim por diante, podem ser selecionados em uma caixa de listagem suspensa. Os provedores da Microsoft ou de terceiros precisam registrar suas soluções com controles dos pais do Windows 7 para que sejam selecionáveis na caixa de listagem suspensa controles adicionais. Para obter informações sobre como registrar uma solução, consulte registro de provedor, mais adiante neste tópico).
-   A imagem de logotipo do provedor selecionado no momento é exibida no canto superior direito da página.
-   Os blocos de usuário gerenciados podem exibir um resumo das configurações de pais fornecidas pelo provedor selecionado no momento.

O provedor selecionado no momento pode optar por usar sua própria interface de usuário para telas de controle de usuário para os usuários gerenciados ou pode optar por confiar na implementação WPC da caixa de entrada desta tela. A implementação na caixa tem as seguintes alterações feitas em seus elementos:

-   A seção relatório de atividades foi removida.
-   O link para exibir relatórios de atividade é removido.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Visão geral da API de controles dos pais: alterações do Windows 7

O mecanismo de integração para provedores de soluções de terceiros foi expandido para permitir:

-   Registro do provedor. Após o registro, um provedor se torna selecionável na caixa de listagem suspensa controles adicionais na tela do painel de controle dos controles dos pais.
-   Consultando o provedor selecionado no momento. Uma interface COM pública é exposta para habilitar essa funcionalidade.
-   Além disso, novo é o conjunto de interfaces COM a ser implementado pelos provedores para permitir:
    -   Habilitando ou desabilitando o provedor por WPC na seleção de usuário de controles adicionais.
    -   WPC para passar o controle para o provedor para definir as configurações de controle de pais do usuário gerenciado.
    -   WPC para consultar o provedor para obter o resumo das configurações de controle de pais do usuário gerenciado.

## <a name="third-party-provider-integration"></a>Integração de provedor de terceiros

### <a name="provider-registration"></a>Registro do provedor

Para registrar um novo provedor com controles dos pais, um valor de registro deve ser gravado na chave de provedores de controles dos pais do Windows. O nome do valor é um GUID exclusivo que é usado para identificar o provedor. Os dados do valor serão um caminho para uma chave do registro **na \_ \_ máquina local hKey** que contém informações do provedor.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Parental Controls
                  Providers
                     {45D63315-0824-4df4-B8A4-EF137D8810D1} = SOFTWARE\Microsoft\Family Safety\WPC\
```

No local da chave do registro especificado, os valores a seguir são esperados.



| Termo                                                                                                                 | Descrição                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | Um caminho totalmente qualificado para um binário de recurso com uma ID de recurso negativo para a imagem do logotipo do provedor (armazenado como um **\_ bitmap de imagem**).<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**<br/> | Um caminho totalmente qualificado para um binário de recurso com uma ID de recurso negativa para o nome do provedor. O comprimento de **DisplayName** não deve exceder 50 caracteres.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**<br/> | Um caminho totalmente qualificado para um binário de recurso com uma ID de recurso negativo para a descrição do provedor. O tamanho da descrição não deve exceder 200 caracteres.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | A ID de classe da classe do provedor que implementa IWPCProviderState.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | A ID de classe da classe do provedor, que implementa IWPCProviderConfig. **StateCLSID** e **ConfigCLSID** podem ser iguais.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Um valor opcional **DWORD** diferente que especifica que os controles dos pais do Windows exibem um link para a tela do sistema de classificação de jogos depois que um provedor é selecionado como o novo provedor atual.<br/> |



 

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Family Safety
            WPC
               LogoImage = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40001
               DisplayName = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40002
               Description = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40003
               StateCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               ConfigCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               GRSVisible = 0x00000001 (1)
```

O painel de controle dos controles pai usa **LogoImage**, **DisplayName** e **Description** para alterar a página principal do painel de controle dos controles dos pais quando esse provedor é selecionado. O valor de **StateCLSID** é usado quando o provedor está habilitado ou desabilitado. O valor de **ConfigCLSID** é usado quando a interface do usuário obtém informações dinâmicas sobre cada usuário (esse é apenas o caso se o provedor estiver selecionado no momento).

 

 




