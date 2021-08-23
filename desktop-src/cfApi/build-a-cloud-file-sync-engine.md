---
description: Saiba como criar um mecanismo de sincronização de arquivos de nuvem que usa arquivos de espaço reservado usando a API de arquivos de nuvem.
title: Criar um mecanismo de sincronização de nuvem que dê suporte a arquivos de espaço reservado
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: d7d1efae4a56e6f52473002953730fb9f1f9459f1ed8dc82e0ba75ddebf05dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551557"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Criar um mecanismo de sincronização de nuvem que dê suporte a arquivos de espaço reservado

Um mecanismo de sincronização é um serviço que sincroniza arquivos, normalmente entre um host remoto e um cliente local. os mecanismos de sincronização no Windows geralmente apresentam esses arquivos ao usuário por meio do sistema de arquivos Windows e do explorador de arquivos. antes de Windows 10, a versão 1709, o suporte ao mecanismo de sincronização no Windows era limitado a superfícies ad hoc independentes de cenário, como o painel de navegação do explorador de arquivos, a bandeja do sistema do Windows e (para aplicativos mais técnicos) drivers de filtro do sistema de arquivos.

Windows 10 versão 1709 (também chamada de atualização de criadores de outono) introduziu a *API de arquivos de nuvem*. Essa API é uma nova plataforma que formalizes o suporte a mecanismos de sincronização. A API de arquivos de nuvem fornece suporte para mecanismos de sincronização de uma maneira que oferece muitos benefícios novos para desenvolvedores e usuários finais.

a API de arquivos de nuvem contém as seguintes apis nativas do Win32 e as apis do Windows Runtime (WinRT):

* [API de filtro de nuvem](cloud-filter-reference.md): essa API Win32 nativa fornece a funcionalidade no limite entre o modo de usuário e o sistema de arquivos. Essa API manipula a criação e o gerenciamento de diretórios e arquivos de espaço reservado.
* [Windows. Armazenamento. Namespace do provedor](/uwp/api/windows.storage.provider): essa API do WinRT permite que os aplicativos configurem o provedor de armazenamento em nuvem e registrem a raiz de sincronização com o sistema operacional.

> [!NOTE]
> Atualmente, a API de arquivos de nuvem não dá suporte à implementação de mecanismos de sincronização de nuvem em aplicativos UWP. Os mecanismos de sincronização de nuvem devem ser implementados em aplicativos da área de trabalho.

## <a name="supported-features"></a>Recursos compatíveis

A API de arquivos de nuvem fornece os seguintes recursos para a criação de mecanismos de sincronização de nuvem.

### <a name="placeholder-files"></a>Arquivos de espaço reservado

* Os mecanismos de sincronização podem criar arquivos de espaço reservado que consomem apenas 1 KB de armazenamento para o cabeçalho do sistema de arquivos e que hidratar automaticamente em arquivos completos em condições de uso normal. os arquivos de espaço reservado apresentam arquivos típicos para aplicativos e usuários finais no Shell de Windows.
* os arquivos de espaço reservado são integrados verticalmente do kernel de Windows até o Shell de Windows, e a compatibilidade de aplicativos com arquivos de espaço reservado geralmente é um problema não. Se você usar APIs do sistema de arquivos, o prompt de comando ou um aplicativo da área de trabalho ou UWP para acessar um arquivo de espaço reservado, o arquivo será hidratar sem alterações de código adicionais e esse aplicativo poderá usar o arquivo normalmente.
* Os arquivos podem existir em três Estados:
  * **Arquivo de espaço reservado**: uma representação vazia do arquivo e estará disponível somente se o serviço de sincronização estiver disponível.
  * **Arquivo completo**: o arquivo foi alimentado implicitamente e poderia ser dealimentado pelo sistema se for necessário espaço.
  * **Arquivo completo fixado**: o arquivo foi alimentado explicitamente pelo usuário por meio do explorador de arquivos e tem a garantia de estar disponível offline.

A imagem a seguir demonstra como os Estados de arquivo completo de espaço reservado, completo e fixado são mostrados no explorador de arquivos.

  ![Exemplo de três Estados de arquivo no explorador de arquivos](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Registro de raiz de sincronização padronizado

* O registro de uma raiz de sincronização é simples e padronizado. Isso inclui a criação de um nó com marca no painel de navegação do explorador de arquivos, conforme mostrado na captura de tela a seguir. As raízes podem ser criadas como entradas individuais de nível superior ou como filhos de um agrupamento pai.

  ![Exemplo de uma entrada de raiz de sincronização no explorador de arquivos](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Integração com o Shell

* Ícones de Estado:
  * a API de arquivos de nuvem fornece ícones de estado de hidratação padrão e automáticos mostrados no explorador de arquivos e na área de trabalho Windows.
  * além dos ícones de estado de Windows padrão usados para o estado hidratação, você pode fornecer ícones de estado personalizado para propriedades adicionais específicas do serviço.
  * Substitui as extensões do Shell de sobreposição de ícone herdado.
* Indicação de progresso:
  * Abrir um arquivo de espaço reservado que leva mais de alguns segundos para hidratar mostrará o hidratação Progress. O andamento é mostrado em alguns locais, dependendo do contexto:
    * Em uma janela de diálogo do mecanismo de cópia.
    * O andamento em linha é mostrado ao lado do arquivo no explorador de arquivos.
    * Se o arquivo não estiver aberto na instrução específica do usuário, uma notificação do sistema será mostrada para informar o usuário e fornecer uma maneira de controlar a atividade de hidratação indesejada.
* Miniaturas e metadados:
  * Os arquivos de espaço reservado podem ter miniaturas avançadas fornecidas pelo serviço e metadados de arquivo estendidos para fornecer ao usuário uma experiência de Gerenciador de arquivos sem interrupções.
* Painel de navegação do explorador de arquivos:
  * O registro de uma raiz de sincronização com a API de arquivos de nuvem faz com que a raiz de sincronização (com um ícone e um nome personalizado) apareça no painel de navegação do explorador de arquivos.
* Menus de contexto do explorador de arquivos:
  * O registro de uma raiz de sincronização com a API de arquivos de nuvem fornece automaticamente vários verbos (entradas de menu) no menu de contexto do explorador de arquivos que permite ao usuário controlar o estado hidratação de seu arquivo.
  * verbos adicionais podem ser adicionados a esta seção do menu de contexto usando APIs compatíveis com Ponte de Desktop.
* Controle de usuário do arquivo hidratação:
  * Os usuários estão sempre no controle do arquivo hidratação, mesmo quando os arquivos não são alimentados explicitamente pelo usuário. Um sistema de notificação interativo é mostrado para hidratação em segundo plano para alertar o usuário e fornecer opções. A imagem a seguir demonstra uma notificação do sistema para um arquivo HYDRATING.
    ![Exemplo de um sistema de notificação interativo mostrado para o arquivo de segundo plano hidratação](images/file-hydration-interactive-toast.png)
  * se um usuário bloquear um aplicativo de arquivos hydrating por meio de um sistema de notificação interativo, ele poderá desbloquear o aplicativo na página de **downloads de arquivo automático** no **Configurações**.
    ![Captura de tela da configuração de downloads de arquivo automático](images/allow-automatic-file-downloads-setting.png)
* operações de mecanismo de cópia de conexão (com suporte no Windows 10 insider Preview versão 19624 e versões posteriores):
  * Os provedores de armazenamento em nuvem podem registrar um gancho de cópia do Shell para monitorar operações de arquivo em sua raiz de sincronização.
  * O provedor registra seu gancho de cópia definindo o valor do registro **CopyHook** sob sua chave de registro raiz de sincronização para um CLSID de seu objeto de servidor local com. Esse objeto de servidor local implementa a interface [IStorageProviderCopyHook](../shell/nn-shobjidl-istorageprovidercopyhook.md) .

### <a name="desktop-bridge"></a>Ponte de Desktop

* os mecanismos de sincronização usando as APIs de arquivos de nuvem são projetados para usar o [Ponte de Desktop](/windows/uwp/porting/desktop-to-uwp-root) como um requisito de implementação.

## <a name="cloud-mirror-sample"></a>Exemplo de espelho de nuvem

O [exemplo de espelho de nuvem](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) ilustra como criar uma solução que usa a API de arquivos de nuvem. Ele não se destina a ser usado como código de produção. Ele não tem um tratamento de erros robusto e é escrito para ser o mais facilmente compreendido possível. Ele é chamado de espelho de nuvem porque simplesmente espelha uma pasta local em seu disco local. Você especifica uma pasta de servidor que deve representar o servidor de arquivos de nuvem e uma pasta de cliente que é destinada a especificar o caminho raiz de sincronização. Um nó de nível superior aparece no painel de navegação no explorador de arquivos chamado **TestStorageProviderDisplayName**, e esse nó é mapeado para a pasta de cliente especificada.

Quando se trata de sincronização, essas são as coisas que um provedor de sincronização de arquivos de nuvem totalmente desenvolvido deve implementar:

* Quando o arquivo raiz de sincronização é apenas um espaço reservado, o serviço é responsável por copiar o conteúdo do arquivo para hidratação. Isso é implementado no exemplo.
* Quando o arquivo raiz de sincronização é um arquivo completo e o conteúdo do arquivo no serviço de nuvem é alterado, o serviço é responsável por notificar o cliente de sincronização local da alteração e o cliente de sincronização local deve lidar com as mesclagens de acordo com suas próprias especificações. Isso não é implementado no exemplo.
* Quando o arquivo raiz de sincronização é um arquivo completo e o conteúdo do arquivo no caminho raiz de sincronização (o cliente local) é alterado, o cliente de sincronização local deve notificar o serviço de nuvem e lidar com as mesclagens de acordo com suas próprias especificações. A notificação de alteração de arquivo local é implementada no exemplo, mas não faz nada.

### <a name="use-the-sample"></a>Usar o exemplo

1. Crie duas pastas na unidade de disco rígido local. Um deles funcionará como o servidor e o outro como o cliente.
2. Adicione alguns arquivos à pasta do servidor. Verifique se a pasta do cliente está vazia.
3. Abra o exemplo de espelho de nuvem em Visual Studio. Defina o projeto **CloudMirrorPackage** como seu projeto de inicialização e, em seguida, compile e execute o exemplo. Quando solicitado pelo exemplo, insira os dois caminhos para as pastas servidor e cliente. Depois disso, você verá uma janela do console com informações de diagnóstico.
4. Abra o explorador de arquivos e confirme se você vê o nó **TestStorageProviderDisplayName** e os espaços reservados para todos os arquivos que você copiou para a pasta do servidor. Para simular um aplicativo que tenta abrir arquivos sem usar o seletor, copie várias imagens para a pasta do servidor. Clique duas vezes em um deles na pasta raiz de sincronização e confirme se ele hidratam. Em seguida, abra o aplicativo fotos. O aplicativo carregará previamente os arquivos adjacentes em segundo plano para torná-lo mais provável que o usuário não experimente atrasos ao examinar as outras imagens. Você pode observar que o DEHYDRATION de fundo acontece por meio de torradeiras ou no explorador de arquivos.
5. Clique com o botão direito do mouse em um arquivo no explorador de arquivos para abrir um menu de contexto e confirme que você vê o item de menu **TestCommand** . Clicar nesse item de menu exibirá uma caixa de mensagem.
6. Para parar o exemplo, defina foco para a saída do console e pressione **Ctrl-C**. Isso limpará o registro de raiz de sincronização para que o provedor seja desinstalado. Se o exemplo falhar, será possível que a raiz de sincronização permaneça registrada. Isso fará com que o explorador de arquivos seja reiniciado sempre que você clicar em qualquer coisa, e você receberá uma solicitação para os locais falsos do cliente e do servidor. Se isso ocorrer, desinstale o aplicativo de exemplo **CloudMirrorPackage** do seu computador.

### <a name="sample-architecture"></a>Arquitetura de exemplo

O exemplo é deliberadamente simples. Ele usa classes estáticas para tornar desnecessário passar ponteiros de instância. Aqui estão as classes principais no exemplo:

* **FakeCloudProvider:** essa classe de nível superior controla as seguintes classes de trabalho:
  * **CloudProviderRegistrar:** registra as informações raiz de sincronização com o Windows Shell.
  * **Espaço reservado:** gera os arquivos de espaço reservado no caminho raiz de sincronização.
  * **ShellServices:** constrói os provedores Windows Shell para o menu de contexto, miniaturas e outros serviços.
  * **CloudProviderSyncRootWatcher:** instalita um DirectoryWatcher para monitorar as alterações no caminho raiz de sincronização e agir com base nas alterações.
  * **FileCopierWithProgress:** copia arquivos da pasta do servidor para a pasta do cliente lentamente em partes para simular o download deles de um servidor de nuvem real. Fornece indicação de progresso para que os sistemas e Explorador de Arquivos interface do usuário mostrem ao usuário algo informativo.

Além das classes acima, o exemplo também fornece várias classes auxiliares para solicitar ao usuário pastas e alguns utilitários. O **TestExplorerCommandHandler,** **CustomStateProvider,** **ThumbnailProvider** e **UriSource** são todos exemplos de provedores de serviços do Shell.

## <a name="cloud-files-api-architecture"></a>Arquitetura da API de arquivos de nuvem

No núcleo da pilha de armazenamento na API de arquivos de nuvem, há um driver de minifiltro do sistema de arquivos chamado cldflt.sys. Esse driver atua como um proxy entre os aplicativos do usuário e o mecanismo de sincronização. Seu mecanismo de sincronização sabe como baixar e carregar os dados sob demanda enquanto é responsabilidade do cldflt.sys trabalhar com o Shell para apresentar arquivos como se os dados de nuvem fossem disponibilizados localmente.

Cldflt.sys atualmente só dá suporte a volumes NTFS porque depende de alguns recursos exclusivos do NTFS.

Há muitos drivers de minifiltro do sistema de arquivos em um sistema e eles podem estar ativos em um determinado volume ao mesmo tempo. Os drivers mais interessantes para a API de arquivos de nuvem são os filtros do sistema de arquivos antivírus.

Os drivers de minifiltro do sistema de arquivos são gerenciados e têm suporte por um componente especial no modo kernel chamado gerenciador de filtros. Entre muitas outras tarefas, o gerenciador de filtros facilita a comunicação não filtrada entre filtros e componentes de modo de usuário por meio de um constructo conhecido como porta de mensagem de filtro.

## <a name="hydration-policies"></a>Políticas de hidratação

Windows dá suporte a uma variedade de políticas [primárias](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) de hidratação e [modificadores de](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) política de hidratação secundária. As políticas primárias de hidratação têm esta ordem:

  **Sempre completo > de > de > Parcial**

Os aplicativos e os mecanismos de sincronização podem definir sua política de hidratação primária preferencial. Se não for especificada, a política de hidratação padrão será progressiva para aplicativos e mecanismos de sincronização.

A política de hidratação de um arquivo de nuvem é determinada no tempo de abertura do arquivo por esta fórmula:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Por exemplo, digamos que o usuário está tentando abrir um arquivo PDF armazenado no Fabrikam Cloud Drive usando o Visualizador de PDF da Contoso, que não especifica uma política de hidratação preferencial. A política de hidratação do aplicativo é, portanto, a hidratação progressiva, nesse caso, por padrão. No entanto, como a Unidade de Nuvem da Fabrikam é um mecanismo de sincronização de hidratação completa, a política final de hidratação no arquivo se torna completa, o que fará com que o arquivo seja totalmente alimentado no primeiro acesso. O mesmo resultado ocorre em casos em que o mecanismo de sincronização dá suporte à hidratação progressiva, mas a preferência do aplicativo é a hidratação completa.

Observe que a política de hidratação de arquivo não pode ser alterada depois que o arquivo é aberto.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Compatibilidade com aplicativos que usam pontos de análise

A API de arquivos de nuvem implementa o sistema de espaço reservado usando [pontos de nova pesquisa.](/windows/desktop/FileIO/reparse-points) Um erro comum sobre pontos de nova repareia é que eles são iguais aos links simbólicos. Esse erro é ocasionalmente refletido em implementações de aplicativo e, como resultado, muitos aplicativos existentes atingem erros ao encontrar qualquer ponto de nova pesquisa.

Para atenuar esse problema de compatibilidade, a API de arquivos de nuvem sempre oculta seus pontos de nova análise de todos os aplicativos, exceto para mecanismos de sincronização e processos cuja imagem principal reside em **%systemroot%.** Aplicativos que entendem os pontos de nova análise corretamente podem forçar a plataforma a expor pontos de nova análise de API de arquivos de nuvem usando [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) ou [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode).