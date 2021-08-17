---
title: Estrutura do aplicativo de desktop de exemplo
description: Estrutura do aplicativo de desktop de exemplo
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Windows Gerenciador de Dispositivos de mídia, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Gerenciador de Dispositivos de mídia, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- exemplos, aplicativos de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dde8250a5efc8bc0f0b9582739bd8770d95ee586ea571a43bcbb9be69e8774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957156"
---
# <a name="structure-of-the-sample-desktop-application"></a>Estrutura do aplicativo de desktop de exemplo

O aplicativo de desktop de exemplo consiste em duas partes principais:

-   O projeto wmdapp contém a maioria das classes que exibem a interface do usuário, manipulam o recurso de arrastar e soltar e executam toda a funcionalidade necessária do programa.
-   O projeto proghelp é um aplicativo auxiliar que contém classes não essenciais para lidar com notificações de status e transferências de arquivos manuais da área de trabalho para o aplicativo.

O executável usa o projeto auxiliar somente quando o usuário seleciona **usar a interface de operação** no menu **Opções** para manipular a transferência manual de arquivos para o dispositivo e incrementar a barra de status no formulário progresso do download. Todo o restante do aplicativo é tratado no projeto wmdapp.



| Classe                | Arquivo                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | wmdmapp. cpp             | A classe que manipula a janela pai da interface do usuário. O código nesse arquivo também manipula algumas entradas de usuário que não são manipuladas pelo CDevFiles, como a criação de uma lista de reprodução ou álbum em um dispositivo, a exclusão de arquivos e o registro de opções de menu.                                                                                                                                                    |
| CDevices             | Devices. cpp             | A classe que manipula o painel esquerdo da janela principal do aplicativo, onde os dispositivos disponíveis são listados. Essa classe gerencia o loop de mensagens, que manipula a entrada do usuário, como selecionar um dispositivo e notificar o painel CDevFiles para carregar os arquivos apropriados quando a seleção do dispositivo for alterada.                                                                              |
| CDevFiles            | Devfiles. cpp            | A classe que manipula o painel à direita da janela principal do aplicativo, em que os arquivos no dispositivo selecionado são listados. Essa classe gerencia o loop de mensagens e manipula a entrada do usuário, como arrastar arquivos para o dispositivo e excluir arquivos do dispositivo.                                                                                                                          |
| CStatus              | Status. cpp              | A classe que manipula a barra de status inferior na janela principal, em que o número de dispositivos e arquivos é listado, junto com a quantidade de memória livre e usada no dispositivo selecionado.                                                                                                                                                                                                         |
| CWMDM                | Wmdevmgr. cpp            | a interface de nível superior para Windows Gerenciador de Dispositivos de mídia. Essa classe manipula a autenticação, recupera a interface **IWMDeviceManager** de nível superior e registra as notificações com a interface **IWMDMNotification** .                                                                                                                                                                  |
| CProgress            | Progress. cpp            | A classe no projeto de aplicativo principal que cria e gerencia a caixa de diálogo mostrando o progresso de um evento.                                                                                                                                                                                                                                                                             |
| CItemData            | Defaultdata. cpp            | Uma classe wrapper que mantém um ponteiro para um armazenamento (se representar um arquivo ou pasta no dispositivo) ou um dispositivo (se representar um dispositivo), bem como uma variedade de informações sobre o objeto, incluindo tamanho e atributos.                                                                                                                                                                  |
| CNotificationHandler | Notificationhandler. cpp | Manipula notificações de chegada e remoção de dispositivos alertando a janela CDevices.                                                                                                                                                                                                                                                                                                               |
| CProgressHelper      | ProgressHelper. cpp      | criado por CDevFiles em funções locais para receber notificações de Windows mídia Gerenciador de Dispositivos implementando **IWMDMProgress**. Ele é usado pela classe CProgress para determinar a quantidade de barras na barra de progresso e quando uma ação é concluída. Essa classe é definida como um objeto COM que expõe a interface do SDK **IWMDMProgress** e uma interface personalizada IWMDMProgressHelper. |
| COperationHelper     | Operationhelper. cpp     | Essa classe implementa o **IWMDMOperation** para lidar com a transferência manual de arquivos. Ele é multi-threaded para permitir que ele ocorra de forma assíncrona e é definido como um objeto COM que expõe uma interface personalizada, IWMDMOperationHelper, para instanciar e inicializar a classe. Essa classe só será usada se o usuário selecionar "usar a interface de operação" no menu de **Opções** .                            |



 

As listas a seguir descrevem as etapas básicas que ocorrem para várias ações do usuário:

**Na inicialização**

As etapas principais a seguir ocorrem quando o aplicativo de exemplo é iniciado.

1.  A variável global CWMDM é instanciada e autenticada e registra-se para receber notificações
2.  Um CDevices global é instanciado e CDevices:: Create é chamado para criar e preencher o painel de dispositivos.
3.  Um CDevFiles global é instanciado e CDevFiles:: Create é chamado para criar o painel de arquivos (que não é preenchido até que o usuário selecione um dispositivo).
4.  Um CStatus global é instanciado e CStatus:: Create é chamado para instanciar a barra de status.
5.  \_OnViewRefresh enumera todos os dispositivos e inicializa e adiciona todos os dispositivos (CItemData) a CDevices e atualiza a barra de status para mostrar o número de dispositivos.
6.  O CDevices:: AddItem adiciona o item ao TreeView que representa os dispositivos, com um ponteiro para ele mesmo como o TVITEM. lParam. Todos os objetos CDevice (dispositivos) e CDevFiles (arquivo) são armazenados nesse membro do nó TreeView na janela apropriada.

**Ao selecionar um dispositivo**

As seguintes etapas principais ocorrem quando o usuário seleciona um dispositivo no painel esquerdo da janela do aplicativo.

1.  A janela CDevices intercepta um clique e posta uma \_ mensagem UPDATEDEVICE do WM DRM \_ , para si mesma.
2.  O CDevices recebe sua própria mensagem e chama UpdateSelection, que diz ao objeto global CDevFiles para limpar tudo, enumerar todos os itens de nível superior no dispositivo e chama CDevFiles:: AddItem para adicionar cada um ao painel arquivos.
3.  Por fim, CDevices chama CDevFiles:: UpdateStatusBar para atualizar a barra de status com o dispositivo e as informações de arquivo corretas.

**Ao criar uma lista de reprodução**

Depois de clicar em "criar playlist" no menu **contêineres** , o aplicativo chama a função local \_ OnCreatePlaylist, que executa as seguintes ações:

1.  Obtém o número de itens selecionados da variável CDevFiles global.
2.  Chame a função local DlgNamePlaylist para abrir uma caixa de diálogo para obter um nome para a lista de reprodução.
3.  Chame o CProgress:: Create para criar uma janela de diálogo mostrando o progresso da ação e defina os parâmetros na classe CProgress, como o texto do título, o intervalo, o valor atual e assim por diante.
4.  Execute um loop em todos os itens selecionados no objeto de exibição de árvore CDevFiles e solicite o objeto CItemData associado a cada arquivo selecionado no modo de exibição de árvore, incrementando a barra de diálogo de progresso com cada arquivo. Os arquivos são adicionados a uma matriz de interfaces [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) .
5.  Obtenha um identificador para o item selecionado no momento e consulte-o para uma interface [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) , que será usada posteriormente para criar a nova lista de reprodução no dispositivo.
6.  Consulte o objeto selecionado para [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)e chame [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) para criar uma nova interface [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata).
7.  Adicione o \_ código de \_ formato ABSTRACTAUDIOVIDEOPLAYLIST WMDM FORMATCODE à nova interface **IWMDMMetadata** e crie uma lista de reprodução no dispositivo chamando [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3), passando a interface de metadados. O método recupera um ponteiro para o novo **IWMDMStorage** no dispositivo.
8.  Preencha a lista de reprodução consultando o novo armazenamento para [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)e chamando [**IWMDMStorage4:: setreferenciations**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences), passando a matriz de ponteiros **IWMDMStorage** coletados na etapa 4.
9.  Por fim, crie um novo objeto CItemData para manter a nova lista de reprodução no dispositivo, inicialize-o com o novo armazenamento e chame CDevFiles:: AddItem para adicioná-lo ao painel CDevFiles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Aplicativo de desktop de exemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




