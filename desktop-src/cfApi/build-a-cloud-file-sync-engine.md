---
description: Saiba como criar um mecanismo de sincronização de arquivos de nuvem que usa arquivos de espaço reservado usando a API de arquivos de nuvem.
title: Criar um Mecanismo de Sincronização de Nuvem que dá suporte a arquivos de espaço reservado
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: d7d1efae4a56e6f52473002953730fb9f1f9459f1ed8dc82e0ba75ddebf05dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551557"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Criar um Mecanismo de Sincronização de Nuvem que dá suporte a arquivos de espaço reservado

Um mecanismo de sincronização é um serviço que sincroniza arquivos, normalmente entre um host remoto e um cliente local. Os mecanismos de sincronização Windows geralmente apresentam esses arquivos ao usuário por meio do Windows de arquivos e Explorador de Arquivos. Antes do Windows 10, versão 1709, o suporte ao mecanismo de sincronização no Windows era limitado a superfícies ad hoc de cenário, como o painel de navegação do Explorador de Arquivos, a bandeja do sistema Windows e os drivers de filtro do sistema de arquivos (para mais aplicativos técnicos).

Windows 10 versão 1709 (também chamada de Fall Creators Update) introduziu a API de *arquivos de nuvem*. Essa API é uma nova plataforma que formaliza o suporte para mecanismos de sincronização. A API de arquivos de nuvem dá suporte a mecanismos de sincronização de uma maneira que oferece muitos novos benefícios para desenvolvedores e usuários finais.

A API de arquivos de nuvem contém as seguintes APIs nativas do Win32 e Windows Runtime (WinRT) :

* [API de Filtro de](cloud-filter-reference.md)Nuvem: essa API nativa do Win32 fornece funcionalidade no limite entre o modo de usuário e o sistema de arquivos. Essa API lida com a criação e o gerenciamento de arquivos e diretórios de espaço reservado.
* [Windows. Armazenamento. Namespace do provedor:](/uwp/api/windows.storage.provider)essa API do WinRT permite que os aplicativos configurem o provedor de armazenamento em nuvem e registrem a raiz de sincronização com o sistema operacional.

> [!NOTE]
> Atualmente, a API de arquivos de nuvem não dá suporte à implementação de mecanismos de sincronização de nuvem em aplicativos UWP. Os mecanismos de sincronização de nuvem devem ser implementados em aplicativos da área de trabalho.

## <a name="supported-features"></a>Recursos compatíveis

A API de arquivos de nuvem fornece os seguintes recursos para a criação de mecanismos de sincronização de nuvem.

### <a name="placeholder-files"></a>Arquivos de espaço reservado

* Os mecanismos de sincronização podem criar arquivos de espaço reservado que consomem apenas 1 KB de armazenamento para o header do sistema de arquivos e que se adote automaticamente em arquivos completos em condições de uso normais. Arquivos de espaço reservado presentes como arquivos típicos para aplicativos e usuários finais no shell Windows.
* Os arquivos de espaço reservado são integrados verticalmente do kernel Windows até o shell Windows e a compatibilidade do aplicativo com arquivos de espaço reservado geralmente não é um problema. Se você usar APIs do sistema de arquivos, o Prompt de Comando ou uma área de trabalho ou um aplicativo UWP para acessar um arquivo de espaço reservado, o arquivo será suado sem alterações de código adicionais e esse aplicativo poderá usar o arquivo normalmente.
* Os arquivos podem existir em três estados:
  * **Arquivo de espaço reservado:** uma representação vazia do arquivo e disponível somente se o serviço de sincronização estiver disponível.
  * **Arquivo completo:** o arquivo foi implícito e poderá ser desbaixado pelo sistema se for necessário espaço.
  * **Arquivo completo fixado:** o arquivo foi explicitamente Explorador de Arquivos pelo usuário e tem a garantia de estar disponível offline.

A imagem a seguir demonstra como os estados de arquivo completo, completo e fixado são mostrados em Explorador de Arquivos.

  ![Exemplo de três estados de arquivo Explorador de Arquivos](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Registro raiz de sincronização padronizado

* Registrar uma raiz de sincronização é simples e padronizado. Isso inclui a criação de um nó de marca no painel de navegação Explorador de Arquivos, conforme mostrado na captura de tela a seguir. As raízes podem ser criadas como entradas individuais de nível superior ou como filhos de um grupo pai.

  ![Exemplo de uma entrada raiz de sincronização Explorador de Arquivos](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Integração do Shell

* Ícones de estado:
  * A API de arquivos de nuvem fornece ícones de estado de hidratação automática padronizados mostrados Explorador de Arquivos e na área Windows área de trabalho.
  * Além dos ícones de estado Windows padrão usados para o estado de hidratação, você pode fornecer ícones de estado personalizados para propriedades adicionais específicas do serviço.
  * Substitui as extensões do Shell de sobreposição de ícone herdou.
* Indicação de progresso:
  * Abrir um arquivo de espaço reservado que leva mais de alguns segundos para se hidratar mostrará o progresso da hidratação. O progresso é mostrado em alguns locais, dependendo do contexto:
    * Em uma janela de diálogo do mecanismo de cópia.
    * O progresso em linha é mostrado ao lado do arquivo Explorador de Arquivos.
    * Se o arquivo não estiver aberto na instrução específica do usuário, uma notificação do sistema será mostrada para informar o usuário e fornecer uma maneira de controlar a atividade de hidratação não intencional.
* Miniaturas e metadados:
  * Os arquivos de espaço reservado podem ter miniaturas fornecidas pelo serviço e metadados de arquivo estendidos para fornecer ao usuário uma experiência de Explorador de Arquivos perfeita.
* Explorador de Arquivos painel de navegação:
  * O registro de uma raiz de sincronização com a API de arquivos de nuvem faz com que a raiz de sincronização (com um ícone e nome personalizado) apareça no painel de navegação Explorador de Arquivos do usuário.
* Explorador de Arquivos menus de contexto:
  * Registrar uma raiz de sincronização com a API de arquivos de nuvem fornece automaticamente vários verbos (entradas de menu) no menu de contexto do Explorador de Arquivos que permitem que o usuário controle o estado de hidratação de seu arquivo.
  * Verbos adicionais podem ser adicionados a esta seção do menu de contexto usando Ponte de Desktop APIs compatíveis.
* Controle do usuário da hidratação de arquivo:
  * Os usuários estão sempre no controle da hidratação de arquivos, mesmo quando os arquivos não são explicitamente explicitamente pelo usuário. Um sistema interativo é mostrado para a hidratação em segundo plano para alertar o usuário e fornecer opções. A imagem a seguir demonstra uma notificação do sistema para um arquivo de hidratação.
    ![Exemplo de um sistema interativo mostrado para a hidratação do arquivo em segundo plano](images/file-hydration-interactive-toast.png)
  * Se um usuário bloquear a desobstrução de arquivos por meio de um sistema interativo, ele poderá desbloquear o aplicativo na página **Downloads automáticos** de arquivo **no Configurações**.
    ![Captura de tela da configuração de downloads automáticos de arquivo](images/allow-automatic-file-downloads-setting.png)
* Conectar operações do mecanismo de cópia (com suporte no Windows 10 Insider Preview Build 19624 e versões posteriores):
  * Os provedores de armazenamento em nuvem podem registrar um gancho de cópia de shell para monitorar operações de arquivo em sua raiz de sincronização.
  * O provedor registra seu gancho de cópia definindo o valor do Registro **CopyHook** em sua chave do Registro raiz de sincronização como um CLSID do objeto de servidor local COM. Esse objeto de servidor local implementa a interface [IStorageProviderCopyHook.](../shell/nn-shobjidl-istorageprovidercopyhook.md)

### <a name="desktop-bridge"></a>Ponte de Desktop

* Os mecanismos de sincronização que usam as APIs de arquivos de nuvem são projetados para usar o [Ponte de Desktop](/windows/uwp/porting/desktop-to-uwp-root) como um requisito de implementação.

## <a name="cloud-mirror-sample"></a>Exemplo de Espelhamento de Nuvem

O [exemplo do Cloud Mirror](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) ilustra como criar uma solução que usa a API de arquivos de nuvem. Ele não se destina a ser usado como código de produção. Ele não tem um tratamento de erro robusto e é escrito para ser o mais facilmente compreendido possível. Ele é chamado de Espelho de Nuvem porque simplesmente espelha uma pasta local no disco local. Especifique uma pasta de servidor destinada a representar o servidor de arquivos de nuvem e uma pasta de cliente destinada a especificar o caminho raiz da sincronização. Um nó de nível superior aparece no painel de navegação no Explorador de Arquivos **chamado TestStorageProviderDisplayName** e esse nó é mapeado para a pasta do cliente especificada.

Quando se trata de sincronização, essas são as coisas que um provedor de sincronização de arquivos de nuvem totalmente desenvolvido deve implementar:

* Quando o arquivo raiz de sincronização é apenas um espaço reservado, o serviço é responsável por copiar o conteúdo do arquivo para a hidratação. Isso é implementado no exemplo.
* Quando o arquivo raiz de sincronização é um arquivo completo e o conteúdo do arquivo no serviço de nuvem muda, o serviço é responsável por notificar o cliente de sincronização local da alteração e o cliente de sincronização local deve lidar com mesclagem de acordo com suas próprias especificações. Isso não é implementado no exemplo.
* Quando o arquivo raiz de sincronização é um arquivo completo e o conteúdo do arquivo na alteração do caminho raiz de sincronização (o cliente local), o cliente de sincronização local deve notificar o serviço de nuvem e manipular mesclações de acordo com suas próprias especificações. A notificação de alteração de arquivo local é implementada no exemplo, mas não faz nada.

### <a name="use-the-sample"></a>Usar o exemplo

1. Crie duas pastas no disco rígido local. Um deles atuará como o servidor e o outro como o cliente.
2. Adicione alguns arquivos à pasta do servidor. Certifique-se de que a pasta do cliente está vazia.
3. Abra o exemplo de Espelhamento de Nuvem Visual Studio. De configurar **o projeto CloudMirrorPackage** como seu projeto de inicialização e, em seguida, criar e executar o exemplo. Quando solicitado pelo exemplo, insira os dois caminhos para as pastas do servidor e do cliente. Depois disso, você verá uma janela do console com informações de diagnóstico.
4. Abra Explorador de Arquivos e confirme se você vê o nó **TestStorageProviderDisplayName** e os espaço reservados para todos os arquivos copiados na pasta do servidor. Para simular um aplicativo que tenta abrir arquivos sem usar o seletor, copie várias imagens para a pasta do servidor. Clique duas vezes em um deles em sua pasta raiz de sincronização e confirme se ela sedosa. Em seguida, abra o aplicativo Fotos. O aplicativo pré-carregará arquivos adjacentes em segundo plano para torná-lo mais provável que o usuário não tenha atrasos ao procurar as outras imagens. Você pode observar que a reidratação em segundo plano ocorre por meio de toasts ou em Explorador de Arquivos.
5. Clique com o botão direito do mouse em um arquivo Explorador de Arquivos para abrir um menu de contexto e confirme se você vê o item de menu **TestCommand.** Clicar nesse item de menu exibirá uma caixa de mensagem.
6. Para interromper o exemplo, de definir o foco para a saída do console e pressione **Ctrl-C.** Isso limpará o registro raiz de sincronização para que o provedor seja desinstalado. Se o exemplo falhar, é possível que a raiz da sincronização permaneça registrada. Isso fará com que Explorador de Arquivos seja relançado sempre que você clicar em qualquer coisa e você será solicitado a obter os locais de cliente e servidor falsos. Se isso ocorrer, desinstale o aplicativo de exemplo **CloudMirrorPackage** do computador.

### <a name="sample-architecture"></a>Arquitetura de exemplo

O exemplo é deliberadamente simples. Ele usa classes estáticas para torná-la desnecessária para passar ponteiros de instância. Aqui estão as principais classes no exemplo:

* **FakeCloudProvider**: essa classe de nível superior controla as seguintes classes de trabalho:
  * **CloudProviderRegistrar**: registra as informações de raiz de sincronização com o Windows Shell.
  * **Espaços reservados**: gera os arquivos de espaço reservado no caminho raiz de sincronização.
  * **shellservices**: constrói os provedores de Shell de Windows para o menu de contexto, miniaturas e outros serviços.
  * **CloudProviderSyncRootWatcher**: cria uma instância de um DirectoryWatcher para monitorar as alterações no caminho raiz da sincronização e agir em alterações.
  * **FileCopierWithProgress**: copia os arquivos da pasta do servidor para a pasta do cliente lentamente em partes para simular o download deles de um servidor em nuvem real. Fornece a indicação de progresso para que as notificações e a interface do usuário do explorador de arquivos mostrem algo informativo.

Além das classes acima, o exemplo também fornece várias classes auxiliares para solicitar ao usuário pastas e alguns utilitários. **TestExplorerCommandHandler**, **CustomStateProvider**, **thumbnailprovider** e **UriSource** são exemplos de provedores de serviço do Shell.

## <a name="cloud-files-api-architecture"></a>Arquitetura de API de arquivos de nuvem

No núcleo da pilha de armazenamento na API de arquivos de nuvem está um driver de minifiltro do sistema de arquivos chamado cldflt.sys. Esse driver atua como um proxy entre os aplicativos do usuário e seu mecanismo de sincronização. Seu mecanismo de sincronização sabe como baixar e carregar os dados sob demanda, enquanto é responsabilidade de cldflt.sys trabalhar com o Shell para apresentar arquivos como se os dados de nuvem estivessem disponíveis localmente.

O Cldflt.sys atualmente dá suporte apenas a volumes NTFS, pois depende de alguns recursos exclusivos do NTFS.

Há muitos drivers do minifiltro do sistema de arquivos em um sistema e eles podem estar ativos em um determinado volume ao mesmo tempo. Os drivers que são mais interessantes para a API de arquivos de nuvem são os filtros do sistema de arquivos antivírus.

Os drivers do minifiltro do sistema de arquivos são gerenciados e têm suporte em um componente especial do modo kernel chamado Gerenciador de filtros. Entre muitas outras tarefas, o Gerenciador de filtros facilita a comunicação não filtrada entre filtros e componentes de modo de usuário por meio de uma construção conhecida como porta de mensagem de filtro.

## <a name="hydration-policies"></a>Políticas de hidratação

o Windows dá suporte a uma variedade de [políticas hidratação primárias](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) e modificadores de [política hidratação secundários](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) . As políticas de hidratação primárias têm esta ordem:

  **Sempre completo > completo > progressivo > parcial**

Os aplicativos e os mecanismos de sincronização podem definir sua política de hidratação primária preferencial. Se não for especificado, a política de hidratação padrão será progressiva para aplicativos e mecanismos de sincronização.

A política de hidratação de um arquivo de nuvem é determinada na hora de abertura do arquivo por esta fórmula:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Por exemplo, digamos que o usuário esteja tentando abrir um arquivo PDF armazenado na unidade de nuvem da Fabrikam usando o Visualizador de PDF da Contoso, que não especifica uma política de hidratação preferida. A política de hidratação de aplicativo é, portanto, hidratação progressiva, neste caso, por padrão. No entanto, como a unidade de nuvem da Fabrikam é um mecanismo de sincronização hidratação completo, a política de hidratação final no arquivo torna-se hidratação completa, o que fará com que o arquivo seja totalmente alimentado no primeiro acesso. O mesmo resultado ocorre nos casos em que o mecanismo de sincronização dá suporte a hidratação progressivos, mas a preferência do aplicativo é hidratação completa.

Observe que a política de hidratação de arquivo não pode ser alterada depois que o arquivo é aberto.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Compatibilidade com aplicativos que usam pontos de nova análise

A API de arquivos de nuvem implementa o sistema de espaço reservado usando [pontos de nova análise](/windows/desktop/FileIO/reparse-points). Um equívoco comum sobre pontos de nova análise é que eles são os mesmos links simbólicos. Esse equívoco é ocasionalmente refletido em implementações de aplicativo e, como resultado, muitos aplicativos existentes têm erros de ocorrência ao encontrar qualquer ponto de nova análise.

Para atenuar esse problema de compatibilidade, a API de arquivos de nuvem sempre oculta seus pontos de nova análise de todos os aplicativos, exceto para mecanismos de sincronização e processos cuja imagem principal reside em **% systemroot%**. Os aplicativos que entendem os pontos de nova análise corretamente podem forçar a plataforma a expor os pontos de nova análise da API de arquivos de nuvem usando [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) ou [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode).