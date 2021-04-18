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
ms.openlocfilehash: 30584439ae2c38ae8a9b7106dae96f69eea5df37
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105781164"
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

-   [O utilitário de limpeza de disco do Windows](#the-windows-disk-cleanup-utility)
-   [Noções básicas de implementação](#implementation-basics)
    -   [Inicializar/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [Mostrarproperties](#showproperties)
    -   [Limpar](#purge)
    -   [Desativar](#deactivate)
-   [Registrando um manipulador de limpeza de disco](#registering-a-disk-cleanup-handler)
    -   [Registrando o CLSID de um manipulador](#registering-a-handlers-clsid)
    -   [Registrando um manipulador com o Gerenciador de limpeza de disco: geral](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [Registrando um manipulador com o Gerenciador de limpeza de disco: Windows 2000 ou sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Usando o objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
    -   [Exemplo de registro de um manipulador de limpeza de disco](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>O utilitário de limpeza de disco do Windows

A partir do Windows 98, o sistema operacional Windows inclui a limpeza de disco, um utilitário que torna muito mais fácil para o usuário gerenciar o espaço disponível no disco rígido. O utilitário limpeza de disco foi projetado para liberar o máximo possível de espaço em disco e diminuir o risco de que o usuário exclua arquivos essenciais acidentalmente.

A limpeza de disco pode ser iniciada de três maneiras.

-   O usuário pode iniciar a limpeza de disco clicando em **Iniciar**; apontando para **todos os programas**, **acessórios** e **Ferramentas do sistema**; e, em seguida, clicando em **limpeza de disco**.
-   O sistema notifica o usuário com uma caixa de mensagem informando que o espaço em disco não utilizado atingiu o modo crítico. O limite de modo crítico para uma unidade maior que 2,25 gigabytes (GB) é 200 megabytes (MB). Os avisos subsequentes são fornecidos em 80, 50 e 1 MB. O usuário recebe a opção de liberar espaço em disco manualmente ou iniciar o utilitário de limpeza de disco.
-   O usuário pode ter o assistente de tarefa agendada do Windows (conhecido como o assistente de manutenção em sistemas mais antigos) executar o utilitário limpeza de disco automaticamente em horários agendados.

O desafio básico inerente à limpeza de disco é liberar o máximo possível de espaço em disco sem excluir arquivos essenciais. Como não há uma maneira padrão de marcar arquivos para limpeza, nenhum aplicativo pode detectar e limpar de forma confiável todos os arquivos não essenciais. O utilitário limpeza de disco resolve esse problema, dividindo a operação de limpeza entre um único *Gerenciador de limpeza de disco* e uma coleção de *manipuladores de limpeza de disco*.

Quando o utilitário limpeza de disco é executado, o usuário vê a caixa de diálogo a seguir. (Se houver mais de um disco ou partição de disco no computador, primeiro será solicitado que o usuário escolha uma unidade antes que essa caixa de diálogo seja exibida.)

![captura de tela da caixa de diálogo limpar](images/cleanup1.png)

O Gerenciador de limpeza de disco faz parte do sistema operacional. Ele exibe a caixa de diálogo mostrada na ilustração anterior, manipula a entrada do usuário e gerencia a operação de limpeza. A seleção e a limpeza reais de arquivos desnecessários é feita pelos manipuladores de limpeza de disco individuais mostrados na caixa de listagem do Gerenciador de limpeza de disco. O usuário tem a opção de habilitar ou desabilitar manipuladores individuais marcando ou desmarcando sua caixa de seleção na interface do usuário do Gerenciador de limpeza de disco.

Cada manipulador é responsável por um conjunto bem definido de arquivos. Por exemplo, o manipulador selecionado na ilustração é responsável por limpar os arquivos de programa baixados. O manipulador selecionado na ilustração também fornece um botão **Exibir arquivos** . Ao clicar no botão, o usuário pode solicitar que o manipulador exiba uma interface do usuário normalmente uma janela do Windows Explorer que permite ao usuário especificar quais arquivos ou classes de arquivos limpar.

Embora o Windows venha com vários manipuladores de limpeza de disco, eles não são projetados para lidar com arquivos produzidos por outros aplicativos. Em vez disso, o Gerenciador de limpeza de disco é projetado para ser flexível e extensível, permitindo que qualquer desenvolvedor implemente e Registre seu próprio manipulador de limpeza de disco. Qualquer desenvolvedor pode estender os serviços de limpeza de disco disponíveis implementando e registrando um manipulador de limpeza de disco.

Todos os aplicativos que produzem arquivos temporários podem e devem implementar e registrar um manipulador de limpeza de disco. Isso fornece aos usuários uma maneira conveniente e confiável de gerenciar os arquivos temporários do aplicativo. Ao implementar o manipulador, você pode decidir quais arquivos são afetados e determinar como ocorre a limpeza real.

## <a name="implementation-basics"></a>Noções básicas de implementação

Os manipuladores de limpeza são objetos COM (Component Object Model de servidor) em processo. O Windows fornece um objeto de manipulador existente chamado DataDrivenCleaner para seu uso. Você também pode optar por implementar um manipulador por conta própria para obter mais flexibilidade. Esses objetos permitem que você especifique como selecionar arquivos, liberar espaço em disco e, no caso de um manipulador implementado, exibir a interface do usuário opcional para um controle mais granular. Esta seção aborda a questão de implementar seu próprio manipulador. Para obter detalhes sobre o uso do objeto DataDrivenCleaner, consulte [usando o objeto DataDrivenCleaner](#using-the-datadrivencleaner-object).

Um manipulador de limpeza de disco deve executar essas cinco tarefas básicas.

-   Inicialize o objeto do manipulador.
-   Verifique o disco para determinar a quantidade de espaço em disco que pode ser liberada.
-   Exiba a interface do usuário para obter comentários de usuários sobre quais arquivos limpar. (Opcional)
-   Faça a limpeza.
-   Desligar.

Para permitir que o Gerenciador de limpeza de disco gerencie essas tarefas, um manipulador deve exportar o [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) para Windows 98 ou [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) para Windows Millennium Edition (Windows Me), Windows 2000 e Windows XP. Como **IEmptyVolumeCache2** é herdado de **IEmptyVolumeCache**, adicionar apenas o método adicional **InitializeEx**, relativamente pouco trabalho extra é necessário para implementar ambos. A menos que seu manipulador seja destinado a apenas um desses sistemas operacionais, ele deve exportar ambas as interfaces.

Para exportar essas interfaces, você deve implementar esses métodos correspondentes às cinco tarefas básicas.

-   [Inicializar/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [Mostrarproperties](#showproperties)
-   [Limpar](#purge)
-   [Desativar](#deactivate)

### <a name="initializeinitializeex"></a>Inicializar/InitializeEx

Os dois métodos de inicialização, que são bastante semelhantes, são chamados quando o utilitário de limpeza de disco é executado. O Gerenciador de limpeza de disco do Windows 98 chama o método [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) de um manipulador. O Windows Millennium Edition (Windows me), o Windows 2000 ou o Gerenciador de limpeza de disco do Windows XP, no entanto, primeiro tenta chamar [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) e só usa **IEmptyVolumeCache:: Initialize** se [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) não é exposto pelo manipulador. O Gerenciador de limpeza de disco passa informações para o método, como a chave do registro do manipulador e o volume do disco a ser limpo.

Qualquer um dos métodos pode retornar várias cadeias de caracteres de exibição e definir um ou mais sinalizadores. A principal diferença entre os dois métodos é como o texto exibido no Gerenciador de limpeza de disco é manipulado. As três cadeias de caracteres a seguir são afetadas.



| String       | Finalidade                                                                            | Inicializar                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Nome de exibição | O nome do manipulador exibido na caixa de listagem do Gerenciador de limpeza de disco.               | Se *ppwszDisplayName* for **NULL**, o valor padrão será recuperado do registro. | Uma cadeia de caracteres localizada corretamente deve ser especificada em *ppwszDisplayName* nenhum valor de registro é usado. |
| Descrição  | Texto descritivo exibido abaixo da caixa de listagem quando o nome do manipulador é selecionado. | Se *ppwszDescription* for **NULL**, o valor padrão será recuperado do registro. | Uma cadeia de caracteres localizada corretamente deve ser especificada em *ppwszDescription* nenhum valor de registro é usado. |
| Texto do botão  | Texto do botão opcional que permite aos usuários exibir a interface do usuário do manipulador.        | Nenhum parâmetro disponível. Deve ser especificado no registro.                           | Uma cadeia de caracteres localizada corretamente deve ser especificada em *ppwszBtnText* nenhum valor de registro é usado.     |



 

O parâmetro *pdwFlags* encontrado em ambos os métodos de inicialização reconhece o mesmo conjunto de sinalizadores. Dois desses sinalizadores são passados para o método pelo Gerenciador de limpeza de disco.

-   **EVCF \_ settingsmode**

    Se o Gerenciador de limpeza de disco estiver sendo executado em um agendamento, ele definirá o sinalizador **EVCF \_ settingsmode** . Se esse sinalizador estiver definido, o Gerenciador de limpeza de disco não chamará os métodos [GetSpaceUsed](#getspaceused), [Purge](#purge)ou [showProperties](#showproperties) . O método [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) ou [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) do manipulador deve lidar com todas as tarefas normalmente executadas por [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) e [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge). Como não há oportunidade de comentários do usuário, somente os arquivos extremamente seguros para limpeza devem ser tocadas. Você deve ignorar o parâmetro *pcwszVolume* do método de inicialização e limpar os arquivos desnecessários, independentemente de em qual unidade eles estão.

-   **EVCF \_ OUTOFDISKSPACE**

    Se o sinalizador **EVCF \_ OUTOFDISKSPACE** for definido, a unidade de disco do usuário será extremamente pequena de espaço. O manipulador deve ser agressivo em relação à exclusão de arquivos, mesmo que ele resulte em uma perda de desempenho. No entanto, o manipulador obviamente não deve excluir arquivos que poderiam causar uma falha no aplicativo ou que o usuário perca dados.

Os sinalizadores restantes são definidos pelo manipulador de limpeza de disco e retornados para o Gerenciador de limpeza de disco. Para obter mais informações, consulte as páginas de referência de método para [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) e [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   EVCF \_ DONTSHOWIFZERO

    Exiba o manipulador na caixa de listagem do Gerenciador de limpeza de disco somente se o valor retornado por [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) indicar que o manipulador pode liberar algum espaço em disco.

-   EVCF \_ ENABLEBYDEFAULT

    Especifica que o manipulador está habilitado por padrão. Ele será executado toda vez que uma limpeza de disco ocorrer, a menos que o usuário a desative, desmarcando sua caixa de seleção na lista de manipuladores do Gerenciador de limpeza de disco.

-   EVCF \_ ENABLEBYDEFAULT \_ auto

    Especifica que o manipulador é habilitado automaticamente para execução durante as limpezas agendadas.

-   EVCF \_ HASSETTINGS

    Defina esse sinalizador se o seu manipulador tiver uma interface do usuário para exibir. Em resposta, o Gerenciador de limpeza de disco exibe um botão quando esse manipulador é selecionado na caixa de listagem. Se esse botão for clicado, o Gerenciador de limpeza de disco chamará [**mostrarproperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties).

-   EVCF \_ REMOVEFROMLIST

    Exclua o nome do manipulador da lista de manipuladores disponíveis depois que o manipulador tiver sido executado uma vez. As informações de registro do manipulador também são excluídas.

### <a name="getspaceused"></a>GetSpaceUsed

O Gerenciador de limpeza de disco chama esse método para determinar a quantidade de espaço que um manipulador de limpeza de disco pode liberar. Em seguida, o Gerenciador de limpeza de disco exibe esse valor à direita do nome do manipulador na caixa de listagem. Essa operação é executada em todos os manipuladores registrados com o Gerenciador de limpeza de disco quando o gerente é iniciado e antes da interface do usuário principal do gerente ser exibida. Quando [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) é chamado, o manipulador deve verificar os arquivos dos quais ele é responsável, determinar quais deles são candidatos à limpeza e retornar a quantidade de espaço em disco que ele pode liberar.

Como a verificação pode ser um processo demorado, o Gerenciador de limpeza de disco usa o parâmetro *picb* do método para passar um ponteiro para uma interface [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) . O manipulador usa a interface periodicamente durante a verificação para chamar [**IEmptyVolumeCacheCallBack:: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress), que atende a duas finalidades.

-   Permite que o Gerenciador de limpeza de disco atualize uma barra de progresso, informando ao usuário como a verificação está progredindo.
-   Notifica o manipulador para interromper a verificação caso o botão **Cancelar** da janela de progresso seja clicado. Esse evento de botão não é comunicado diretamente ao manipulador; em vez disso, o Gerenciador de limpeza de disco retorna E \_ aborta na próxima vez em que [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) chama [**IEmptyVolumeCacheCallBack:: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="showproperties"></a>Mostrarproperties

Antes de iniciar a limpeza, o manipulador pode exibir uma interface do usuário normalmente na forma de uma janela do Windows Explorer que permite ao usuário ver uma lista de arquivos ou classes de arquivos selecionados para limpeza pelo manipulador. Se o manipulador define o sinalizador **EVCF \_ HASSETTINGS** quando [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) ou [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) é chamado, o usuário pode solicitar a interface do usuário clicando no botão exibido para essa finalidade no Gerenciador de limpeza de disco. O texto do botão varia de um manipulador para um manipulador, mas "exibir arquivos", "exibir páginas" e "opções" são rótulos comuns.

Quando o botão é clicado, o Gerenciador de limpeza de disco chama [**mostrarproperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) para solicitar que o manipulador exiba a interface do usuário. A interface do usuário deve ser criada como um filho da janela cujo identificador é passado no parâmetro *HWND* do método **showProperties** .

### <a name="purge"></a>Limpar

O Gerenciador de limpeza de disco chama o [**método de limpeza do**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) manipulador para definir a limpeza em movimento. O parâmetro *picb* do método é um ponteiro para a interface [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) do Gerenciador de limpeza de disco. Assim como com o método [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) , o manipulador deve usar a interface de retorno de chamada periodicamente para relatar seu progresso e consultar o Gerenciador de limpeza de disco se o usuário clicou em **Cancelar**. No entanto, observe que o método **Purge** deve chamar [**IEmptyVolumeCacheCallBack::P Urgeprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress), não [**ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="deactivate"></a>Desativar

O método [**Deactivate**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) é chamado quando o Gerenciador de limpeza de disco está se preparando para desligar. O manipulador deve executar todas as tarefas de limpeza necessárias e retornar. Se você não quiser que o manipulador seja executado novamente, defina o sinalizador **EVCF \_ REMOVEFROMLIST** no parâmetro *pdwFlags* do método de inicialização. Se esse sinalizador for definido, o Gerenciador de limpeza de disco removerá o manipulador de sua lista e excluirá as entradas do registro do manipulador. Você deve adicionar novamente as entradas do registro para executar o manipulador novamente. Esse sinalizador é normalmente usado para manipuladores que são executados apenas uma vez.

## <a name="registering-a-disk-cleanup-handler"></a>Registrando um manipulador de limpeza de disco

Para adicionar um manipulador à lista do Gerenciador de limpeza de disco, determinadas chaves e valores devem ser adicionados ao registro do Windows.

-   [Registrando o CLSID de um manipulador](#registering-a-handlers-clsid)
-   [Registrando um manipulador com o Gerenciador de limpeza de disco: geral](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registrando um manipulador com o Gerenciador de limpeza de disco: Windows 2000 ou sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Usando o objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
-   [Exemplo de registro de um manipulador de limpeza de disco](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registrando o CLSID de um manipulador

Assim como com todos os objetos COM, o GUID e a DLL do objeto Handler devem ser registrados sob a chave **CLSID** na **\_ \_ raiz de classes hKey**. Você também pode registrar um ícone que é exibido ao lado do nome do manipulador na caixa de listagem do Gerenciador de limpeza de disco, mas isso é opcional. O exemplo a seguir mostra as chaves, os valores e os dados envolvidos.

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

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registrando um manipulador com o Gerenciador de limpeza de disco: geral

Para concluir o registro, um manipulador deve adicionar uma chave que contém suas especificidades, conforme mostrado aqui. O restante desta seção aborda o conteúdo dessa chave.

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

Em geral, o nome da chave que contém as particularidades de um manipulador é nomeado para o tipo de arquivo que ele manipula, como **arquivos de programas baixados**, mas isso não é um requisito. A tabela a seguir detalha os possíveis valores encontrados nessa chave.

> [!Note]  
> Somente o valor padrão que especifica o identificador de classe do manipulador (CLSID) é necessário todos os outros valores são opcionais.

 



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
<td>O CLSID do manipulador, conforme registrado em <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Texto do botão opcional no qual os usuários podem clicar para exibir a interface do usuário do manipulador. O caractere de & pode ser colocado antes de um caractere para atribuir um atalho de teclado para o botão. O valor de AdvancedButtonText é ignorado por manipuladores expondo <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a>.</td>
</tr>
<tr class="odd">
<td>Limpeza</td>
<td>REG_SZ</td>
<td>Linha de comando especificando um arquivo executável e parâmetros de linha de comando opcionais. Essa linha de comando é executada na conclusão da limpeza de disco.</td>
</tr>
<tr class="even">
<td>CSIDl</td>
<td>REG_DWORD</td>
<td>Um identificador independente do sistema para uma pasta especial a ser incluída na pesquisa de arquivo. Esse valor deve ser inserido como um valor numérico para a instância, 0x0000001c em vez de CSIDL_LOCAL_APPDATA. Para obter uma lista de valores possíveis, consulte <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Apenas um único valor pode ser usado.<br/> Se o valor da pasta for especificado, o local indicado pelo valor CSIDl será anexado a essas informações para compor um caminho de pesquisa. Por exemplo, considere o cenário a seguir.<br/>
<ul>
<li>O valor CSIDl é especificado como 0x0000000d (CSIDL_MYMUSIC)</li>
<li>Sua pasta minhas músicas está localizada em C:\Documents and Settings \<em>nome_do_usuário</em>\Meus Music</li>
<li>O valor da pasta contém &quot; Jazz\Singers&quot;</li>
</ul>
O resultado desse cenário é que o manipulador de limpeza de disco pesquisa a pasta C:\Documents and Settings \<em>username</em>Music\Jazz\Singers. Observe que a barra que precede o valor da pasta será adicionada se não estiver presente.<br/></td>
</tr>
<tr class="odd">
<td>Descrição</td>
<td>REG_SZ</td>
<td>Texto descritivo exibido abaixo da caixa de listagem do Gerenciador de limpeza de disco quando o nome do manipulador é selecionado. Aqui você pode explicar o que o manipulador faz, em quais arquivos ele se preocupa e quaisquer outras informações elucidatory ao usuário. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a> não for exposto pelo manipulador, esse texto poderá ser substituído por meio do método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> do manipulador, especificando uma cadeia de caracteres alternativa no parâmetro <em>ppwszDescription</em> quando o método for chamado.</td>
</tr>
<tr class="even">
<td>Monitor</td>
<td>REG_SZ</td>
<td>O nome do manipulador a ser exibido na caixa de listagem do Gerenciador de limpeza de disco. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a> não for exposto pelo manipulador, esse texto poderá ser substituído por meio do método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> do manipulador, especificando uma cadeia de caracteres alternativa no parâmetro <em>ppwszDisplayName</em> quando o método for chamado.</td>
</tr>
<tr class="odd">
<td>FileList</td>
<td>REG_SZ ou REG_MULTI_SZ</td>
<td>Uma lista de arquivos pesquisados e limpos por esse manipulador. Você pode especificar curingas usando o? ou * caracteres. Se o valor for do tipo REG_SZ, várias extensões serão separadas usando o | ou: caracteres, sem espaços em ambos os lados.<br/> Se o sinalizador de DDEVCF_REMOVEDIRS for definido no valor de flags, esses valores poderão especificar nomes de diretório, bem como arquivos.<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>Sinalizadores que controlam os elementos do procedimento de pesquisa e limpeza. Um ou mais dos valores a seguir.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Pesquisar e remover recursivamente.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Depois que o manipulador for executado uma vez, remova-o do registro.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Remova os arquivos que atendem aos critérios de pesquisa, mesmo que eles sejam somente leitura.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Remova os arquivos que atendem aos critérios de pesquisa, mesmo que eles sejam arquivos do sistema.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Remova os arquivos que atendem aos critérios de pesquisa, mesmo que eles sejam arquivos ocultos.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Não exibirá esse manipulador no Gerenciador de limpeza de disco se nenhum arquivo corresponder aos seus critérios de pesquisa.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Corresponder o valor de Filelist em diretórios e remover correspondências e todos os seus subdiretórios.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Execute esse manipulador somente se o espaço em disco disponível estiver abaixo do valor crítico, determinado pelo Gerenciador de limpeza de disco definindo o sinalizador de EVCF_OUTOFDISKSPACE por meio de <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> ou <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a>.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Remova o diretório pai dos arquivos especificados quando o limpador tiver sido executado.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Use o valor LastAccess, se fornecido, em concerto quais arquivos devem ser limpos. Esse sinalizador é ignorado ao usar o <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> qualquer valor LastAccess fornecido é sempre usado.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pasta</td>
<td>REG_SZ, REG_MULTI_SZ ou REG_EXPAND_SZ</td>
<td>Uma pasta ou pastas específicas para procurar itens que correspondem a entradas no valor de FileList. Você pode especificar curingas usando o? ou * caracteres. Se o valor for do tipo REG_SZ, vários nomes de pastas serão separados usando o | caractere, sem espaços em ambos os lados.<br/> Se um valor CSIDl estiver presente, somente uma pasta poderá ser especificada nesse valor. O local indicado pelo valor CSIDl é anexado a esse caminho de pasta para compor um caminho de pesquisa. Para obter um exemplo, consulte a descrição do valor CSIDl.<br/> Se esse valor estiver ausente no Windows Vista Service Pack 1 (SP1) e posterior, o manipulador de limpeza será ignorado e ele retornará S_FALSE na inicialização.<br/> Se esse valor estiver ausente na versão original do Windows Vista e versões anteriores, a pasta raiz do volume atual será usada. O sinalizador de DDEVCF_DOSUBDIRS é necessário nesse caso para pesquisar a unidade inteira. Sem ele, somente a própria pasta raiz é pesquisada.<br/> Uma unidade ou unidades devem ser especificadas. Isso pode ser fornecido por meio do valor CSIDl ou por meio de uma cadeia de caracteres REG_EXPAND_SZ. No entanto, o bloqueio dessas opções, no entanto, a unidade a ser pesquisada deve ser especificada no nome da pasta. Usar?: para pesquisar a pasta na unidade atual.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ ou REG_EXPAND_SZ</td>
<td>O caminho para o recurso do qual obter um ícone para usar em associação com o manipulador.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>O número de dias que devem ter decorrido desde que um arquivo foi acessado pela última vez ou que um diretório foi criado para esse arquivo ou diretório ser considerado para limpeza.</td>
</tr>
<tr class="even">
<td>Prioridade</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>Determina a ordem em que o manipulador é executado em relação a outros manipuladores. Quanto maior o número, anteriormente no processo em que o manipulador é executado. Não há um intervalo definido, nenhum número é aceitável.</td>
</tr>
<tr class="odd">
<td>PropertyBag</td>
<td>REG_SZ</td>
<td>O CLSID de um recurso usado para fornecer texto localizado para o nome de exibição, a descrição e o texto do botão. Esse recurso é útil na situação em que um manipulador não implementa <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> e o manipulador está sendo executado no Microsoft Windows NT ou no Windows XP.<br/> O Gerenciador de limpeza de disco verifica primeiro se a rotina de inicialização do manipulador retornou essas cadeias de caracteres, como seria o caso quando <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> é implementado. Com falha, o gerente avançará para um conjunto de propriedades chamado nesse valor. Se nenhum tiver sido fornecido, ele recuperará o texto do registro.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>Ao executar o arquivo executável do Gerenciador de limpeza de disco Cleanmgr.exe de uma linha de comando, você pode declarar <em>perfis</em>de limpeza. Esses perfis são compostos de um subconjunto dos manipuladores disponíveis e recebem um rótulo numérico exclusivo. Isso permite que você automatize a execução de diferentes conjuntos de manipuladores em momentos diferentes.<br/> A linha de comando &quot;cleanmgr.exe/sageset:<strong>nnnn</strong> &quot; , em que <strong>nnnn</strong> é um rótulo numérico exclusivo, exibe uma interface do usuário que permite que você escolha os manipuladores a serem incluídos nesse perfil. Além de definir o perfil, o parâmetro sageset também grava um valor chamado StateFlags<strong>nnnn</strong>, em que <strong>nnnn</strong> é o rótulo usado no parâmetro, para todas as subchaves em <strong>VolumeCaches</strong>. Há dois valores de dados possíveis para essas entradas.
<ul>
<li>0: não execute este manipulador quando este perfil for executado.</li>
<li>2: incluir esse manipulador quando este perfil for executado.</li>
</ul>
<br/> Por exemplo, suponha que a linha de comando &quot;cleanmgr.exe/sageset: 1234 &quot; seja executada. Na interface do usuário que é apresentada, o usuário escolhe <strong>arquivos de programas baixados</strong>, mas não escolhe <strong>arquivos de Internet temporários</strong>. Os valores a seguir são gravados no registro.<br/>
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
<br/> A linha &quot; de comandocleanmgr.exe/sagerun:<strong>nnnn</strong> &quot; , em que o valor de <strong>nnnn</strong> corresponde ao rótulo declarado com o parâmetro do sageset, executa todos os manipuladores selecionados nesse perfil.<br/> Um valor StateFlags genérico é gravado no registro quando a limpeza de disco é executada normalmente. Esse valor simplesmente armazena o estado (marcado ou desmarcado) do manipulador na última vez em que foi apresentado como uma opção para o usuário. Há dois valores de dados possíveis para essas entradas.
<ul>
<li>0: o manipulador não foi selecionado.</li>
<li>1: o manipulador foi selecionado.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registrando um manipulador com o Gerenciador de limpeza de disco: Windows 2000 ou sistemas posteriores

Especificar o texto de exibição no registro pode dificultar a localização do software. Por esse motivo, o Windows 2000 e o Windows XP dão suporte à interface [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) com seu método de inicialização preferencial [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex). No Windows 2000 ou posterior, uma tentativa sempre é feita para chamar **IEmptyVolumeCache2:: InitializeEx** antes de [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize). O sistema usará **Initialize** somente para inicializar um manipulador se **IEmptyVolumeCache2** não for exposto.

Em relação ao registro, a única diferença no Windows 2000 ou posterior é que você pode omitir os valores de AdvancedButtonText, exibição e descrição quando [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) é exposto pelo manipulador. Esses valores, que contêm texto localizado corretamente, são fornecidos ao Gerenciador de limpeza de disco quando ele chama **InitializeEx**.

### <a name="using-the-datadrivencleaner-object"></a>Usando o objeto DataDrivenCleaner

Um manipulador de limpeza de disco básico, chamado de DataDrivenCleaner, é fornecido pelo sistema operacional. Para usar esse objeto como um manipulador em vez de implementar seu próprio, use o CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} como o valor padrão para a subchave do manipulador em **VolumeCaches** , conforme descrito em [registrando um manipulador com o Gerenciador de limpeza de disco: geral](#registering-a-handler-with-the-disk-cleanup-manager-general).

O DataDrivenCleaner não expõe [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2), portanto os valores de exibição e descrição são fornecidos pelo registro. Ao declarar essas cadeias de caracteres, lembre-se de que isso pode causar problemas de localização. O texto localizado pode ser fornecido por meio do valor PropertyBag. O valor de AdvancedButtonText é ignorado, pois não há interface do usuário e, portanto, nenhum botão para exibi-lo está disponível para esse manipulador.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Exemplo de registro de um manipulador de limpeza de disco

Veja a seguir um exemplo de registro de um manipulador de limpeza de disco implementado pela companhia telefônica. Esse manipulador implementa [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) e [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)e, portanto, fornece os valores de AdvancedButtonText, descrição e exibição, caso ele seja usado em um computador que executa o Windows 98. O manipulador combina os valores de CSIDl e de pasta para pesquisar arquivos nos arquivos de \\ programas C: \\ o diretório temporário da empresa telefônica \\ e o \_ sinalizador DDEVCF DOSUBDIRS é definido para que seus subdiretórios também sejam pesquisados. Somente os arquivos com as extensões. tmp e. TPC são considerados para limpeza e o \_ \_ sinalizador LASTACCESS privado DDEVCF é definido para que esses arquivos, somente aqueles que não tenham sido acessados por 14 dias ou mais, sejam considerados. O \_ sinalizador DDEVCF DONTSHOWIFZERO também é definido para que o manipulador não apareça na lista, a menos que tenha encontrado candidatos à limpeza.

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

 

