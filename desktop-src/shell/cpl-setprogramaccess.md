---
description: Este tópico discute o recurso Definir acesso do programa e padrões do computador (SPAD) encontrado no painel de controle.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Definir o acesso do programa e padrões do computador (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f35d9ed70d382e2db6714082ade2d2d76e6ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164311"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Definir o acesso do programa e padrões do computador (SPAD)

Este tópico discute o recurso **Definir acesso do programa e padrões do computador (SPAD)** encontrado no painel de controle. O SPAD está localizado no item do painel de controle [programas padrão](default-programs.md) no Windows Vista e versões posteriores do Windows. No Windows XP, ele está localizado no item **Adicionar ou remover programas** e intitulado **Definir acesso e padrões do programa**.

> [!IMPORTANT]
> Este tópico não se aplica ao Windows 10. A maneira como as associações de arquivo padrão funcionam alteradas no Windows 10. Para obter mais informações, consulte a seção sobre **alterações de como o Windows 10 trata os aplicativos padrão** nesta [postagem](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

-   [Usando a ferramenta definir acesso do programa e padrões do computador](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Uma visão geral de definir o acesso do programa e padrões do computador](#an-overview-of-set-program-access-and-computer-defaults)
    -   [O valor do registro LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Filtrando a lista Adicionar ou remover programas](#filtering-the-add-or-remove-programs-list)
-   [Recursos adicionais](#filtering-the-add-or-remove-programs-list)
-   [Tópicos relacionados](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Usando a ferramenta definir acesso do programa e padrões do computador

> [!Note]  
> A partir do Windows 8, o SPAD configura padrões por usuário para o usuário atual. Antes do Windows 8, o SPAD definiu padrões por computador. Quando um padrão por usuário ainda não tiver sido configurado pelo usuário, o sistema solicitará a eles que definam um padrão por usuário, em vez de fazer fallback em um padrão por máquina. É possível que os padrões por máquina nunca tenham sido vistos por usuários no Windows Vista e no Windows 7 se tiverem definido anteriormente padrões por usuário, porque os padrões por usuário substituem os padrões por computador nesses sistemas operacionais.

 

No Windows XP, **Definir acesso e padrões do programa** é uma ferramenta encontrada como uma opção no item **Adicionar ou remover programas** do painel de controle. No Windows Vista e posterior, ele está localizado no item [padrão](default-programs.md) do painel de controle de programas. Para programas [registrados](reg-middleware-apps.md) , ele executa as seguintes funções:

-   Habilita a opção de programas padrão para cada tipo de cliente (somente até o Windows 7).
-   Habilita o controle da exibição dos ícones, atalhos e entradas de menu do programa.
-   Fornece um conjunto de opções de programa predefinidas padrão. (Somente Windows XP Service Pack 1 (SP1))

Essa ferramenta é usada para os cinco tipos de cliente a seguir.

-   Navegador
-   Email
-   Programa de Messenging instantânea
-   Media player
-   Máquina virtual para Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Uma visão geral de definir o acesso do programa e padrões do computador

A página **Definir acesso do programa e padrões do computador** do Windows 8 é mostrada na captura de tela a seguir.

![captura de tela da exibição de entrada definir acesso do programa e padrões do computador](images/spad-initial.png)

Três opções de configuração possíveis são apresentadas ao usuário, com a opção para que os OEMs apresentem uma quarta opção intitulada "fabricante do computador".

-   [Microsoft Windows](#microsoft-windows)
-   [Não Microsoft](#non-microsoft)
-   [Personalizado](#custom)
-   [Fabricante do Computador](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

A configuração do **Microsoft Windows** consiste em um conjunto de programas padrão fornecidos com o Windows, conforme mostrado na captura de tela a seguir.

![captura de tela das opções definir acesso do programa e padrões da Microsoft](images/mspage.png)

A seleção da configuração do **Microsoft Windows** também permite a exibição de ícones, atalhos ou entradas de menu para cada programa registrado para qualquer um dos cinco tipos de cliente. Esses ícones, atalhos e entradas de menu estão disponíveis para o usuário no menu **Iniciar** ou na tela iniciar, na área de trabalho e em todos os outros locais aos quais foram adicionados.

### <a name="non-microsoft"></a>Não Microsoft

A configuração **que não** é da Microsoft, mostrada na captura de tela a seguir, é usada para aplicativos registrados no sistema do usuário que não são produzidos pela Microsoft. Esses aplicativos podem ser pré-instalados no sistema do usuário ou podem ser aplicativos que não são da Microsoft instalados pelo usuário.

> [!Note]  
> Os aplicativos devem ser registrados para serem exibidos nesta página. Para obter instruções sobre como registrar um aplicativo, consulte [registrando programas com tipos de cliente](reg-middleware-apps.md).

 

![captura de tela das opções definir acesso do programa e padrões que não são da Microsoft](images/nonmspage.png)

A seleção da opção **não Microsoft** também remove o acesso aos ícones, atalhos e entradas de menu dos programas da Microsoft listados na configuração do [Microsoft Windows](#microsoft-windows) para todos os tipos de clientes que os possuem. Esses ícones, atalhos e entradas de menu da Microsoft são removidos do menu **Iniciar** , da área de trabalho e de outros locais aos quais foram adicionados.

### <a name="custom"></a>Personalizado

A configuração **personalizada** , mostrada na captura de tela a seguir, permite que os usuários personalizem seus sistemas com qualquer combinação de programas da Microsoft e não Microsoft registrados como possibilidades padrão para os cinco tipos de cliente. Essa é a única das quatro opções disponíveis no Windows 2000 Service Pack 3 (SP3).

![captura de tela das opções de definir acesso do programa e padrões personalizados](images/custompage.png)

Todas as opções apresentadas no [Microsoft Windows](#microsoft-windows) e configurações [que não](#non-microsoft) são da Microsoft estão disponíveis para o usuário na seção **personalizada** , bem como outros aplicativos da Microsoft que não fazem parte do Windows. O botão de opção **usar meu navegador da Web atual** é preselecionado, conforme mostrado na captura de tela anterior. Não é possível determinar o navegador padrão atual da interface do usuário. Invocar links da Web ou arquivos no Windows é a única maneira de descobrir o navegador padrão atual.

Quando um usuário marca a caixa de seleção **habilitar o acesso a este programa** para um programa, os ícones, atalhos e entradas de menu do programa são exibidos no menu iniciar ou na tela iniciar, na área de trabalho ou em qualquer outro local onde eles foram instalados. Desmarcar essa opção deve remover esses ícones, atalhos e entradas de menu, no entanto, como essas opções se comportam totalmente para o fornecedor do aplicativo. O Windows não controla como o acesso é habilitado ou removido em toda a interface do usuário. Também é importante entender que não é necessário que os aplicativos se registrem para **definir o acesso do programa e os padrões do computador**.

### <a name="computer-manufacturer"></a>Fabricante do Computador

Uma quarta categoria intitulada "fabricante do computador" pode aparecer na janela SPAD em alguns sistemas. Os fabricantes de computadores podem optar por pré-configurar seus computadores com um conjunto personalizado de padrões, escolhendo entre as mesmas seleções disponíveis na configuração [personalizada](#custom) . (Para fins ilustrativos, um conjunto fictício de aplicativos chamado LitWare é registrado para uso com todos os tipos de clientes.) Um usuário pode retornar à configuração padrão do fabricante do computador a qualquer momento, escolhendo a opção **fabricante do computador** , conforme mostrado na seguinte captura de tela do Windows XP.

> [!Note]  
> Essa configuração não aparece em todos os sistemas. Para obter detalhes, consulte o OPK (Kit de pré-instalação OEM).

 

![captura de tela das opções definir acesso do programa e padrões do fabricante do computador](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>O valor do registro LastUserInitiatedDefaultChange

O valor LastUserInitiatedDefaultChange foi adicionado ao registro para ajudar os aplicativos a reconhecer e respeitar as opções padrão do usuário. O valor contém \_ dados binários reg na forma de uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contém a data e a hora (no UTC (tempo Universal Coordenado) da última vez em que o usuário alterou uma opção padrão por meio da ferramenta **Definir acesso do programa e padrões do computador** . Esse valor é encontrado na subchave a seguir.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

O cenário a seguir usa esse valor para um aplicativo que monitora as associações de arquivos.

1.  Um aplicativo registra internamente a hora em que foi definido pela última vez como o programa padrão para seu tipo de cliente (na instalação ou em um momento posterior).
2.  O aplicativo detecta que o programa padrão para seu tipo de cliente foi alterado para um programa que não seja o próprio ou o aplicativo que ele representa (no caso de programas auxiliares de segundo plano). Sem suporte em aplicativos no Windows 8.
3.  O aplicativo lê o valor de LastUserInitiatedDefaultChange (o carimbo de data/hora da última alteração padrão iniciada pelo usuário) e o compara ao valor de carimbo de data/hora que ele armazenou por sua própria escolha como padrão.
4.  Se LastUserInitiatedDefaultChange for posterior ao valor armazenado do aplicativo, nenhuma ação deverá ser tomada por esse aplicativo porque a alteração foi solicitada explicitamente pelo usuário por meio da ferramenta **Definir acesso e padrões do programa** .
5.  O aplicativo não monitora mais essa associação de arquivo até que ela seja novamente escolhida como padrão. Sem suporte em aplicativos no Windows 8.

Ao aderir a esse esquema, os desejos do usuário são respeitados e sua propriedade definitiva de seus sistemas é mantida.

## <a name="filtering-the-add-or-remove-programs-list"></a>Filtrando a lista Adicionar ou remover programas

> [!Note]  
> Esta seção se aplica ao Windows XP Service Pack 2 (SP2) e posterior e ao Windows Server 2003 e posterior.

 

No Windows XP e no Windows Server 2003, a lista de aplicativos exibida na guia **alterar ou remover programas** em **Adicionar ou remover programas** pode ser filtrada pelo usuário para excluir entradas de atualizações de aplicativos. Nessas versões do Windows, isso é feito por meio de uma caixa de seleção **Mostrar atualizações** na parte superior da janela. A opção **Mostrar atualizações** não é selecionada por padrão, portanto, as atualizações *não* são mostradas, a menos que o usuário opte por mostrá-las. As alterações no estado da caixa de seleção persistem quando **Adicionar ou remover programas** está fechado; se um usuário optar por mostrar as atualizações, elas continuarão sendo mostradas até que o usuário desmarque a caixa de seleção.

> [!Note]  
> A atualização do Windows XP SP2 em si é uma exceção à filtragem. Ele é sempre exibido, independentemente do estado da caixa de seleção.

 

No Windows Vista e versões posteriores, as atualizações de aplicativo são exibidas em uma página separada no painel de controle dedicado a atualizações sozinhas. Essa página é mostrada quando o usuário clica no link da tarefa **Exibir atualizações instaladas** . Não há nenhuma opção selecionável pelo usuário para mostrar atualizações na mesma página que os programas instalados. Apesar da alteração na interface do usuário, o mecanismo de registro como uma atualização para um programa instalado permanece o mesmo em versões anteriores do Windows.

Os aplicativos Microsoft e não Microsoft que usam o Windows Installer não precisam fazer mais nada para que suas atualizações sejam reconhecidas como atualizações. Aplicativos não Microsoft que não usam Windows Installer devem declarar determinados valores no registro como parte de sua instalação para serem reconhecidos como uma atualização para um programa existente.

O exemplo a seguir ilustra quais valores de registro a serem declarados para que uma instalação seja reconhecida como uma atualização de um programa existente.

1.  O aplicativo pai deve adicionar suas informações de desinstalação em uma subchave na subchave **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall** . Consulte o tópico de [instalação](/previous-versions/ms997548(v=msdn.10)) para obter mais informações sobre como usar a subchave **Uninstall** .
2.  Cada atualização para esse aplicativo pai também deve adicionar suas informações como uma subchave da subchave de **desinstalação** . Ele deve usar uma Convenção de nomenclatura específica de sua escolha, tentando evitar possíveis conflitos com outros programas. As convenções a seguir são reservadas como nomes de subchave pela Microsoft para uso com atualizações do Windows.
    -   IEUpdate
    -   OEUpdate
    -   "KB" seguido de seis dígitos, por exemplo, "KB123456"
    -   "Q" seguido por seis dígitos, por exemplo, "Q123456"
    -   Seis dígitos, por exemplo "123456"
3.  Além das informações de desinstalação padrão adicionadas para o aplicativo pai, as subchaves para cada atualização também devem incluir duas das três entradas a seguir. Seus valores são do tipo REG \_ sz.
    -   **ParentKeyName**. Esse valor é necessário. Este é o nome da subchave do pai declarada na etapa 1. Isso associa a atualização ao programa.
    -   **ParentDisplayName**. Esse valor é necessário. Se nenhuma subchave corresponder à chamada em ParentKeyName, esse valor será usado como um programa-pai de espaço reservado para ser exibido em **Adicionar ou remover programas**.
    -   **InstallDate**. Esse valor é opcional. Ele deve usar o formulário `yyyymmdd` para especificar a data. Essa data é usada para as informações **instaladas** exibidas ao lado da entrada da atualização na interface do usuário. Se não houver nenhuma entrada **InstallDate** ou se ela estiver presente, mas não tiver nenhum valor atribuído a ela, ocorrerá o seguinte:
        -   Versões do sistema operacional que não sejam o Windows Vista e o Windows 7: não há informações **instaladas no** são mostradas.
        -   Windows Vista e posterior: uma data padrão é usada. Esta é a data da "última modificação" para qualquer uma das entradas sob a subchave dessa atualização. Normalmente, esse é o dia em que a atualização foi adicionada ao registro. No entanto, como é uma data de "última modificação", qualquer alteração subseqüente feita em qualquer uma das entradas da subchave faz com que o valor de InstallDate seja alterado para a data da alteração.

O exemplo a seguir mostra as entradas de registro pertinentes para uma atualização para o aplicativo LitWare Deluxe.

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

Aplicativos que não são da Microsoft que não fornecem as informações apropriadas do registro, como atualizações geradas antes dessa opção, continuam sendo exibidos normalmente na lista de programas instalados e não são filtrados.

A filtragem de atualizações em versões do sistema operacional que não sejam o Windows Vista e o Windows 7 normalmente é uma configuração controlada pelo usuário e deve ser respeitada como tal por aplicativos. No entanto, em um ambiente corporativo, os administradores podem controlar se os usuários recebem a opção de filtrar atualizações por meio do valor do registro DontGroupPatches, conforme mostrado no exemplo a seguir.

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
| 0                                  | A caixa de seleção **Mostrar atualizações** é exibida para o usuário. A filtragem depende se o usuário marcou essa caixa ou não.                                                                                         |
| 1                                  | A caixa de seleção **Mostrar atualizações** é removida da interface do usuário. As atualizações não são filtradas na lista. Esse valor é essencialmente revertido para o comportamento do Windows XP SP1, antes que a funcionalidade **Mostrar atualizações** tenha sido introduzida. |
| A entrada DontGroupPatches não está presente | Isso é equivalente a definir o valor como 0.                                                                                                                                                                       |



 

DontGroupPatches não tem efeito no Windows Vista e no Windows 7, em que a interface do usuário não contém nenhuma caixa de seleção e as atualizações registradas são sempre filtradas.

> [!Note]  
> As políticas são definidas somente por administradores. Os aplicativos não devem alterar esse valor. Para obter mais informações sobre como definir um Política de Grupo baseado no registro, consulte [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page) ou [Windows Server política de grupo](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Recursos adicionais

-   [Registrando programas com tipos de cliente](reg-middleware-apps.md)
-   [Instalação](/previous-versions/ms997548(v=msdn.10))
-   [Configurando adicionar/remover programas com Windows Installer](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para associações de arquivo](fa-best-practices.md)
</dt> <dt>

[Cenário de exemplo de associação de arquivo](fa-sample-scenarios.md)
</dt> <dt>

[Diretrizes para o gerenciamento de aplicativos padrão no Windows Vista e posterior](vista-managing-defaults.md)
</dt> <dt>

[Programas padrão](default-programs.md)
</dt> </dl>

 

 
