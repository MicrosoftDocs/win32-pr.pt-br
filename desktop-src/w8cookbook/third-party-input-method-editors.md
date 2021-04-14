---
title: Editores de método de entrada de terceiros
description: Editores de método de entrada de terceiros
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca9768de96b9dcdeac7f4b0da210f7aa788801b
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104552248"
---
# <a name="third-party-input-method-editors"></a>Editores de método de entrada de terceiros

## <a name="platforms"></a>Plataformas

**Clientes** -Windows 8  
**Servidores** -Windows Server 2012  


## <a name="description"></a>Description

IMEs (Input Method Editors) são componentes de software que permitem que um usuário digite texto em um idioma que tenha mais caracteres do que pode ser representado em um teclado. (Isso é comum, mas não se limita a idiomas do leste asiático.) Em vez de cada caractere que aparece em uma única chave, os usuários digitam combinações de chaves que são então interpretadas pelo IME. O IME gera o caractere que corresponde ao conjunto de traços de chave, às vezes apresentando ao usuário uma lista de possíveis caracteres a serem escolhidos e, em seguida, insere o caractere na janela de controle de edição do aplicativo do usuário.

No passado, o Windows permitia que IMEs de terceiros executassem no sistema Windows, e esse recurso continua para o Windows 8. Os usuários podem instalar um IME de terceiros e usá-lo. Além disso, estamos protegendo o sistema e os processos para evitar IMEs mal-intencionados, melhorar a segurança e aprimorar a experiência do usuário.

No Windows 8, você encontrará:

-   Suporte de IME de terceiros para teclados de hardware e teclados de toque
-   Os fornecedores de IME de terceiros devem seguir as diretrizes da Microsoft para desenvolver seus IMEs para o Windows 8
-   IMEs de terceiros devem ser assinados digitalmente
-   IMEs de terceiros devem ser compatíveis com TSF (estrutura de serviços de texto) e os sinalizadores adequados do IME devem ser definidos para serem executados corretamente no Windows 8
-   IMEs de terceiros herdados poderão ser executados em aplicativos da área de trabalho, mas serão bloqueados em aplicativos da Windows Store
-   IMEs de terceiros podem usar o layout de teclado de toque fornecido pelo Windows para vincular o IME, para que os usuários possam usar o IME com teclas de toque. No entanto, determinadas funções do IMEs do box para teclados de toque não estarão disponíveis para IMEs de terceiros
-   O Windows Defender removerá IMEs mal-intencionados do sistema Windows

## <a name="manifestation"></a>Manifestação

**Alterações de opção de idioma de entrada e de método de entrada**

Em vez de mostrar todos os ícones do modo IME junto com o ícone de identidade visual do IME, apenas um ícone do modo IME junto com o ícone de identidade visual do IME é mostrado. As duas figuras abaixo mostram o submenu de entrada do Windows 8 e o submenu IME, com o IME do japonês como o método de entrada atual. Se você clicar no ícone de identidade visual do IME, poderá alternar os métodos de entrada.

![alternar métodos de entrada](images/inputindicator2.png)

Se você clicar no ícone do modo IME, poderá alternar para um modo IME diferente.

![alternar modos de IME](images/inputindicator1.png)

Se um IME depender da barra de idiomas para mostrar seus ícones de modo no Windows 7, o IME deverá ser alterado para mostrar o ícone de marca e o ícone de modo no indicador de entrada no Windows 8.

> [!Note]  
> Observação: os detalhes sobre como um IME podem mostrar seu ícone de identidade visual e o ícone de modo no SysTray na barra de tarefas do desktop serão documentados e postados publicamente nas diretrizes do IME do Windows 8.

 

**Novo ambiente do Windows**

O ambiente no Windows 8 altera o cenário para IMEs. Os conceitos de aplicativos da Windows Store, contêineres de aplicativo de contexto local e restrições de API em IMEs não estavam presentes no Windows 7. Alguns IMEs existentes do Windows 7 param de responder quando executados dentro de um aplicativo da Windows Store e, portanto, não permitem que IMEs herdados sejam executados dentro de aplicativos da Windows Store. Além disso, certifique-se de que as novas versões do IMEs sejam validadas para garantir que elas sejam compatíveis com o novo ambiente de interface do usuário antes de serem executadas dentro de aplicativos da Windows Store.

## <a name="mitigation"></a>Atenuação

Você pode usar um IME compatível com a área de trabalho no sistema. Essa pode ser a melhor opção se você usa principalmente aplicativos da área de trabalho e deseja continuar a usar um IME de legado preferencial para entrada. Recomendamos que você use um IME do Windows 8 e pare de usar IMEs herdados/não certificados. As notificações são fornecidas pelo CPL de idioma e pela opção de entrada para avisá-lo sobre os efeitos do uso de um IME compatível com a área de trabalho.

Você verá um dos comportamentos abaixo se um IME compatível com a área de trabalho não funcionar em seu sistema:

-   As linguagens da interface do usuário da CPL de idioma rotulam IMEs compatíveis com a área de trabalho e exibe uma mensagem informando que IMEs não compatíveis só funcionam em aplicativos de desktop
-   O submenu de entrada acinzenta os IMEs compatíveis com a área de trabalho quando o usuário está dentro de aplicativos da Windows Store. Isso indica que o IME não funciona nesse aplicativo. (No desktop, os IMEs compatíveis com a área de trabalho não estão acinzentados). Se você alternar para aplicativos da Windows Store com um IME não compatível e perceber que o IME está desativado, use o indicador de entrada para alterar para um IME compatível com os aplicativos da Windows Store.

IMEs herdados ou compatíveis com a área de trabalho são limitados a estas condições:

-   Atualizando do Windows 7 para o Windows 8, com IMEs de terceiros no sistema
-   O fornecedor não lançou uma versão compatível com o Windows 8 e o usuário tenta usar uma versão existente do Windows 7 enquanto isso

## <a name="solution"></a>Solução

**Geral**

Use a infraestrutura existente do TSF (estrutura de serviços de texto) para implementar a lógica do IME e os controles comuns do aplicativo da Windows Store para suas interfaces do serviço. Crie janelas de propriedade para hospedar sua interface do usuário.

Novas APIs de pesquisa estão sendo adicionadas para melhorar a previsão de pesquisa e fornecer uma experiência de pesquisa mais limpa na interface do usuário.

As APIs também estão sendo adicionadas para notificar IMEs de terceiros quando um teclado de toque é invocado para proteger a interface do usuário de ser coberta pelo teclado de toque. Um layout de teclado de toque clássico padrão é carregado automaticamente para IMEs de terceiros. Nenhum trabalho adicional é necessário para integrar com esse layout de teclado de toque clássico. No entanto, IMEs de terceiros poderão solicitar um layout de toque alternativo.

Familiarize-se com as diretrizes do IME do Windows 8 para que você possa promover os principais princípios de experiência do usuário do aplicativo da Windows Store em seu IME. Os IMEs que seguem as diretrizes devem definir um sinalizador para indicar que o IME é compatível com o design da Microsoft. O Windows 8 bloqueia a execução de todos os IMEs compatíveis com a área de trabalho em aplicativos da Windows Store.

A assinatura digital, além da revogação pelo Windows Defender, impede que IMEs mal-intencionados sejam instalados no sistema Windows 8. Após a verificação de identidade, o. dll de um IME de terceiros é assinado digitalmente. Somente IMEs que têm essa assinatura digital podem ser instalados no sistema sem que uma mensagem de aviso crítica seja exibida ao usuário. Os usuários podem relatar IMEs mal-intencionados. Depois que um IME for determinado como mal-intencionado, o Windows defender o removerá do sistema Windows.

**Estrutura de serviços de texto**

O IME deve reconhecer o TSF para poder ser executado no Windows 8. O Windows 8 bloqueia a execução de IMEs não cientes de TSF em aplicativos da Windows Store. Quando um aplicativo é iniciado, o TSF carrega o IME. dll para o IME que o usuário selecionou para o processo do aplicativo.

> [!Note]  
> Para fornecer funcionalidades ou interfaces de trabalho separadas entre aplicativos da Windows Store e aplicativos de desktop, o. dll carregado pelo TSF pode verificar em qual tipo de aplicativo ele está sendo carregado. O IME chama o método [ITfThreadMgrEx:: GetActiveFlags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) e verifica o \_ sinalizador TF TMF \_ imersivamode e pode disparar uma lógica de aplicativo diferente dependendo do resultado.

 

Quando um IME é carregado em um aplicativo da Windows Store, ele está sujeito às mesmas restrições de contêiner de aplicativo que o próprio aplicativo. Esse comportamento garante que os IMEs não sejam capazes de violar os contratos de segurança de aplicativo da Windows Store, apesar de terem acesso ao SDK de desktop (porque eles não são distribuídos ou certificados pela Windows Store). Algumas funções que os IMEs executam atualmente são afetadas dentro de um contêiner de aplicativo. Essas funções incluem:

-   Arquivos de dicionário
-   Atualização da Internet
-   Aprendizado em tempo real
-   Compartilhando informações entre processos

Consulte as diretrizes do IME do Windows 8 para obter mais informações.

Os IMEs herdados não funcionam em aplicativos da Windows Store para evitar o potencial de experiências de usuário inadequadas, incluindo contornarem o sistema. Os IMEs compatíveis com os aplicativos da Windows Store devem ser autodeclarados definindo um sinalizador que indica essa compatibilidade. Esse sinalizador é fornecido pelo TSF na estrutura TF \_ INPUTPROCESSORPROFILE. Os detalhes sobre como usar esse sinalizador para declarar um IME de terceiros como compatível com o aplicativo da Windows Store serão documentados e postados publicamente nas diretrizes do IME do Windows 8.

IMEs compatíveis com aplicativos da Windows Store podem ser executados em aplicativos de área de trabalho ou aplicativos da Windows Store. Os IMEs que não são compatíveis só podem ser executados em processos de área de trabalho.

**Interface do usuário**

Embora IMEs de terceiros tenham acesso às APIs de janelas da área de trabalho, eles devem seguir as mesmas restrições de API de janela que o aplicativo em que estão sendo executados. Por exemplo, um IME não pode desenhar sobre um aplicativo da Windows Store enquanto estiver ativo em um aplicativo de área de trabalho. As restrições de API são destinadas a evitar esses cenários:

-   Aplicativos da área de trabalho que se concentram em aplicativos da Windows Store
-   Desenho de aplicativos da área de trabalho no aplicativo da Windows Store
-   Aplicativos da área de trabalho interferindo com aplicativos da Windows Store

**Suporte ao teclado de toque**

Embora o suporte ao Touch Keyboard (TKB) ainda esteja disponível para fornecedores de IME de terceiros, uma experiência de teclado de toque totalmente personalizável e integrada não é fornecida no Windows 8. No entanto, IMEs de terceiros podem mapear seus IMEs com o layout de teclado otimizado para toque. O SIP (painel de entrada suave) do Windows fornece um layout de teclado clássico por padrão para IMEs de terceiros. Como o teclado clássico gera eventos importantes semelhantes a como um teclado de hardware faz, atualmente não há nenhum requisito de implementação especial para que IMEs de terceiros trabalhem com um teclado de toque. O tratamento de entrada para eventos de chave de hardware também tratará os principais eventos de layouts de toque clássicos.

> [!Note]  
> Observação: os IMEs talvez precisem começar a tratar eventos de entrada Unicode se o suporte a TKB for estendido para incluir layouts de teclado otimizados também.

 

Um IME de terceiros pode optar por usar o layout de teclado otimizado para seu IME. Consulte a diretriz de IME de terceiros para obter mais informações.

Verifique se a interface do usuário do seu painel candidato (e outros elementos da interface do usuário) não está desenhada sob o teclado de toque. Na maioria dos casos, o aplicativo deve redimensionar sua janela para considerar o teclado de toque. No entanto, se um aplicativo não fizer isso, os IMEs ainda poderão usar a API InputPaneFramework para saber a posição do teclado de toque. Os IMEs de terceiros podem usar essa API para obter o espaço de tela consumido pelo teclado de toque antes de desenhar (ou outras) interfaces do usuário e refluir sua interface do usuário para evitar o desenho sob o teclado de toque.

**Procurar**

No Windows 8, os aplicativos da Windows Store podem facilmente fornecer aos usuários recursos de pesquisa implementando o [contrato de pesquisa](/previous-versions/windows/apps/hh464906(v=win.10)) e integrando com o painel de pesquisa. O painel de pesquisa é um local central para os usuários executarem pesquisas em todos os seus aplicativos. O Windows ajuda os aplicativos que usam o painel de pesquisa a acessar seus usuários onde quiserem o mais rápido possível. Em particular, para os usuários do IME, ele fornece uma experiência de pesquisa exclusiva que permite que IMEs compatíveis se integrem ao Windows 8 para maior eficiência e usabilidade.

Um IME é compatível com a experiência de pesquisa integrada se atender a estes critérios:

-   É compatível com o ambiente de aplicativo da Windows Store
-   Implementa APIs do modo UILess do TFS
-   Implementa APIs de integração de pesquisa do TFS:
-   -   ItfSearchCandidateProvider
    -   ItfSearchHardwareKeyboardBehaviors

Quando ativado no painel de pesquisa, o IME compatível é colocado no modo UILess e não pode mostrar sua interface do usuário. Em vez disso, ele envia candidatos à conversão para o Windows, que os exibirá no controle de lista de candidatos embutidos.

O IME também envia os candidatos do Windows que devem ser usados para executar a pesquisa atual – esses candidatos podem ser iguais aos candidatos à conversão ou podem ser adaptados para pesquisa. Bons candidatos de pesquisa atendem a estes critérios:

-   Sem sobreposição de prefixo
-   Nenhum candidato à previsão (somente conclusão)

Os IMEs que não atendem aos critérios e não são compatíveis com a pesquisa são mostrados da mesma maneira que em outros controles de aplicativo da Windows Store e não podem aproveitar a integração da interface do usuário e os candidatos à pesquisa. (Os aplicativos recebem consultas somente depois que o usuário termina de redigir.)

Quando um aplicativo que dá suporte ao contrato de pesquisa recebe uma consulta, o evento de consulta incluirá uma matriz "queryTextAlternatives" contendo todas as alternativas conhecidas, classificadas da mais relevante (provavelmente) a menos relevante (improvável). Sempre que as alternativas são fornecidas, o aplicativo deve tratar cada alternativa como uma consulta e retornar todos os resultados que correspondam a qualquer uma das alternativas (como se o usuário tivesse emitido várias consultas ao mesmo tempo), essencialmente emitindo uma consulta "or" para o serviço que fornece os resultados. Para melhorar o desempenho, os aplicativos geralmente limitarão a correspondência às 10 alternativas mais relevantes.

**Assinatura digital do IME**

Todos os IMEs de terceiros devem ser assinados digitalmente para serem instalados no sistema do Windows 8 como um IME. Usando o SmartScreen, os usuários podem ver uma mensagem de aviso ao baixar um IME não assinado da Web. Para obter um certificado e assinar seus arquivos:

-   **Usar uma assinatura Authenticode para assinar digitalmente os programas**
    -   Obter um certificado de assinatura de código Authenticode válido de uma das várias autoridades de certificação com suporte no Windows
    -   Usar ferramentas de desenvolvimento (como [signtool.exe](../seccrypto/signtool.md)) para assinar os aplicativos antes da distribuição
    -   Para obter mais informações e uma descrição passo a passo do processo de assinatura de código, consulte a entrada de blog [tudo o que você precisa saber sobre assinatura de código Authenticode](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing)
-   **Certifique-se de que os downloads não sejam detectados como malware**
    -   Programas baixados que são detectados e confirmados como malware afetam a reputação do download e a reputação do certificado digital usado para assinar esse arquivo
-   **Aplicar para certificação do Windows**
    -   Visite a página de certificação de aplicativo do Windows no MSDN

Para obter mais informações, consulte estes artigos sobre assinaturas digitais e assinatura de código:

-   [Visão geral do Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantindo a integridade e a autenticidade](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Práticas recomendadas de assinatura de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [O que são certificados digitais?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

Se um IME **não estiver** assinado, o usuário receberá essa mensagem de aviso quando tentar baixar o IME:

![mensagem de aviso do IME não assinado](images/downloadwarning02-fhu-ivu.png)

Se um IME for assinado, os usuários verão essa mensagem:

![o IME é uma mensagem assinada](images/downloadwarning01-fhu-vcu.png)

Com base nessas notificações, os usuários podem escolher se deseja excluir o arquivo ou ignorar o aviso e executar o programa baixado.

**Revogação do IME**

Os IMEs que são mal-intencionados ou que não seguem as diretrizes do IME do Windows 8 podem ser removidos do sistema usando o Windows Defender. Para obter mais informações sobre IMEs mal-intencionados, consulte o artigo sobre IMEs de terceiros [no Windows 8](/previous-versions/windows/apps/hh967426(v=win.10)).

## <a name="resources"></a>Recursos

-   [Método ITfThreadMgrEx:: obter sinalizadores ativos](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [SignTool](../seccrypto/signtool.md)
-   [Tudo o que você precisa saber sobre a assinatura de código Authenticode](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   [Contratos e extensões de aplicativo do Windows](/previous-versions/windows/apps/hh464906(v=win.10))
-   [Requisitos de certificação para aplicativos de área de trabalho do Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Requisitos de certificação para aplicativos do Windows](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [Usando o Kit de Certificação de Aplicativos Windows](../win_cert/using-the-windows-app-certification-kit.md)
-   [Visão geral do Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantindo a integridade e a autenticidade](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)
-   [Práticas recomendadas de assinatura de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [O que são certificados digitais?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

 

 