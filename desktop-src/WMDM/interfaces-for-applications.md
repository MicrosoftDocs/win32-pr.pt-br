---
title: Interfaces para aplicativos
description: Interfaces para aplicativos
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Media Gerenciador de Dispositivos, interfaces de aplicativo
- Gerenciador de Dispositivos, interfaces de aplicativo
- aplicativos de área de trabalho, interfaces
- referência de programação, interfaces de aplicativo
- referência para Windows Media Gerenciador de Dispositivos, interfaces de aplicativo
- plug-ins, interfaces
- interfaces de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49d66272c42679fd38d01b0114a834ee6f33e92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292284"
---
# <a name="interfaces-for-applications"></a>Interfaces para aplicativos

Esta seção descreve as interfaces usadas ou implementadas por aplicativos que usam o SDK do Windows Media Gerenciador de Dispositivos para se comunicar com dispositivos. O termo "aplicativo" usado aqui significa qualquer executável, plug-in ou objeto COM existente em um computador desktop e precisa de comunicação de alto nível com um dispositivo portátil conectado. Isso pode incluir um aplicativo de player de mídia, um plug-in do Windows Media Player (se ele precisar de acesso direto a um dispositivo portátil) ou um objeto COM de medição de contagem de reprodução.

Algumas dessas interfaces são implementadas pelo aplicativo, enquanto outras são chamadas pelo aplicativo. A documentação de cada interface indica se ela é implementada ou chamada (e, se implementada, se é opcional ou necessária).

As seguintes interfaces ou classes são usadas por aplicativos.



| Interface ou classe                                           | Descrição                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classe CSecureChannelClient](csecurechannelclient-class.md) | Uma classe auxiliar que permite que os aplicativos se autentiquem, criptografem e descriptografem dados e criem MACs.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | A interface de nível superior do Windows Media Gerenciador de Dispositivos para aplicativos.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Estende o **IWMDeviceManager** fornecendo métodos de enumeração avançados e outros métodos.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Estende a interface **IWMDeviceManager2** fornecendo um método que define a preferência de enumeração de dispositivo.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Fornece métodos para examinar e explorar um único dispositivo portátil.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Estende o **IWMDMDevice** ao tornar possível obter os formatos de vídeo com suporte de um dispositivo, localizar um armazenamento por nome e usar páginas de propriedades.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Estende o **IWMDMDevice2** fornecendo métodos para consultar um dispositivo para propriedades, enviar códigos de controle de e/s de dispositivo e também fornecer métodos atualizados para pesquisar armazenamentos e recuperar recursos de formato de dispositivo. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Fornece métodos para controlar dispositivos.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Melhora a eficiência das operações de dispositivo agrupando várias operações em uma sessão                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Enumera dispositivos portáteis anexados a um computador.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Enumera armazenamentos em um dispositivo.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Define e recupera propriedades de metadados (como artista, álbum, gênero e assim por diante) de um armazenamento.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Obtém e define informações que controlam como os arquivos reproduzidos no dispositivo são manipulados pela interface **IWMDMDeviceControl**                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Recupera a URL da qual os componentes atualizados podem ser baixados, se uma transferência falhar com um erro de revogação.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Fornece métodos para examinar e explorar um armazenamento (arquivo, pasta, lista de reprodução) em um dispositivo.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Estende o **IWMDMStorage** tornando possível obter um armazenamento filho por nome e obter e definir atributos estendidos.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Estende o **IWMDMStorage2** expondo os metadados.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Estende o **IWMDMStorage3** fornecendo métodos para recuperar um subconjunto de metadados disponíveis para um armazenamento e para configurar e recuperar uma lista de referências a outros armazenamentos.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Usado para inserir, excluir ou mover arquivos em um dispositivo ou entre um dispositivo e o computador.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Estende o **IWMDMStorageControl** tornando possível definir o nome do arquivo de destino ao inserir o conteúdo em um armazenamento.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Estende o **IWMDMStorageControl2** , tornando possível passar um ponteiro de interface **IWMDMMetaData** .                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Fornece métodos para recuperar informações globais sobre um meio de armazenamento (como uma placa Flash ROM) em um dispositivo.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Permite que um aplicativo execute a medição, a sincronização de licenças e a atualização dos componentes DRM de um dispositivo.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Estende o **IWMDRMDeviceApp** fornecendo uma nova versão do método **QueryDeviceStatus** .                                                                                                                         |



 

Interfaces de retorno de chamada

As seguintes interfaces opcionais são implementadas por um aplicativo para acompanhar o progresso de uma solicitação assíncrona, como uma solicitação de leitura ou gravação.



| Interface                                      | Descrição                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Permite que aplicativos e provedores de serviços recebam notificações quando dispositivos ou armazenamentos de memória (como placas de RAM) são conectados ou desconectados do computador. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Estende **IWMDMOperation** fornecendo métodos para obter e definir atributos estendidos.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Estende o **IWMDMOperation** fornecendo um novo método para transferir dados descriptografados para maior eficiência.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Permite que um aplicativo controle como os dados são lidos ou gravados no computador durante uma transferência de arquivo.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Estende o método **IWMDMProgress:: End** fornecendo um indicador de status.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Estende o **IWMDMProgress2** fornecendo parâmetros de entrada adicionais para especificar a ID do evento e informações específicas do contexto.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Permite que um aplicativo acompanhe o progresso das operações, como formatação de mídia ou transferências de arquivos.                                                                  |



 

O diagrama a seguir mostra como a maioria das interfaces de aplicativo importantes são adquiridas da interface **IWMDeviceManager** raiz. Um aplicativo obtém essa interface raiz colocando o objeto MediaDevMgr, solicitando a interface **IComponentAuthenticate** , Autenticando o componente e, em seguida, solicitando o **IWMDeviceManager** (essas etapas são descritas em [Autenticando o aplicativo](authenticating-the-application.md)). Depois que essa interface raiz tiver sido adquirida, [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) será chamado para criar um objeto que implementa [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). Outras interfaces são obtidas chamando métodos em interfaces na ordem mostrada. Interfaces derivadas, como [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) , são obtidas chamando **QueryInterface** na interface base.

No diagrama a seguir, as interfaces derivadas são rotuladas por barras, de modo que "IWMDMStorage/2/3" indicaria **IWMDMStorage**, **IWMDMStorage2** e **IWMDMStorage3**.

![diagrama mostrando como obter as principais interfaces de aplicativo no Gerenciador de dispositivos do Windows Media.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 




