---
description: Fornece uma visão geral das alterações nos controles Windows pais introduzidos no Windows 7.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Novidades nos controles Windows 7 pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7b545c6791d286e51ae7a36ed65623d1697a7e742b1ae956e3ef4aaf3425e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951816"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Novidades nos controles Windows 7 pais

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Visão geral das alterações de controles dos pais Windows 7

A finalidade deste documento é dar uma visão geral das alterações nos controles dos pais do Windows introduzidos no Windows 7 e permitir que provedores de soluções de controle dos pais de terceiros aproveitem essas alterações. Este documento assume a familiaridade dos leitores com os Controles dos Pais para Windows Vista e refletirá apenas as alterações feitas a essa funcionalidade no Windows 7 que são relevantes para o desenvolvimento de soluções de controle dos pais de terceiros. Uma atualização completa da documentação do MSDN Windows Controle dos Pais será seguida em uma data posterior.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Principais decisões de design para Windows 7 alterações de controle dos pais

As alterações nos Controles dos Pais introduzidas no Windows 7 continuam a meta abrangente de promover a coexistência das soluções de controle dos pais de terceiros com a funcionalidade in-box. As alterações são:

-   Remoção de relatórios de atividades e filtragem da Web da funcionalidade de controles internos dos pais. Os controles internos dos pais fornecem as principais restrições offline implementadas pela Microsoft, como limites de tempo, restrições de aplicativo e restrições de jogo. A filtragem da Web, o relatório de atividades e outras funcionalidades podem ser fornecidos pela Microsoft ou por soluções de controle dos pais de terceiros. Por exemplo, Windows Live Proteção para a Família solução fornece filtragem da Web, gerenciamento remoto e monitoramento de atividades, bem como gerenciamento de contatos para todos os Windows Live.
-   Habilitando soluções de terceiros para substituir a interface do usuário de configuração do provedor in-box enquanto ainda depende da implementação in-box de restrições de tempo, aplicativo e jogo.
-   Permitir que soluções de terceiros sejam descobertas e habilitadas no computador por um pai ou guardião (conta de administrador).

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Controles dos pais Alterações Interface do Usuário nível superior no Windows 7

Windows 7 traz as seguintes alterações à interface do usuário de nível superior Painel de Controle Controles Dos Pais:

-   A seção Controles adicionais é introduzida em que controles que fornecem funcionalidades adicionais, como filtragem da Web, relatórios de atividades e assim por diante, podem ser selecionados em uma caixa de listagem listada. A Microsoft ou provedores de terceiros precisam registrar suas soluções com Windows 7 Controles Dos Pais para que eles sejam selecionáveis na caixa de listagem lista de controles adicionais. Para obter informações sobre como registrar uma solução, consulte Registro de provedor, mais adiante neste tópico).
-   A imagem de logotipo do provedor selecionado no momento é exibida no canto superior direito da página.
-   Os blocos de usuário gerenciado podem exibir um resumo das configurações dos pais fornecidas pelo provedor selecionado no momento.

O provedor selecionado no momento pode optar por usar sua própria interface do usuário para telas de Controle de Usuário para os usuários gerenciados ou pode optar por contar com a implementação de WPC interna desta tela. A implementação in-box tem as seguintes alterações feitas em seus elementos:

-   A seção relatório de atividades é removida.
-   O link para exibir relatórios de atividade é removido.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Visão geral da API de Controles dos Pais: Windows 7 alterações

O mecanismo de integração para provedores de soluções de terceiros foi expandido para permitir:

-   Registro do provedor. Após o registro, um provedor se torna selecionável na caixa de listagem lista de controles adicionais na tela Controles dos Pais Painel de Controle.
-   Consultando o provedor selecionado no momento. Uma interface COM pública é exposta para habilitar essa funcionalidade.
-   Também é novo o conjunto de interfaces COM a ser implementado pelos provedores para permitir:
    -   Habilitando ou desabilitando o provedor pelo WPC após a seleção de controles adicionais pelo usuário.
    -   WPC para passar o controle para o provedor para definir as configurações de controle dos pais do usuário gerenciado.
    -   WPC para consultar o provedor para ver o resumo das configurações de controle dos pais do usuário gerenciado.

## <a name="third-party-provider-integration"></a>Integração de provedores de terceiros

### <a name="provider-registration"></a>Registro do provedor

Para registrar um novo provedor com controles dos pais, um valor do Registro deve ser gravado na chave Provedores do Windows Dos Pais. O nome do valor é um GUID exclusivo usado para identificar o provedor. Os dados de valor serão um caminho para uma chave do Registro em **HKEY \_ LOCAL \_ MACHINE** que contém informações do provedor.

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

No local da chave do Registro especificado, os valores a seguir são esperados.



| Termo                                                                                                                 | Descrição                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogotipoImagem**<br/>         | Um caminho totalmente qualificado para um binário de recurso com uma ID de recurso negativa para a imagem de logotipo do provedor (armazenada como **um \_ BITMAP de IMAGEM).**<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**<br/> | Um caminho totalmente qualificado para um binário de recurso com uma ID de recurso negativa para o nome do provedor. O comprimento de **DisplayName** não deve exceder 50 caracteres.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**<br/> | Um caminho totalmente qualificado para um binário de recurso com uma ID de recurso negativa para a descrição do provedor. O comprimento da descrição não deve exceder 200 caracteres.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | A ID de classe da classe do provedor que implementa IWPCProviderState.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | A ID de classe da classe do provedor, que implementa IWPCProviderConfig. **StateCLSID** e **ConfigCLSID** podem ser os mesmos.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Um valor **opcional DWORD** diferente de zero que especifica que Windows Controles Dos Pais exibe um link para a tela Sistema de Classificação de Jogos depois que um provedor é selecionado como o novo provedor atual.<br/> |



 

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

Os controles dos Painel de Controle usam **o LogotipoImage,** **DisplayName** e **Descrição** para alterar a página principal dos controles dos pais Painel de Controle quando esse provedor é selecionado. O **valor StateCLSID** é usado quando o provedor está habilitado ou desabilitado. O **valor configCLSID** é usado quando a interface do usuário obtém informações dinâmicas sobre cada usuário (esse é apenas o caso se o provedor está selecionado no momento).

 

 




