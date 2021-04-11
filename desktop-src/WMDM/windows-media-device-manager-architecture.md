---
title: Arquitetura de Gerenciador de Dispositivos de mídia do Windows
description: Arquitetura de Gerenciador de Dispositivos de mídia do Windows
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Media Gerenciador de Dispositivos, arquitetura
- Gerenciador de Dispositivos, arquitetura
- arquitetura do Windows Media Gerenciador de Dispositivos
- Windows Media Gerenciador de Dispositivos, aplicativos de área de trabalho
- Gerenciador de Dispositivos, aplicativos de área de trabalho
- Windows Media Gerenciador de Dispositivos, provedores de serviços
- Gerenciador de Dispositivos, provedores de serviços
- Gerenciador de Dispositivos de mídia do Windows, plug-ins
- Gerenciador de Dispositivos, plug-ins
- aplicativos de desktop, arquitetura de Gerenciador de Dispositivos de mídia do Windows
- provedores de serviços, arquitetura de Gerenciador de Dispositivos de mídia do Windows
- plug-ins, arquitetura de Gerenciador de Dispositivos de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fda87e4ed4bce2c82bbb9c0863c119851965940
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159542"
---
# <a name="windows-media-device-manager-architecture"></a>Arquitetura de Gerenciador de Dispositivos de mídia do Windows

O Windows Media Gerenciador de Dispositivos permite que um aplicativo ou um plug-in se comunique com um dispositivo. Os aplicativos podem solicitar metadados de dispositivo, enumerar e explorar dispositivos anexados e enviar ou receber objetos (pastas, arquivos, listas de reprodução e assim por diante). O Windows Media Gerenciador de Dispositivos fornece uma única API para o aplicativo de chamada, não importa o tipo de dispositivo que está sendo chamado (classe MTP ou de armazenamento em massa, provedores de serviços criados na versão 10 ou provedores de serviços criados em versões anteriores do Windows Media Gerenciador de Dispositivos).

O Windows Media Gerenciador de Dispositivos atua como uma passagem entre os três principais componentes do sistema: o aplicativo, que faz solicitações (para obter informações, ler ou gravar dados etc.); um provedor de conteúdo seguro, que é um componente que lida com a comunicação com arquivos protegidos por DRM; e um provedor de serviços, que recebe solicitações do aplicativo e se comunica com o dispositivo para executar essas solicitações. O aplicativo e o provedor de serviços são criados no SDK do Windows Media Gerenciador de Dispositivos.

O diagrama a seguir mostra como um aplicativo de área de trabalho se comunica com um dispositivo usando o Windows Media Gerenciador de Dispositivos 11.

![diagrama mostrando um aplicativo que se comunica com quatro tipos diferentes de dispositivos.](images/wmdm-device-communication.gif)

O diagrama anterior mostra um aplicativo que se comunica com quatro tipos diferentes de dispositivos, cada um com seu próprio provedor de serviços. Cada provedor de serviços é projetado para se comunicar com um tipo específico de dispositivo; Este diagrama mostra os três provedores de serviços fornecidos pela Microsoft (drivers de classe genérica para dispositivos de classe de armazenamento em massa, dispositivos RAPI e dispositivos MTP), bem como um provedor de serviços personalizado para um dispositivo proprietário criado por terceiros. Quando um dispositivo se conecta, o Windows Media Gerenciador de Dispositivos instancia uma instância do provedor de serviços registrado para esse dispositivo. Os provedores de serviço obtêm solicitações do aplicativo por meio das interfaces do Windows Media Gerenciador de Dispositivos que elas implementam, usam os drivers apropriados para se comunicar com o dispositivo e retornam os resultados apropriados. A comunicação entre o provedor de serviços e o dispositivo está fora do domínio do Windows Media Gerenciador de Dispositivos.

Provedores de serviço são invisíveis para o aplicativo; um aplicativo vê apenas uma lista de "dispositivos" porque o Windows Media Gerenciador de Dispositivos expõe um conjunto padrão de métodos e interfaces para todos os dispositivos. Se um fabricante criar um provedor de serviços personalizado, ele deverá lidar com todos os métodos padrão de Gerenciador de Dispositivos de mídia do Windows se os aplicativos forem capazes de usar o dispositivo.

Esse diagrama também mostra um módulo SCP (provedor de conteúdo seguro). Este módulo é responsável por manipular conteúdo protegido por DRM (gerenciamento de direitos digitais). A Microsoft fornece um módulo SCP que pode lidar com arquivos WMA e WMV protegidos por DRM. Se um aplicativo ou dispositivo pretender lidar com outros formatos protegidos, ele deve fornecer seu próprio módulo SCP. Nem o aplicativo nem o provedor de serviços lidam diretamente com o SCP.

O aplicativo e o provedor de serviços são criados no Windows Media Gerenciador de Dispositivos, que roteia chamadas entre o aplicativo e o provedor de serviços apropriado para um dispositivo; o provedor de serviços é responsável pela comunicação direta com o dispositivo. O Windows Media Gerenciador de Dispositivos executa algumas ações em si (por exemplo, enumerando dispositivos conectados, chamadas de roteamento e manipulando a verificação de componentes); no entanto, a maior parte do trabalho é feita pelo provedor de serviços, que recebe solicitações do aplicativo e se comunica com o dispositivo.

Um aplicativo criado no Windows Media Gerenciador de Dispositivos pode se comunicar com dispositivos e provedores de serviço criados em versões anteriores do Windows Media Gerenciador de Dispositivos; no entanto, esses dispositivos mais antigos serão executados por meio de componentes da série 9 (não mostrados) e não oferecerão suporte aos recursos mais recentes, especialmente a tecnologia de gerenciamento de direitos digitais mais avançada.

Arquitetura de um dispositivo

O diagrama a seguir mostra uma hierarquia simplificada de dispositivos e armazenamentos, como visto por um aplicativo usando o Windows Media Gerenciador de Dispositivos.

![diagrama mostrando armazenamentos em um dispositivo.](images/wmdm-basic-device-layout.gif)

O diagrama anterior mostra uma versão simplificada de uma unidade flash conectada, como visto por um aplicativo do Windows Media Gerenciador de Dispositivos. A unidade flash tem atributos e propriedades, como um número de série e configurações de formato com suporte. Um filho imediato do dispositivo flash é o objeto de armazenamento raiz, que contém uma pasta, que contém uma imagem e uma música.

Um aplicativo enumera a lista de dispositivos anexados chamando um método de enumeração exposto pela interface [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) raiz. Os dispositivos são representados por uma interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (ou uma derivada). Essa interface expõe métodos para recuperar o nome do dispositivo, os recursos de formato, o número de série e assim por diante, bem como um método que enumera os *armazenamentos* no dispositivo. No Windows Media Gerenciador de Dispositivos, um armazenamento é qualquer tipo de objeto no dispositivo, seja ou não um blob real de dados. Por exemplo: Arquivos de áudio, arquivos de texto, pastas, listas de reprodução armazenadas como arquivos e listas de reprodução armazenadas como metadados são consideradas armazenamentos, mesmo que pastas e itens de metadados provavelmente não representem um arquivo físico. O tipo (ou formato) de um armazenamento pode ser recuperado chamando [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (ou [**GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata), solicitando o formato do armazenamento).

Os armazenamentos em um dispositivo são armazenados hierarquicamente e todos os dispositivos têm um armazenamento raiz. Cada armazenamento pode conter zero ou mais objetos filho, enumerados chamando o método [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) do armazenamento.

Observe que cada armazenamento no diagrama tem atributos e metadados associados a ele (nem todos os valores são mostrados). Os atributos são simples, as informações booleanas geralmente descrevem informações de gerenciamento ou de navegação (como "tem pastas&quot; ou &quot;pode excluir"), enquanto os metadados podem ser valores de cadeia de caracteres, números ou informações complexas (como recursos de renderização). Os atributos são descritos por um conjunto bastante limitado de sinalizadores definidos pelo SDK e recuperados chamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) ou [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Os valores de metadados são recuperados por um nome exclusivo; o SDK define vários valores de metadados aos quais os dispositivos devem dar suporte, mas os dispositivos podem definir suas próprias [constantes de metadados](metadata-constants.md). No entanto, se um dispositivo ou provedor de serviços definir uma nova constante de metadados, os aplicativos não poderão solicitar ou definir esse valor, a menos que os desenvolvedores de aplicativos estejam cientes dessa nova constante. Um provedor de serviços deve dar suporte a [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) ou posterior para dar suporte à recuperação ou à configuração de metadados. Para obter mais informações, consulte [obtendo e configurando metadados e atributos](getting-and-setting-metadata-and-attributes.md).

Provedores de serviço

O provedor de serviços atua como um meio entre o aplicativo e o dispositivo. O provedor de serviços é invisível para o desenvolvedor de aplicativos, portanto, um desenvolvedor de aplicativos não precisa saber nada sobre o desenvolvimento de um provedor de serviços. No entanto, é o provedor de serviços que faz o trabalho de comunicação com um dispositivo.

Um provedor de serviços é uma DLL COM criada no Windows Media Gerenciador de Dispositivos que recebe solicitações de um aplicativo e se comunica com o dispositivo para realizá-las. A comunicação com o aplicativo da área de trabalho é mediada pelo Windows Media Gerenciador de Dispositivos; a comunicação com o dispositivo está sob o controle do provedor de serviços.

Um provedor de serviços recebe solicitações do aplicativo para enumerar o conteúdo do dispositivo, solicitações de recursos do dispositivo, solicitações para ler ou gravar dados e assim por diante. Ele deve saber o design de um dispositivo bem suficiente para que ele possa enviar comandos no formato e protocolo adequados. Ele também deve ser capaz de ocultar requisitos específicos do dispositivo, como uma extensão de arquivo necessária para listas de reprodução, para que os aplicativos não precisem saber esses requisitos para usar o dispositivo.

A Microsoft fornece vários provedores de serviços para tipos de dispositivos padrão, incluindo dispositivos MTP genéricos, dispositivos de classe de armazenamento em massa e dispositivos RAPI. O único motivo pelo qual um designer de dispositivo deve precisar criar um provedor de serviços personalizado é se um dispositivo tem alguns requisitos de armazenamento de dados específicos ou incomuns que os provedores de serviço Standard não manipulam, por exemplo, se os arquivos devem ser armazenados em locais específicos e o sistema operacional do dispositivo não tratar isso automaticamente.

Quando um dispositivo está conectado ao computador, o sistema operacional cria uma instância do provedor de serviços apropriado para cada aplicativo do Windows Media Gerenciador de Dispositivos. Se um segundo aplicativo do Windows Media Gerenciador de Dispositivos for iniciado, uma segunda instância do provedor de serviços será carregada. No entanto, cada provedor de serviços pode lidar com vários dispositivos. O diagrama a seguir ilustra isso.

![diagrama mostrando dois dispositivos MTP se comunicando com dois aplicativos.](images/wmdm-sp-to-device.gif)

O diagrama anterior mostra dois aplicativos diferentes se comunicando com dois dispositivos MTP. Os dispositivos usam a mesma classe de provedor de serviços, mas cada aplicativo tem sua própria instância do mesmo provedor de serviços. Cada instância do provedor de serviços está se comunicando com dispositivos. As diferentes instâncias do provedor de serviços não estão cientes umas das outras.

Muitos métodos de aplicativo têm um método de provedor de serviços nomeado de forma correspondente. Quando o aplicativo chama um método, o Windows Media Gerenciador de Dispositivos roteia a chamada para o método correspondente no provedor de serviços (embora possa executar algumas ações internas adicionais primeiro). Por exemplo, quando o aplicativo chama [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty), o Windows Media Gerenciador de dispositivos roteia essa chamada para a implementação do provedor de serviços de [**IMDSPDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty). (A maioria das interfaces de aplicativo começa com IWMDM e a interface do provedor de serviço correspondente começa com IMDSP). Espera-se que o provedor de serviços manipule essa chamada de método e retorne um resultado apropriado.

Um aplicativo nunca explora ou se comunica com um dispositivo diretamente (a menos que ele chame [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) ou [**IWMDMStorage:: SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)); o aplicativo se comunica com o provedor de serviços, que deve representar um dispositivo na maneira mais lógica e simples possível. Quando o aplicativo solicita informações sobre o dispositivo ou enumera objetos no dispositivo, o provedor de serviços consulta o dispositivo de maneira apropriada e adquire e retorna as informações apropriadas. Ele pode expor a organização do arquivo no dispositivo de forma diferente de como ele está fisicamente armazenado no dispositivo, se isso for apropriado. No entanto, ele expõe o dispositivo, ele deve estar de maneira consistente e lógica, para permitir que o aplicativo encontre o que precisa e manipule os comandos que ele envia. Um bom provedor de serviços ocultará as peculiaridades específicas do dispositivo — por exemplo, se o dispositivo armazenar fisicamente uma lista de reprodução como um arquivo com uma extensão de arquivo Personalizada, o provedor de serviços deverá adicionar essa extensão automaticamente quando o aplicativo criar uma lista de reprodução no dispositivo; Não deve esperar que o aplicativo saiba a extensão apropriada ao criar um objeto de playlist.

Os provedores de serviço são executados dentro do processo do aplicativo de chamada. A única exceção é o provedor de serviços do MTP, que é executado em seu próprio processo. Por isso, há algum risco de que um provedor de serviços bloqueados faça com que o aplicativo de chamada seja bloqueado. Portanto, os provedores de serviços devem ser projetados para serem robustos e impedir o bloqueio, e os aplicativos devem ser criados para evitar a parada se uma chamada de método específica não retornar rapidamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](getting-started.md)
</dt> </dl>

 

 




