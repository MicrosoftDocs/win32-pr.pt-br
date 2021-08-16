---
title: Criando um manipulador de limpeza de disco
description: Um tempo axioma comprovado e novamente no mundo dos computadores é que, independentemente do tamanho da capacidade de armazenamento do seu computador, você acabará preenchendo.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- manipuladores de limpeza de disco
- Limpeza de Disco
- DataDrivenCleaner
- registrar, manipuladores de limpeza de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ce7fc96e16cb27168e00196b65d48d378758a47594122cca978dc1a1f4de94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479885"
---
# <a name="creating-a-disk-cleanup-handler"></a>Criando um manipulador de limpeza de disco

Um tempo axioma comprovado e novamente no mundo dos computadores é que, independentemente do tamanho da capacidade de armazenamento do seu computador, você acabará preenchendo. Embora o tamanho médio do disco rígido de um computador tenha aumentado drasticamente ao longo do tempo, os aplicativos também cresceram de acordo, deixando os usuários buscando formas de criar mais espaço livre no disco rígido. O espaço disponível também é reduzido pelos vários arquivos temporários que os aplicativos criam para fins de backup ou desempenho. Quando o espaço em disco fica baixo, ele se torna necessário para reduzir a quantidade de espaço usado pelos aplicativos. O espaço em disco pode ser liberado usando uma variedade de meios, incluindo o seguinte:

-   Excluindo arquivos.
-   Compactando arquivos.
-   Movendo arquivos para um meio de backup.
-   Transferindo arquivos para um servidor remoto.

Os arquivos que são bons candidatos à limpeza incluem:

-   Arquivos que o usuário nunca precisará novamente.
-   Arquivos temporários que existem apenas por motivos de desempenho.
-   Arquivos que podem ser restaurados, se necessário, de um CD de instalação.
-   Arquivos de dados que possivelmente foram substituídos por versões mais recentes, como arquivos de backup antigos.
-   Arquivos mais antigos que não foram usados em muito tempo.

A exclusão é particularmente apropriada para os arquivos que o usuário nunca precisará novamente, por exemplo, arquivos que são armazenados temporariamente em cache por motivos de desempenho. A exclusão também é apropriada para arquivos que são facilmente restaurados, como arquivos gráficos que podem ser recarregados a partir de um CD de instalação. Os arquivos que o usuário pode precisar mais tarde ou que seriam difíceis de reconstruir são candidatos melhores para compactação ou backup.

Esperar que um usuário limpe manualmente o sistema de arquivos não é uma boa solução. O usuário pode não saber onde muitos arquivos estão localizados ou como reconhecer quais deles podem ser removidos com segurança. Além disso, há o risco de que o usuário possa excluir arquivos essenciais.

As facetas a seguir do utilitário limpeza de disco são discutidas neste tópico.

-   [o utilitário de limpeza de disco Windows](#the-windows-disk-cleanup-utility)
-   [Noções básicas de implementação](#implementation-basics)
    -   [Inicializar/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [Mostrarproperties](#showproperties)
    -   [Limpar](#purge)
    -   [Desativar](#deactivate)
-   [Registrando um manipulador de limpeza de disco](#registering-a-disk-cleanup-handler)
    -   [Registrando o CLSID de um manipulador](#registering-a-handlers-clsid)
    -   [Registrando um manipulador com o Gerenciador de limpeza de disco: geral](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [registrando um manipulador com o gerenciador de limpeza de disco: Windows 2000 ou sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Usando o objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
    -   [Exemplo de registro de um manipulador de limpeza de disco](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>o utilitário de limpeza de disco Windows

a partir do Windows 98, o sistema operacional Windows inclui a limpeza de disco, um utilitário que torna muito mais fácil para o usuário gerenciar o espaço disponível no disco rígido. O utilitário limpeza de disco foi projetado para liberar o máximo possível de espaço em disco e diminuir o risco de que o usuário exclua arquivos essenciais acidentalmente.

A limpeza de disco pode ser iniciada de três maneiras.

-   O usuário pode iniciar a limpeza de disco clicando em **Iniciar**; apontando para **todos os programas**, **acessórios** e **Ferramentas do sistema**; e, em seguida, clicando em **limpeza de disco**.
-   O sistema notifica o usuário com uma caixa de mensagem informando que o espaço em disco não utilizado atingiu o modo crítico. O limite de modo crítico para uma unidade maior que 2,25 gigabytes (GB) é 200 megabytes (MB). Os avisos subsequentes são fornecidos em 80, 50 e 1 MB. O usuário recebe a opção de liberar espaço em disco manualmente ou iniciar o utilitário de limpeza de disco.
-   o usuário pode ter o assistente de Windows tarefa agendada (conhecido como o assistente de manutenção em sistemas mais antigos) executar o utilitário limpeza de disco automaticamente em horários agendados.

O desafio básico inerente à limpeza de disco é liberar o máximo possível de espaço em disco sem excluir arquivos essenciais. Como não há uma maneira padrão de marcar arquivos para limpeza, nenhum aplicativo pode detectar e limpar de forma confiável todos os arquivos não essenciais. O utilitário limpeza de disco resolve esse problema, dividindo a operação de limpeza entre um único *Gerenciador de limpeza de disco* e uma coleção de *manipuladores de limpeza de disco*.

Quando o utilitário limpeza de disco é executado, o usuário vê a caixa de diálogo a seguir. (Se houver mais de um disco ou partição de disco no computador, primeiro será solicitado que o usuário escolha uma unidade antes que essa caixa de diálogo seja exibida.)

![captura de tela da caixa de diálogo limpar](images/cleanup1.png)

O Gerenciador de limpeza de disco faz parte do sistema operacional. Ele exibe a caixa de diálogo mostrada na ilustração anterior, manipula a entrada do usuário e gerencia a operação de limpeza. A seleção e a limpeza reais de arquivos desnecessários é feita pelos manipuladores de limpeza de disco individuais mostrados na caixa de listagem do Gerenciador de limpeza de disco. O usuário tem a opção de habilitar ou desabilitar manipuladores individuais marcando ou desmarcando sua caixa de seleção na interface do usuário do Gerenciador de limpeza de disco.

Cada manipulador é responsável por um conjunto bem definido de arquivos. Por exemplo, o manipulador selecionado na ilustração é responsável por limpar os arquivos de programa baixados. O manipulador selecionado na ilustração também fornece um botão **Exibir arquivos** . ao clicar no botão, o usuário pode solicitar que o manipulador exiba uma interface do usuário normalmente uma janela Windows Explorer que permite que o usuário especifique quais arquivos ou classes de arquivos limpar.

embora Windows seja fornecido com vários manipuladores de limpeza de disco, eles não são projetados para lidar com arquivos produzidos por outros aplicativos. Em vez disso, o Gerenciador de limpeza de disco é projetado para ser flexível e extensível, permitindo que qualquer desenvolvedor implemente e Registre seu próprio manipulador de limpeza de disco. Qualquer desenvolvedor pode estender os serviços de limpeza de disco disponíveis implementando e registrando um manipulador de limpeza de disco.

Todos os aplicativos que produzem arquivos temporários podem e devem implementar e registrar um manipulador de limpeza de disco. Isso fornece aos usuários uma maneira conveniente e confiável de gerenciar os arquivos temporários do aplicativo. Ao implementar o manipulador, você pode decidir quais arquivos são afetados e determinar como ocorre a limpeza real.

## <a name="implementation-basics"></a>Noções básicas de implementação

Os manipuladores de limpeza são objetos COM (Component Object Model de servidor) em processo. Windows fornece um objeto de manipulador existente chamado DataDrivenCleaner para seu uso. Você também pode optar por implementar um manipulador por conta própria para obter mais flexibilidade. Esses objetos permitem que você especifique como selecionar arquivos, liberar espaço em disco e, no caso de um manipulador implementado, exibir a interface do usuário opcional para um controle mais granular. Esta seção aborda a questão de implementar seu próprio manipulador. Para obter detalhes sobre o uso do objeto DataDrivenCleaner, consulte [usando o objeto DataDrivenCleaner](#using-the-datadrivencleaner-object).

Um manipulador de limpeza de disco deve executar essas cinco tarefas básicas.

-   Inicialize o objeto do manipulador.
-   Verifique o disco para determinar a quantidade de espaço em disco que pode ser liberada.
-   Exiba a interface do usuário para obter comentários de usuários sobre quais arquivos limpar. (Opcional)
-   Faça a limpeza.
-   Desligar.

para permitir que o gerenciador de limpeza de disco gerencie essas tarefas, um manipulador deve exportar [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) para o Windows 98 ou [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) para Windows Millennium Edition (Windows Me), Windows 2000 e Windows XP. Como **IEmptyVolumeCache2** é herdado de **IEmptyVolumeCache**, adicionar apenas o método adicional **InitializeEx**, relativamente pouco trabalho extra é necessário para implementar ambos. A menos que seu manipulador seja destinado a apenas um desses sistemas operacionais, ele deve exportar ambas as interfaces.

Para exportar essas interfaces, você deve implementar esses métodos correspondentes às cinco tarefas básicas.

-   [Inicializar/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [Mostrarproperties](#showproperties)
-   [Limpar](#purge)
-   [Desativar](#deactivate)

### <a name="initializeinitializeex"></a>Inicializar/InitializeEx

Os dois métodos de inicialização, que são bastante semelhantes, são chamados quando o utilitário de limpeza de disco é executado. o gerenciador de limpeza de disco Windows 98 chama o método [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) de um manipulador. o Windows Millennium Edition (Windows Me), Windows 2000 ou Windows o gerenciador de limpeza de disco do XP, no entanto, primeiro tenta chamar [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) e só usa **IEmptyVolumeCache:: Initialize** se [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) não é exposto pelo manipulador. O Gerenciador de limpeza de disco passa informações para o método, como a chave do registro do manipulador e o volume do disco a ser limpo.

Qualquer método pode retornar várias cadeias de caracteres de exibição e definir um ou mais sinalizadores. A principal diferença entre os dois métodos é como o texto exibido no gerenciador de limpeza de disco é tratado. As três cadeias de caracteres a seguir são afetadas.



| String       | Finalidade                                                                            | Inicializar                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Nome de Exibição | O nome do manipulador exibido na caixa de listagem do gerenciador de limpeza de disco.               | Se *ppwszDisplayName* **for NULL,** o valor padrão será recuperado do Registro. | Uma cadeia de caracteres localizada corretamente deve ser especificada *em ppwszDisplayName.* Nenhum valor do Registro é usado. |
| Descrição  | Texto descritivo exibido abaixo da caixa de listagem quando o nome do manipulador é selecionado. | Se *ppwszDescription* for **NULL,** o valor padrão será recuperado do Registro. | Uma cadeia de caracteres localizada corretamente deve ser especificada *em ppwszDescription.* Nenhum valor do Registro é usado. |
| Texto do botão  | Texto para o botão opcional que permite aos usuários exibir a interface do usuário do manipulador.        | Nenhum parâmetro disponível. Deve ser especificado no Registro.                           | Uma cadeia de caracteres localizada corretamente deve ser especificada *em ppwszBtnText,* nenhum valor do Registro é usado.     |



 

O *parâmetro pdwFlags* encontrado em ambos os métodos de inicialização reconhece o mesmo conjunto de sinalizadores. Dois desses sinalizadores são passados para o método pelo gerenciador de limpeza de disco.

-   **EVCF \_ SETTINGSMODE**

    Se o gerenciador de limpeza de disco estiver sendo executado de acordo com um agendamento, ele definirá o sinalizador **EVCF \_ SETTINGSMODE.** Se esse sinalizador for definido, o gerenciador de limpeza de disco não chamará os métodos [GetSpaceUsed,](#getspaceused) [Purge](#purge)ou [ShowProperties.](#showproperties) O método [**Initialize ou**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) do manipulador deve manipular todas as tarefas normalmente executadas por [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) e [**Limpar**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge). Como não há nenhuma oportunidade para comentários do usuário, somente os arquivos que são extremamente seguros de limpeza devem ser tocados. Você deve ignorar o parâmetro *pcwszVolume* do método de inicialização e limpar arquivos não precisos, independentemente da unidade em que eles estão.

-   **EVCF \_ OUTOFDISKSPACE**

    Se o **sinalizador EVCF \_ OUTOFDISKSPACE** estiver definido, a unidade de disco do usuário será muito curta. O manipulador deve ser agressivo quanto à exclusão de arquivos, mesmo que isso resulta em uma perda de desempenho. No entanto, o manipulador obviamente não deve excluir arquivos que causaria falha em um aplicativo ou que o usuário perca dados.

Os sinalizadores restantes são definidos pelo manipulador de limpeza de disco e retornados para o gerenciador de limpeza de disco. Para obter mais informações, consulte as páginas de referência de método [**para IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) e [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   EVCF \_ DONTSHOWIFZERO

    Exibir o manipulador na caixa de listagem do gerenciador de limpeza de disco somente se o valor retornado por [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) indicar que o manipulador pode liberar algum espaço em disco.

-   EVCF \_ ENABLEBYDEFAULT

    Especifica que o manipulador está habilitado por padrão. Ele será executado sempre que uma limpeza de disco ocorrer, a menos que o usuário o desabilite desempaque sua caixa de seleção na lista de manipuladores do gerenciador de limpeza de disco.

-   EVCF \_ ENABLEBYDEFAULT \_ AUTO

    Especifica que o manipulador é habilitado automaticamente para ser executado durante as limpezas agendadas.

-   EVCF \_ HASSETTINGS

    De definir esse sinalizador se o manipulador tiver uma interface do usuário a ser exibida. Em resposta, o gerenciador de limpeza de disco exibe um botão quando esse manipulador é selecionado na caixa de listagem. Se esse botão for clicado, o gerenciador de limpeza de disco [**chamará ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties).

-   EVCF \_ REMOVEFROMLIST

    Exclua o nome do manipulador da lista de manipuladores disponíveis depois que o manipulador tiver sido executado uma vez. As informações do registro do manipulador também são excluídas.

### <a name="getspaceused"></a>GetSpaceUsed

O gerenciador de limpeza de disco chama esse método para determinar quanto espaço um manipulador de limpeza de disco pode liberar potencialmente. Em seguida, o gerenciador de limpeza de disco exibe esse valor à direita do nome do manipulador na caixa de listagem. Essa operação é executada em todos os manipuladores registrados com o gerenciador de limpeza de disco quando o gerenciador é lançado e antes que a interface do usuário principal do gerenciador seja exibida. Quando [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) é chamado, o manipulador deve verificar os arquivos pelos quais ele é responsável, determinar quais deles são candidatos à limpeza e retornar a quantidade de espaço em disco que ele pode liberar.

Como a verificação pode ser um processo demorado, o gerenciador de limpeza de disco usa o parâmetro *picb* desse método para passar um ponteiro para uma interface [**IEmptyVolumeCacheCallBack.**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) O manipulador usa a interface periodicamente durante a verificação para chamar [**IEmptyVolumeCacheCallBack::ScanProgress,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)que atende a duas finalidades.

-   Permite que o gerenciador de limpeza de disco atualize uma barra de progresso, informando ao usuário como a verificação está progredindo.
-   Notifica o manipulador para interromper a verificação caso o  botão Cancelar da janela de progresso seja clicado. Esse evento de botão não é comunicado diretamente ao manipulador; em vez disso, o gerenciador de limpeza de disco retorna E ABORT na próxima vez que \_ [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) chamar [**IEmptyVolumeCacheCallBack::ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="showproperties"></a>ShowProperties

Antes de iniciar a limpeza, o manipulador pode exibir uma interface do usuário normalmente na forma de uma janela do gerenciador do Windows que permite que o usuário veja uma lista de arquivos ou classes de arquivos selecionados para limpeza pelo manipulador. Se o manipulador define o sinalizador **EVCF \_ HASSETTINGS** quando [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) ou [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) é chamado, o usuário pode solicitar a interface do usuário clicando no botão exibido para essa finalidade no gerenciador de limpeza de disco. O texto do botão varia de manipulador para manipulador, mas "Exibir Arquivos", "Exibir Páginas" e "Opções" são rótulos comuns.

Quando o botão é clicado, o gerenciador de limpeza de disco chama [**ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) para solicitar ao manipulador para exibir a interface do usuário. A interface do usuário deve ser criada como um filho da janela cujo handle é passado no parâmetro *hwnd* do método **ShowProperties.**

### <a name="purge"></a>Limpar

O gerenciador de limpeza de disco chama o método [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) do manipulador para definir a limpeza em movimento. O parâmetro *picb* do método é um ponteiro para a interface [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) do gerenciador de limpeza de disco. Assim como com o [**método GetSpaceUsed,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) o manipulador deve usar a interface de retorno de chamada periodicamente para relatar seu progresso e consultar o gerenciador de limpeza de disco se o usuário clicou **em Cancelar**. No entanto, observe que o método **Purge** deve chamar [**IEmptyVolumeCacheCallBack::P eProgress,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress)não [**ScanProgress.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)

### <a name="deactivate"></a>Desativar

O [**método Desativar é**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) chamado quando o gerenciador de limpeza de disco está se preparando para desligar. O manipulador deve executar as tarefas de limpeza necessárias e retornar. Se você não quiser que o manipulador seja executado novamente, defina o sinalizador **\_ REMOVEFROMLIST EVCF** no parâmetro *pdwFlags do* método de inicialização. Se esse sinalizador for definido, o gerenciador de limpeza de disco removerá o manipulador de sua lista e excluirá as entradas do Registro do manipulador. Você deve adicionar novamente as entradas do Registro para executar o manipulador novamente. Normalmente, esse sinalizador é usado para manipuladores que são executados apenas uma vez.

## <a name="registering-a-disk-cleanup-handler"></a>Registrando um manipulador de limpeza de disco

Para adicionar um manipulador à lista do gerenciador de limpeza de disco, determinadas chaves e valores devem ser adicionados ao Windows registro.

-   [Registrando o CLSID de um manipulador](#registering-a-handlers-clsid)
-   [Registrando um manipulador com o Gerenciador de Limpeza de Disco: Geral](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registrando um manipulador com o Gerenciador de Limpeza de Disco: Windows 2000 ou sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Usando o objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
-   [Exemplo de registro de um manipulador de limpeza de disco](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registrando o CLSID de um manipulador

Assim como com todos os objetos COM, o GUID e a DLL do objeto do manipulador devem ser registrados na **chave CLSID** em **CLASSES HKEY \_ \_ ROOT**. Você também pode registrar um ícone exibido ao lado do nome do manipulador na caixa de listagem do gerenciador de limpeza de disco, mas isso é opcional. O exemplo a seguir mostra as chaves, os valores e os dados envolvidos.

```
HKEY_CLASSES_ROOT
   CLSID
      Handler's GUID
         DefaultIcon
            (Default) = Handler's Icon Path, Icon Index
         InprocServer32
            (Default) = Handler's DLL path
            ThreadingModel = Apartment
```

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registrando um manipulador com o Gerenciador de Limpeza de Disco: Geral

Para concluir o registro, um manipulador deve adicionar uma chave que mantém suas especificações, conforme mostrado aqui. O restante desta seção aborda o conteúdo dessa chave.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Handler's Key
```

Em geral, o nome da chave que mantém as particularidades de um manipulador é nomeado para o tipo de arquivo que ele trata, como Arquivos de Programas Baixados, mas isso não é um requisito. A tabela a seguir detalha os possíveis valores encontrados nessa chave.

> [!Note]  
> Somente o valor Padrão que especifica o CLSID (identificador de classe) do manipulador é necessário, todos os outros valores são opcionais.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Type</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Padrão</td>
<td>REG_SZ</td>
<td>CLSID do manipulador conforme registrado em <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Texto para o botão opcional que os usuários podem clicar para exibir a interface do usuário do manipulador. O & caractere pode ser colocado antes de um caractere para atribuir um atalho de teclado para o botão. O valor AdvancedButtonText é ignorado por manipuladores que expõem <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx.</strong></a></td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Linha de comando especificando um arquivo executável e parâmetros opcionais de linha de comando. Essa linha de comando é executado na conclusão da limpeza do disco.</td>
</tr>
<tr class="even">
<td>Csidl</td>
<td>REG_DWORD</td>
<td>Um identificador independente do sistema para uma pasta especial a ser incluído na pesquisa de arquivos. Esse valor deve ser inserido como um valor numérico, por exemplo, 0x0000001c em vez de CSIDL_LOCAL_APPDATA. Para ver uma lista de valores possíveis, consulte <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Somente um único valor pode ser usado.<br/> Se o valor pasta for especificado, o local indicado pelo valor CSIDL será anexado a essas informações para compor um caminho de pesquisa. Por exemplo, considere o cenário a seguir.<br/>
<ul>
<li>O valor CSIDL é especificado como 0x0000000d (CSIDL_MYMUSIC)</li>
<li>A pasta Minha Música está localizada em C:\Documents e Configurações\<em>nome de usuário</em>\My Music</li>
<li>O valor De pasta &quot; contém Jazz\Jazzs&quot;</li>
</ul>
O resultado desse cenário é que o manipulador de limpeza de disco pesquisa a pasta C:\Documents e Configurações\<em>username</em>\My Music\Jazz\Countrys. Observe que a barra que precede o valor Pasta será adicionada se não estiver presente.<br/></td>
</tr>
<tr class="odd">
<td>Descrição</td>
<td>REG_SZ</td>
<td>Texto descritivo exibido abaixo da caixa de listagem do gerenciador de limpeza de disco quando o nome do manipulador é selecionado. Aqui, você pode explicar o que o manipulador faz, com quais arquivos ele se preocupa e com quais outras informações o usuário se preocupa. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> não for exposto pelo manipulador, esse texto poderá ser substituído por meio do método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> do manipulador especificando uma cadeia de caracteres alternativa no parâmetro <em>ppwszDescription</em> quando o método for chamado.</td>
</tr>
<tr class="even">
<td>Exibir</td>
<td>REG_SZ</td>
<td>O nome do manipulador a ser exibido na caixa de listagem do gerenciador de limpeza de disco. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> não for exposto pelo manipulador, esse texto poderá ser substituído por meio do método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> do manipulador especificando uma cadeia de caracteres alternativa no parâmetro <em>ppwszDisplayName</em> quando o método for chamado.</td>
</tr>
<tr class="odd">
<td>Filelist</td>
<td>REG_SZ ou REG_MULTI_SZ</td>
<td>Uma lista de arquivos pesquisados e limpos por esse manipulador. Você pode especificar curingas usando o ? ou * caracteres. Se o valor for do tipo REG_SZ, várias extensões serão separadas usando o | ou : caracteres, sem espaços em nenhum dos lados deles.<br/> Se o DDEVCF_REMOVEDIRS sinalizador for definido no valor Sinalizadores, esses valores poderão especificar nomes de diretório, bem como arquivos.<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>Sinalizadores que controlam elementos do procedimento de pesquisa e limpeza. Um ou mais dos valores a seguir.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Pesquise e remova recursivamente.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Depois que o manipulador for executado uma vez, remova-o do Registro.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Remova os arquivos que atendem aos critérios de pesquisa mesmo se eles são somente leitura.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Remova os arquivos que atendem aos critérios de pesquisa mesmo se eles são arquivos do sistema.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Remova os arquivos que atendem aos critérios de pesquisa mesmo se eles são arquivos ocultos.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Não ex exibir esse manipulador no gerenciador de limpeza de disco se nenhum arquivo corresponder aos critérios de pesquisa.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Corresponder o valor FileList aos diretórios e remover as correspondeções e todos os seus subdireários.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Execute esse manipulador somente se o espaço em disco disponível estiver abaixo do valor crítico, determinado pelo gerenciador de limpeza de disco definindo o sinalizador EVCF_OUTOFDISKSPACE por meio de <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> ou <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a>.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Remova o diretório pai dos arquivos especificados depois que o limpeza for executado.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Use o valor LastAccess, se fornecido, para determinar quais arquivos devem ser limpos. Esse sinalizador é ignorado ao usar <a href="#using-the-datadrivencleaner-object">o DataDrivenCleaner,</a> qualquer valor LastAccess fornecido sempre é usado.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pasta</td>
<td>REG_SZ, REG_MULTI_SZ ou REG_EXPAND_SZ</td>
<td>Uma pasta ou pastas específicas para pesquisar itens correspondentes a entradas no valor FileList. Você pode especificar curingas usando o ? ou * caracteres. Se o valor for do tipo REG_SZ, vários nomes de pasta serão separados usando o | caractere, sem espaços em nenhum dos lados dele.<br/> Se um valor CSIDL estiver presente, somente uma pasta poderá ser especificada nesse valor. O local indicado pelo valor CSIDL é anexado a esse caminho de pasta para compor um caminho de pesquisa. Para ver um exemplo, consulte a descrição do valor CSIDL.<br/> Se esse valor estiver ausente no Windows Vista Service Pack 1 (SP1) e posterior, o manipulador de limpeza será ignorado e retornará S_FALSE na inicialização.<br/> Se esse valor estiver ausente na versão original do Windows Vista e anterior, a pasta raiz do volume atual será usada. O DDEVCF_DOSUBDIRS sinalizador é necessário nesse caso para pesquisar toda a unidade. Sem ele, somente a pasta raiz em si é pesquisada.<br/> Uma unidade ou unidades devem ser especificadas. Isso pode ser fornecido por meio do valor CSIDL ou por meio de uma REG_EXPAND_SZ de caracteres. No entanto, a unidade a ser pesquisada deve ser especificada no nome da pasta. Use ?: para pesquisar a pasta na unidade atual.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ ou REG_EXPAND_SZ</td>
<td>O caminho para o recurso do qual obter um ícone a ser usado em associação com o manipulador.</td>
</tr>
<tr class="odd">
<td>Lastaccess</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>O número de dias que devem ter decorrido desde que um arquivo foi acessado pela última vez ou um diretório foi criado para que esse arquivo ou diretório seja considerado para limpeza.</td>
</tr>
<tr class="even">
<td>Prioridade</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>Determina a ordem em que o manipulador é executado em relação a outros manipuladores. Quanto maior o número, mais cedo no processo que o manipulador executa. Não há nenhum intervalo definido, nenhum número é aceitável.</td>
</tr>
<tr class="odd">
<td>Propertybag</td>
<td>REG_SZ</td>
<td>O CLSID de um recurso usado para fornecer texto localizado para o nome de exibição, a descrição e o texto do botão. Esse recurso é útil na situação em que um manipulador não implementa <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> e o manipulador está sendo executado no Microsoft Windows NT ou Windows XP.<br/> O gerenciador de limpeza de disco primeiro verifica se a rotina de inicialização do manipulador retornou essas cadeias de caracteres, como seria o caso quando <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> é implementado. Falhando, o gerenciador se transforma em um pacote de propriedades chamado nesse valor. Se nenhum tiver sido fornecido, ele recuperará o texto do Registro.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>Ao executar o arquivo executável do gerenciador de limpeza de disco Cleanmgr.exe de uma linha de comando, você pode declarar perfis de <em>limpeza</em>. Esses perfis são compostos por um subconjunto dos manipuladores disponíveis e têm um rótulo numérico exclusivo. Isso permite automatizar a execução de diferentes conjuntos de manipuladores em momentos diferentes.<br/> A linha &quot; de comandocleanmgr.exe /sageset:<strong>nnnn,</strong>em que &quot; <strong>nnnn</strong> é um rótulo numérico exclusivo, exibe uma interface do usuário permitindo que você escolha os manipuladores a serem incluídos nesse perfil. Além de definir o perfil, o parâmetro sageset também grava um valor chamado StateFlags<strong>nnnn,</strong>em que <strong>nnnn</strong> é o rótulo usado no parâmetro , em todas as sub-chaves em <strong>VolumeCaches</strong>. Há dois valores de dados possíveis para essas entradas.
<ul>
<li>0: Não execute esse manipulador quando esse perfil for executado.</li>
<li>2: Inclua esse manipulador quando esse perfil for executado.</li>
</ul>
<br/> Por exemplo, suponha que a linha de &quot; comandocleanmgr.exe /sageset:1234 &quot; seja executado. Na interface do usuário apresentada, o <strong></strong>usuário escolhe Arquivos de Programas Baixados, mas não escolhe <strong>Arquivos temporários da Internet.</strong> Os valores a seguir são gravados no Registro.<br/>
<pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Downloaded Program Files
                        StateFlags1234 = 0x00000002
                     Internet Cache Files
                        StateFlags1234 = 0x00000000</code></pre>
<br/> A linha &quot; de comandocleanmgr.exe /sagerun:<strong>nnnn</strong>, em que o valor de nnnn corresponde ao rótulo declarado com o parâmetro sageset, executa todos os &quot; manipuladores selecionados nesse perfil. <strong></strong><br/> Um valor StateFlags genérico é gravado no Registro quando a Limpeza de Disco é executado normalmente. Esse valor simplesmente armazena o estado (marcado ou desmarcado) do manipulador na última vez em que ele foi apresentado como uma opção para o usuário. Há dois valores de dados possíveis para essas entradas.
<ul>
<li>0: O manipulador não foi selecionado.</li>
<li>1: o manipulador foi selecionado.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registrando um manipulador com o Gerenciador de Limpeza de Disco: Windows 2000 ou sistemas posteriores

Especificar texto de exibição no Registro pode dificultar a localização do software. Por esse motivo, Windows 2000 e Windows XP suportam a interface [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) com seu método de inicialização preferencial [**InitializeEx.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) No Windows 2000 ou posterior, sempre é feita uma tentativa de chamar **IEmptyVolumeCache2::InitializeEx** antes [**de IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize). O sistema só usará **Inicializar** para inicializar um manipulador **se IEmptyVolumeCache2** não for exposto.

Em relação ao Registro, a única diferença no Windows 2000 ou posterior é que você pode omitir os valores AdvancedButtonText, Display e Description quando [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) é exposto pelo manipulador. Esses valores, que contêm texto localizado corretamente, são fornecidos ao gerenciador de limpeza de disco quando ele chama **InitializeEx**.

### <a name="using-the-datadrivencleaner-object"></a>Usando o objeto DataDrivenCleaner

Um manipulador de limpeza de disco básico, chamado DataDrivenCleaner, é fornecido pelo sistema operacional. Para usar esse objeto como um manipulador em vez de implementar seu próprio, use o CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} como o valor Padrão para a sub-chave do manipulador em **VolumeCaches,** conforme descrito em Registrando um manipulador com o Gerenciador de Limpeza de [Disco: Geral.](#registering-a-handler-with-the-disk-cleanup-manager-general)

O DataDrivenCleaner não expõe [**IEmptyVolumeCache2,**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)portanto, os valores de Exibição e Descrição são fornecidos por meio do Registro. Ao declarar essas cadeias de caracteres, esteja ciente de que isso pode causar problemas de localização. O texto localizado pode ser fornecido por meio do valor PropertyBag. O valor AdvancedButtonText é ignorado, pois nenhuma interface do usuário e, portanto, nenhum botão para exibi-lo, está disponível para esse manipulador.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Exemplo de registro de um manipulador de limpeza de disco

A seguir, é possível ver um exemplo de registro para um manipulador de limpeza de disco implementado pela Telefone Company. Esse manipulador implementa [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) e [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)e, portanto, fornece valores AdvancedButtonText, Description e Display caso seja usado em um computador executando Windows 98. O manipulador combina os valores CSIDL e Folder para pesquisar arquivos no diretório C: Arquivos de Programas O diretório Temp da Empresa Telefone e o sinalizador \\ \\ \\ DOSUBDIRS de DDEVCF são definidos para que seus subdireários também sejam \_ pesquisados. Somente os arquivos com extensões .tmp e .tpc são considerados para limpeza e o sinalizador \_ LASTACCESS PRIVADO DDEVCF é definido para que, fora desses arquivos, somente aqueles que não foram acessados por 14 dias ou mais sejam \_ considerados. O sinalizador DDEVCF DONTSHOWIFZERO também é definido para que o manipulador não apareça na lista, a menos que tenha encontrado candidatos \_ de limpeza.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     The Phone Company Files
                        (Default) = {the CLSID GUID}
                        AdvancedButtonText = &View Files
                        CleanupString = c:\tpc.exe
                        CSIDL = 0x00000026
                        Description = Old temporary files.
                        Display = The Phone Company Files
                        FileList = *.tmp|*.tpc
                        Flags = 0x10000021
                        Folder = \The Phone Company\Temp
                        IconPath = c:\Program Files\The Phone Company\tpc.dll,2
                        LastAccess = 0x0000000e
                        Priority = 200
                        PropertyBag = {Property Bag CLSID GUID}
```

 

