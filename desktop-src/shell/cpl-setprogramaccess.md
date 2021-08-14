---
description: Este tópico discute o recurso Definir SPAD (Padrões de Computador e Acesso ao Programa) encontrado no Painel de Controle.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Definir acesso ao programa e padrões de computador (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978749171366e3091738ac22c78e04cd92123a75d2288f7c83200ee8532d232c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861454"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Definir acesso ao programa e padrões de computador (SPAD)

Este tópico discute o recurso **Definir SPAD (Padrões** de Computador e Acesso ao Programa) encontrado no Painel de Controle. O SPAD está localizado no [item Painel de Controle](default-programs.md) padrão no Windows Vista e versões posteriores do Windows. No Windows XP, ele está localizado no **item** Adicionar ou Remover Programas e intitulou Definir Padrões e Acesso **ao Programa.**

> [!IMPORTANT]
> Este tópico não se aplica a Windows 10. A maneira como as associações de arquivos padrão funcionam mudou Windows 10. Para obter mais informações, consulte a seção sobre **Alterações em como Windows 10 lida com aplicativos padrão** nesta [postagem.](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

-   [Usando a ferramenta Definir Acesso ao Programa e Padrões do Computador](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Uma visão geral de definir o acesso ao programa e os padrões do computador](#an-overview-of-set-program-access-and-computer-defaults)
    -   [O valor do Registro LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Filtrando a lista Adicionar ou Remover Programas](#filtering-the-add-or-remove-programs-list)
-   [Recursos adicionais](#filtering-the-add-or-remove-programs-list)
-   [Tópicos relacionados](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Usando a ferramenta Definir Acesso ao Programa e Padrões do Computador

> [!Note]  
> A partir Windows 8, o SPAD configura padrões por usuário para o usuário atual. Antes de Windows 8, o SPAD definia padrões por computador. Quando um padrão por usuário ainda não tiver sido configurado pelo usuário, o sistema solicitará que ele defira um padrão por usuário em vez de fazer o retorno em um padrão por computador. É possível que os padrões por computador nunca foram vistos pelos usuários no Windows Vista e no Windows 7 se eles tivessem definido padrões por usuário anteriormente, pois os padrões por usuário substituem os padrões por computador nesses sistemas operacionais.

 

No Windows **XP,** Definir Acesso e Padrões do Programa é uma ferramenta encontrada como uma opção no item Adicionar ou Remover **Programas** do Painel de Controle. No Windows Vista e posterior, ele está localizado no [item Painel de Controle](default-programs.md) Padrão. Para [programas](reg-middleware-apps.md) registrados, ele executa as seguintes funções:

-   Habilita a escolha de programas padrão para cada tipo de cliente (até Windows somente 7).
-   Habilita o controle da exibição dos ícones, atalhos e entradas de menu do programa.
-   Fornece um conjunto de opções de programa padrão predefinidas. (Windows XP Service Pack 1 (SP1) somente)

Essa ferramenta é usada para os cinco tipos de cliente a seguir.

-   Navegador
-   Email
-   Programa de engenhamento instantâneo
-   Media player
-   Máquina virtual para Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Uma visão geral de definir o acesso ao programa e os padrões do computador

A Windows 8 **Definir Acesso ao Programa e** Padrões do Computador é mostrada na captura de tela a seguir.

![captura de tela da exibição de entrada definir acesso ao programa e padrões do computador](images/spad-initial.png)

Três opções de configuração possíveis são apresentadas ao usuário, com a opção para que os OEMs apresentem uma quarta opção intitulada "Fabricante do Computador".

-   [Microsoft Windows](#microsoft-windows)
-   [Não Microsoft](#non-microsoft)
-   [Personalizado](#custom)
-   [Fabricante do Computador](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

A **configuração Windows** Microsoft consiste em um conjunto de programas padrão fornecidos com Windows, conforme mostrado na captura de tela a seguir.

![captura de tela do conjunto de acesso ao programa e as opções padrão da Microsoft](images/mspage.png)

Selecionar a **configuração Windows** Microsoft também permite a exibição dos ícones, atalhos ou entradas de menu para cada programa registrado para qualquer um dos cinco tipos de cliente. Esses ícones, atalhos e entradas de **menu** estão disponíveis para o usuário no menu Iniciar ou tela inicial, na área de trabalho e em todos os outros locais aos quais foram adicionados.

### <a name="non-microsoft"></a>Não Microsoft

A **configuração não Microsoft,** mostrada na captura de tela a seguir, é usada para aplicativos registrados no sistema do usuário que não são produzidos pela Microsoft. Esses aplicativos podem ser pré-instalados no sistema do usuário ou podem ser aplicativos não Microsoft que o usuário instalou.

> [!Note]  
> Os aplicativos devem se registrar para aparecer nesta página. Para obter instruções sobre como registrar um aplicativo, consulte [Registrando programas com tipos de cliente](reg-middleware-apps.md).

 

![captura de tela do conjunto de acesso ao programa e padrões de opções que não são da Microsoft](images/nonmspage.png)

Selecionar a **opção Não Microsoft** também remove o acesso aos ícones, atalhos e entradas de menu dos programas da Microsoft listados na configuração do Microsoft [Windows](#microsoft-windows) para todos os tipos de cliente que os têm. Esses ícones, atalhos e entradas de **menu** da Microsoft são removidos do menu Iniciar, da área de trabalho e de outros locais aos quais foram adicionados.

### <a name="custom"></a>Personalizado

A **Configuração** personalizada, mostrada na captura de tela a seguir, permite que os usuários personalizem seus sistemas com qualquer combinação de programas da Microsoft e não Microsoft registrados como possibilidades padrão para os cinco tipos de cliente. Essa é a única das quatro opções disponíveis no Windows 2000 Service Pack 3 (SP3).

![captura de tela do conjunto de opções personalizadas de acesso ao programa e padrões](images/custompage.png)

Todas as opções apresentadas nas configurações do [Microsoft Windows](#microsoft-windows) e não  [Microsoft](#non-microsoft) estão disponíveis para o usuário na seção Personalizado, bem como quaisquer aplicativos da Microsoft instalados adicionalmente que não fazem parte do Windows. O **botão de rádio** Usar meu navegador da Web atual é pré-selecionado, conforme mostrado na captura de tela anterior. Não é possível determinar o navegador padrão atual da interface do usuário. Invocar links da Web ou arquivos Windows é a única maneira de descobrir o navegador padrão atual.

Quando um usuário  seleciona a caixa de seleção Habilitar acesso a este programa para um programa, os ícones, atalhos e entradas de menu do programa são exibidos no menu Iniciar ou tela inicial, na área de trabalho ou em qualquer outro local em que foram instalados. Limpar essa opção deve remover esses ícones, atalhos e entradas de menu, no entanto, o comportamento dessas opções é totalmente responsabilidade do fornecedor do aplicativo. Windows não controla como o acesso é habilitado ou removido em toda a interface do usuário. Também é importante entender que os aplicativos não precisam se registrar para Definir Acesso ao Programa **e Padrões do Computador.**

### <a name="computer-manufacturer"></a>Fabricante do Computador

Uma quarta categoria intitulada "Fabricante do Computador" pode aparecer na janela SPAD em alguns sistemas. Os fabricantes de computadores podem optar por pré-configurar seus computadores com um conjunto personalizado de padrões, escolhendo entre as mesmas seleções disponíveis na [Configuração](#custom) personalizada. (Para fins ilustrativos, um conjunto fictício de aplicativos chamado LitWare é registrado para uso com todos os tipos de cliente.) Um usuário pode retornar à configuração padrão do fabricante  do computador a qualquer momento escolhendo a opção Fabricante do Computador, conforme mostrado na captura de tela Windows XP a seguir.

> [!Note]  
> Essa configuração não aparece em todos os sistemas. Para obter detalhes, consulte o OPK (Kit de Pré-instalação do OEM).

 

![captura de tela das opções definir acesso ao programa e padrão do fabricante do computador](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>O valor do Registro LastUserInitiatedDefaultChange

O valor LastUserInitiatedDefaultChange foi adicionado ao Registro para ajudar os aplicativos a reconhecer e respeitar as opções padrão do usuário. O valor contém dados BINARY REG na forma de uma estrutura FILETIME que contém a data e \_ hora (em Tempo Universal Coordenado (UTC)) da [](/windows/win32/api/minwinbase/ns-minwinbase-filetime) última vez que o usuário alterou uma opção padrão por meio da ferramenta Definir Acesso ao Programa e Padrões do Computador.  Esse valor é encontrado na sub-chave a seguir.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

O cenário a seguir usa esse valor para um aplicativo que monitora associações de arquivos.

1.  Um aplicativo registra internamente a hora em que foi definido pela última vez como o programa padrão para seu tipo de cliente (na instalação ou posterior).
2.  O aplicativo detecta que o programa padrão para seu tipo de cliente foi alterado para um programa diferente de si mesmo ou o aplicativo que ele representa (no caso de programas auxiliares em segundo plano). Sem suporte em aplicativos no Windows 8.
3.  O aplicativo lê o valor de LastUserInitiatedDefaultChange (o carimbo de data/hora da última alteração padrão iniciada pelo usuário) e o compara com o valor do carimbo de data/hora armazenado para sua própria escolha como padrão.
4.  Se LastUserInitiatedDefaultChange for posterior ao valor armazenado do aplicativo, nenhuma ação deverá ser tomada por esse aplicativo  porque a alteração foi explicitamente solicitada pelo usuário por meio da ferramenta Definir Acesso e Padrões do Programa.
5.  O aplicativo não monitora mais essa associação de arquivo até que ele seja escolhido novamente como o padrão. Sem suporte em aplicativos no Windows 8.

Ao aderir a esse esquema, os votos do usuário são respeitados e sua propriedade final de seus sistemas é mantida.

## <a name="filtering-the-add-or-remove-programs-list"></a>Filtrando a lista Adicionar ou Remover Programas

> [!Note]  
> Esta seção se aplica ao Windows XP Service Pack 2 (SP2) e posterior e Windows Server 2003 e posterior.

 

No Windows XP e no Windows Server 2003, a lista  de aplicativos exibidos na guia Alterar ou Remover Programas em Adicionar ou Remover Programas pode ser filtrada pelo usuário para excluir entradas para atualizações de aplicativos.  Nessas versões do Windows, isso é  feito por meio de uma caixa de seleção Mostrar atualizações na parte superior da janela. A **opção Mostrar atualizações** não está selecionada  por padrão, portanto, as atualizações não são mostradas, a menos que o usuário opte por exibi-las. As alterações no estado da caixa de seleção persistem **quando Adicionar ou Remover Programas** é fechado; Se um usuário optar por mostrar as atualizações, ele continuará a ser mostrado até que o usuário des marque a caixa de seleção.

> [!Note]  
> A Windows XP SP2 em si é uma exceção para a filtragem. Ele é sempre exibido independentemente do estado da caixa de seleção.

 

No Windows Vista e posterior, as atualizações de aplicativos são exibidas em uma página separada Painel de Controle dedicadas apenas a atualizações. Esta página é mostrada quando o usuário clica no link da tarefa Exibir **atualizações instaladas.** Não há nenhuma opção selecionável pelo usuário para mostrar atualizações na mesma página que os programas instalados. Apesar da alteração na interface do usuário, o mecanismo de registro como uma atualização para um programa instalado permanece o mesmo que nas versões anteriores do Windows.

Aplicativos da Microsoft e não Microsoft que usam o Windows Instalador não precisam fazer nada além para que suas atualizações sejam reconhecidas como atualizações. Aplicativos não Microsoft que não usam Windows Instalador devem declarar determinados valores no Registro como parte de sua instalação para serem reconhecidos como uma atualização para um programa existente.

O exemplo a seguir ilustra quais valores de Registro declarar para que uma instalação seja reconhecida como uma atualização para um programa existente.

1.  O aplicativo pai deve adicionar suas informações de desinstalação em uma sub-chave na sub-chave **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall.** Consulte o [tópico Instalação](/previous-versions/ms997548(v=msdn.10)) para obter mais informações sobre como usar a sub-chave **Desinstalar.**
2.  Cada atualização para esse aplicativo pai também deve adicionar suas informações como uma sub-chave da sub-chave **Desinstalar.** Ele deve usar uma convenção de nomenização específica de sua escolha, tentando evitar possíveis conflitos com outros programas. As convenções a seguir são reservadas como nomes de sub-chave pela Microsoft para uso com Windows atualizações.
    -   IEUpdate
    -   OEUpdate
    -   "KB" seguido por seis dígitos, por exemplo"KB123456"
    -   "Q" seguido por seis dígitos, por exemplo "Q123456"
    -   Seis dígitos, por exemplo, "123456"
3.  Além das informações padrão de desinstalação adicionadas para o aplicativo pai, as sub-chaves para cada atualização também devem incluir duas das três entradas a seguir. Seus valores são do tipo REG \_ SZ.
    -   **ParentKeyName.** Esse valor é necessário. Esse é o nome da sub-chave do pai declarada na etapa 1. Isso associa a atualização ao programa.
    -   **ParentDisplayName**. Esse valor é necessário. Se nenhuma sub-chave corresponde à nomeada em ParentKeyName, esse valor é usado como um programa pai de espaço reservado a ser exibido em Adicionar ou **Remover Programas**.
    -   **InstallDate**. Esse valor é opcional. Ele deve usar o formulário `yyyymmdd` para especificar a data. Essa data é usada para **as informações Instaladas em** exibidas ao lado da entrada da atualização na interface do usuário. Se não houver nenhuma **entrada InstallDate** ou se ela estiver presente, mas não tiver nenhum valor atribuído a ela, ocorrerá o seguinte:
        -   Versões do sistema operacional diferentes Windows Vista e Windows 7: Nenhuma **informação instalada em** é mostrada.
        -   Windows Vista e posterior: uma data padrão é usada. Esta é a data de "última modificação" para qualquer uma das entradas na sub-chave dessa atualização. Normalmente, esse é o dia em que a atualização foi adicionada ao Registro. No entanto, como é uma data de "última modificação", qualquer alteração subsequente em qualquer uma das entradas da sub-chave faz com que o valor InstallDate seja alterado para a data dessa alteração.

O exemplo a seguir mostra as entradas pertinentes do Registro para uma atualização para o aplicativo LitWare Deluxe.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Uninstall
                  LitWare
                     DisplayName = LitWare Deluxe
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\litware.exe" /uninstall
                  LitWare_Update123456
                     DisplayName = LitWare Deluxe Update 123456. Fixes printing problems.
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\Updates\123456.exe" /uninstall
                     ParentKeyName = LitWare
                     ParentDisplayName = LitWare Deluxe
                     InstallDate = 20050513
```

Aplicativos não Microsoft que não fornecem as informações apropriadas do Registro, como atualizações produzidas antes que essa opção estava disponível, continuam sendo exibidos normalmente na lista de programas instalados e não são filtrados.

A filtragem de atualizações em versões do sistema operacional diferentes Windows Vista e Windows 7 normalmente é uma configuração controlada pelo usuário e deve ser respeitada como tal pelos aplicativos. No entanto, em um ambiente corporativo, os administradores podem controlar se os usuários têm a opção de filtrar atualizações por meio do valor do Registro DontGroupPatches, conforme mostrado no exemplo a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               policies
                  Uninstall
                     DontGroupPatches = 0 or 1
```

Esse valor é do tipo REG \_ DWORD e é interpretado da seguinte maneira.



| Valor de DontGroupPatches             | Significado                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | A **caixa de seleção** Mostrar atualizações é exibida para o usuário. A filtragem depende de o usuário ter marcado essa caixa ou não.                                                                                         |
| 1                                  | A **caixa de seleção** Mostrar atualizações é removida da interface do usuário. As atualizações não são filtradas da lista. Basicamente, esse valor é reversível Windows comportamento XP SP1, antes que a funcionalidade Mostrar **atualizações** seja introduzida. |
| Entrada DontGroupPatches não presente | Isso é equivalente a definir o valor como 0.                                                                                                                                                                       |



 

DontGroupPatches não tem nenhum efeito no Windows Vista e Windows 7, em que a interface do usuário não contém nenhuma caixa de seleção e as atualizações registradas sempre são filtradas.

> [!Note]  
> As políticas são definidas somente por administradores. Os aplicativos não devem alterar esse valor. Para obter mais informações sobre como definir um registro baseado em Política de Grupo, consulte [Política de Grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page) ou [Windows Server Política de Grupo](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Recursos adicionais

-   [Registrando programas com tipos de cliente](reg-middleware-apps.md)
-   [Instalação](/previous-versions/ms997548(v=msdn.10))
-   [Configurando Adicionar/Remover Programas com Windows Instalador](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para associações de arquivos](fa-best-practices.md)
</dt> <dt>

[Cenário de exemplo de associação de arquivo](fa-sample-scenarios.md)
</dt> <dt>

[Diretrizes para gerenciar aplicativos padrão no Windows Vista e posterior](vista-managing-defaults.md)
</dt> <dt>

[Programas padrão](default-programs.md)
</dt> </dl>

 

 
