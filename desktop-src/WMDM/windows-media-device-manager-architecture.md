---
title: Windows Arquitetura de Gerenciador de Dispositivos de mídia
description: Windows Arquitetura de Gerenciador de Dispositivos de mídia
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Gerenciador de Dispositivos de mídia, arquitetura
- Gerenciador de Dispositivos, arquitetura
- arquitetura para Windows de mídia Gerenciador de Dispositivos
- Windows Gerenciador de Dispositivos de mídia, aplicativos de área de trabalho
- Gerenciador de Dispositivos, aplicativos de área de trabalho
- Windows Gerenciador de Dispositivos de mídia, provedores de serviço
- Gerenciador de Dispositivos, provedores de serviços
- Windows Gerenciador de Dispositivos de mídia, plug-ins
- Gerenciador de Dispositivos, plug-ins
- aplicativos de desktop, Windows arquitetura de Gerenciador de Dispositivos de mídia
- provedores de serviço, Windows a arquitetura de Gerenciador de Dispositivos de mídia
- plug-ins, Windows a arquitetura de Gerenciador de Dispositivos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deadb7e5a85c4d7331a276a515add2ace30e566c2b683404b7b4466bf891dbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055584"
---
# <a name="windows-media-device-manager-architecture"></a>Windows Arquitetura de Gerenciador de Dispositivos de mídia

Windows A mídia Gerenciador de Dispositivos permite que um aplicativo ou um plug-in se comunique com um dispositivo. Os aplicativos podem solicitar metadados de dispositivo, enumerar e explorar dispositivos anexados e enviar ou receber objetos (pastas, arquivos, listas de reprodução e assim por diante). Windows a mídia Gerenciador de Dispositivos fornece uma única API para o aplicativo de chamada, não importa o tipo de dispositivo que está sendo chamado (MTP ou Armazenamento de classe em massa, provedores de serviços criados na versão 10 ou provedores de serviços criados em versões anteriores do Windows Gerenciador de Dispositivos de mídia).

Windows A mídia Gerenciador de Dispositivos atua como uma passagem entre os três principais componentes do sistema: o aplicativo, que faz solicitações (para obter informações, ler ou gravar dados etc.); um provedor de conteúdo seguro, que é um componente que lida com a comunicação com arquivos protegidos por DRM; e um provedor de serviços, que recebe solicitações do aplicativo e se comunica com o dispositivo para executar essas solicitações. o aplicativo e o provedor de serviços são criados no SDK do Windows Media Gerenciador de Dispositivos.

o diagrama a seguir mostra como um aplicativo de área de trabalho se comunica com um dispositivo usando Windows mídia Gerenciador de Dispositivos 11.

![diagrama mostrando um aplicativo que se comunica com quatro tipos diferentes de dispositivos.](images/wmdm-device-communication.gif)

O diagrama anterior mostra um aplicativo que se comunica com quatro tipos diferentes de dispositivos, cada um com seu próprio provedor de serviços. Cada provedor de serviços é projetado para se comunicar com um tipo específico de dispositivo; este diagrama mostra os três provedores de serviços fornecidos pela Microsoft (drivers de classe genérica para dispositivos de classe de Armazenamento em massa, dispositivos RAPI e dispositivos MTP), bem como um provedor de serviços personalizado para um dispositivo proprietário criado por terceiros. quando um dispositivo se conecta, Windows mídia Gerenciador de Dispositivos cria uma instância do provedor de serviços registrado para esse dispositivo. os provedores de serviço obtêm solicitações do aplicativo por meio de Windows mídia Gerenciador de Dispositivos interfaces que eles implementam, usam os drivers apropriados para se comunicar com o dispositivo e retornam os resultados apropriados. a comunicação entre o provedor de serviços e o dispositivo está fora do domínio do Windows Gerenciador de Dispositivos de mídia.

Provedores de serviço são invisíveis para o aplicativo; um aplicativo vê apenas uma lista de "dispositivos" porque Windows mídia Gerenciador de Dispositivos expõe um conjunto padrão de métodos e interfaces para todos os dispositivos. se um fabricante criar um provedor de serviços personalizado, ele deverá lidar com todos os métodos de Gerenciador de Dispositivos de mídia padrão Windows se os aplicativos forem capazes de usar o dispositivo.

Esse diagrama também mostra um módulo SCP (provedor de conteúdo seguro). Este módulo é responsável por manipular conteúdo protegido por DRM (gerenciamento de direitos digitais). A Microsoft fornece um módulo SCP que pode lidar com arquivos WMA e WMV protegidos por DRM. Se um aplicativo ou dispositivo pretender lidar com outros formatos protegidos, ele deve fornecer seu próprio módulo SCP. Nem o aplicativo nem o provedor de serviços lidam diretamente com o SCP.

o aplicativo e o provedor de serviços são criados em Windows Gerenciador de Dispositivos de mídia, que roteia chamadas entre o aplicativo e o provedor de serviços apropriado para um dispositivo; o provedor de serviços é responsável pela comunicação direta com o dispositivo. Windows A mídia Gerenciador de Dispositivos executa algumas ações em si (como a enumeração de dispositivos conectados, chamadas de roteamento e manipulação da verificação de componentes); no entanto, a maior parte do trabalho é feita pelo provedor de serviços, que recebe solicitações do aplicativo e se comunica com o dispositivo.

um aplicativo criado em Windows mídia Gerenciador de Dispositivos pode se comunicar com dispositivos e provedores de serviços criados em versões anteriores do Gerenciador de Dispositivos de mídia do Windows; no entanto, esses dispositivos mais antigos serão executados por meio de componentes da série 9 (não mostrados) e não oferecerão suporte aos recursos mais recentes, especialmente a tecnologia de gerenciamento de direitos digitais mais avançada.

Arquitetura de um dispositivo

o diagrama a seguir mostra uma hierarquia simplificada de dispositivos e armazenamentos, como visto por um aplicativo usando Windows Gerenciador de Dispositivos de mídia.

![diagrama mostrando armazenamentos em um dispositivo.](images/wmdm-basic-device-layout.gif)

o diagrama anterior mostra uma versão simplificada de uma unidade flash conectada, como visto por um aplicativo de Gerenciador de Dispositivos de mídia Windows. A unidade flash tem atributos e propriedades, como um número de série e configurações de formato com suporte. Um filho imediato do dispositivo flash é o objeto de armazenamento raiz, que contém uma pasta, que contém uma imagem e uma música.

Um aplicativo enumera a lista de dispositivos anexados chamando um método de enumeração exposto pela interface [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) raiz. Os dispositivos são representados por uma interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (ou uma derivada). Essa interface expõe métodos para recuperar o nome do dispositivo, os recursos de formato, o número de série e assim por diante, bem como um método que enumera os *armazenamentos* no dispositivo. no Gerenciador de Dispositivos de mídia Windows, um armazenamento é qualquer tipo de objeto no dispositivo, seja ou não um blob real de dados. Por exemplo: Arquivos de áudio, arquivos de texto, pastas, listas de reprodução armazenadas como arquivos e listas de reprodução armazenadas como metadados são consideradas armazenamentos, mesmo que pastas e itens de metadados provavelmente não representem um arquivo físico. O tipo (ou formato) de um armazenamento pode ser recuperado chamando [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (ou [**GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata), solicitando o formato do armazenamento).

Os armazenamentos em um dispositivo são armazenados hierarquicamente e todos os dispositivos têm um armazenamento raiz. Cada armazenamento pode conter zero ou mais objetos filho, enumerados chamando o método [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) do armazenamento.

Observe que cada armazenamento no diagrama tem atributos e metadados associados a ele (nem todos os valores são mostrados). Os atributos são simples, as informações booleanas geralmente descrevem informações de gerenciamento ou de navegação (como "tem pastas" ou "pode excluir"), enquanto os metadados podem ser valores de cadeia de caracteres, números ou informações complexas (como recursos de renderização). Os atributos são descritos por um conjunto bastante limitado de sinalizadores definidos pelo SDK e recuperados chamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) ou [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Os valores de metadados são recuperados por um nome exclusivo; o SDK define vários valores de metadados aos quais os dispositivos devem dar suporte, mas os dispositivos podem definir suas próprias [constantes de metadados](metadata-constants.md). No entanto, se um dispositivo ou provedor de serviços definir uma nova constante de metadados, os aplicativos não poderão solicitar ou definir esse valor, a menos que os desenvolvedores de aplicativos estejam cientes dessa nova constante. Um provedor de serviços deve dar suporte a [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) ou posterior para dar suporte à recuperação ou à configuração de metadados. Para obter mais informações, consulte [obtendo e configurando metadados e atributos](getting-and-setting-metadata-and-attributes.md).

Provedores de serviço

O provedor de serviços atua como um meio entre o aplicativo e o dispositivo. O provedor de serviços é invisível para o desenvolvedor de aplicativos, portanto, um desenvolvedor de aplicativos não precisa saber nada sobre o desenvolvimento de um provedor de serviços. No entanto, é o provedor de serviços que faz o trabalho de comunicação com um dispositivo.

um provedor de serviços é uma DLL COM criada em Windows mídia Gerenciador de Dispositivos que recebe solicitações de um aplicativo e se comunica com o dispositivo para realizá-las. a comunicação com o aplicativo da área de trabalho é mediada por Windows mídia Gerenciador de Dispositivos; a comunicação com o dispositivo está sob o controle do provedor de serviços.

Um provedor de serviços recebe solicitações do aplicativo para enumerar o conteúdo do dispositivo, solicitações de recursos do dispositivo, solicitações para ler ou gravar dados e assim por diante. Ele deve saber o design de um dispositivo bem suficiente para que ele possa enviar comandos no formato e protocolo adequados. Ele também deve ser capaz de ocultar requisitos específicos do dispositivo, como uma extensão de arquivo necessária para listas de reprodução, para que os aplicativos não precisem saber esses requisitos para usar o dispositivo.

a Microsoft fornece vários provedores de serviços para tipos de dispositivos padrão, incluindo dispositivos MTP genéricos, dispositivos de classe de Armazenamento em massa e dispositivos RAPI. O único motivo pelo qual um designer de dispositivo deve precisar criar um provedor de serviços personalizado é se um dispositivo tem alguns requisitos de armazenamento de dados específicos ou incomuns que os provedores de serviço Standard não manipulam, por exemplo, se os arquivos devem ser armazenados em locais específicos e o sistema operacional do dispositivo não tratar isso automaticamente.

quando um dispositivo está conectado ao computador, o sistema operacional cria uma instância do provedor de serviços apropriado para cada aplicativo de Windows de mídia Gerenciador de Dispositivos. se um segundo Windows aplicativo de Gerenciador de Dispositivos de mídia for iniciado, uma segunda instância do provedor de serviços será carregada. No entanto, cada provedor de serviços pode lidar com vários dispositivos. O diagrama a seguir ilustra isso.

![diagrama mostrando dois dispositivos MTP se comunicando com dois aplicativos.](images/wmdm-sp-to-device.gif)

O diagrama anterior mostra dois aplicativos diferentes se comunicando com dois dispositivos MTP. Os dispositivos usam a mesma classe de provedor de serviços, mas cada aplicativo tem sua própria instância do mesmo provedor de serviços. Cada instância do provedor de serviços está se comunicando com dispositivos. As diferentes instâncias do provedor de serviços não estão cientes umas das outras.

Muitos métodos de aplicativo têm um método de provedor de serviços nomeado de forma correspondente. quando o aplicativo chama um método, Windows mídia Gerenciador de Dispositivos roteia a chamada para o método correspondente no provedor de serviços (embora possa executar algumas ações internas adicionais primeiro). por exemplo, quando o aplicativo chama [**IWMDMDevice3:: getproperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty), Windows mídia Gerenciador de Dispositivos roteia essa chamada para a implementação do provedor de serviços de [**IMDSPDevice3:: getproperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty). (A maioria das interfaces de aplicativo começa com IWMDM e a interface do provedor de serviço correspondente começa com IMDSP). Espera-se que o provedor de serviços manipule essa chamada de método e retorne um resultado apropriado.

Um aplicativo nunca explora ou se comunica com um dispositivo diretamente (a menos que ele chame [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) ou [**IWMDMStorage:: SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)); o aplicativo se comunica com o provedor de serviços, que deve representar um dispositivo na maneira mais lógica e simples possível. Quando o aplicativo solicita informações sobre o dispositivo ou enumera objetos no dispositivo, o provedor de serviços consulta o dispositivo de maneira apropriada e adquire e retorna as informações apropriadas. Ele pode expor a organização do arquivo no dispositivo de forma diferente de como ele está fisicamente armazenado no dispositivo, se isso for apropriado. No entanto, ele expõe o dispositivo, ele deve estar de maneira consistente e lógica, para permitir que o aplicativo encontre o que precisa e manipule os comandos que ele envia. Um bom provedor de serviços ocultará as peculiaridades específicas do dispositivo — por exemplo, se o dispositivo armazenar fisicamente uma lista de reprodução como um arquivo com uma extensão de arquivo Personalizada, o provedor de serviços deverá adicionar essa extensão automaticamente quando o aplicativo criar uma lista de reprodução no dispositivo; Não deve esperar que o aplicativo saiba a extensão apropriada ao criar um objeto de playlist.

Os provedores de serviço são executados dentro do processo do aplicativo de chamada. A única exceção é o provedor de serviços do MTP, que é executado em seu próprio processo. Por isso, há algum risco de que um provedor de serviços bloqueados faça com que o aplicativo de chamada seja bloqueado. Portanto, os provedores de serviços devem ser projetados para serem robustos e impedir o bloqueio, e os aplicativos devem ser criados para evitar a parada se uma chamada de método específica não retornar rapidamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](getting-started.md)
</dt> </dl>

 

 




