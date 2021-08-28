---
title: Interfaces para aplicativos
description: Interfaces para aplicativos
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Interfaces de Gerenciador de Dispositivos mídia, interfaces de aplicativo
- Gerenciador de Dispositivos, interfaces de aplicativo
- aplicativos da área de trabalho, interfaces
- referência de programação, interfaces de aplicativo
- referência para Windows mídia Gerenciador de Dispositivos, interfaces de aplicativo
- plug-ins, interfaces
- interfaces de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690b8419a7f04ef2b4eab1db65266027bdf5bcf3a102e59a95030a290e3747ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619947"
---
# <a name="interfaces-for-applications"></a>Interfaces para aplicativos

Esta seção descreve as interfaces usadas ou implementadas por aplicativos usando o SDK Windows Media Gerenciador de Dispositivos para se comunicar com dispositivos. O termo "aplicativo" usado aqui significa qualquer objeto EXECUTÁVEL, plug-in ou COM que existe em um computador desktop e precisa de comunicação de alto nível com um dispositivo portátil conectado. Isso pode incluir um aplicativo de player de mídia, um plug-in Windows Media Player (se precisar de acesso direto a um dispositivo portátil) ou um objeto COM de medição de contagem de reprodução.

Algumas dessas interfaces são implementadas pelo aplicativo, enquanto outras são chamadas pelo aplicativo. A documentação de cada interface indica se ela é implementada ou chamada (e, se implementada, se é opcional ou necessária).

As seguintes interfaces ou classes são usadas por aplicativos.



| Interface ou classe                                           | Descrição                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classe CSecureChannelClient](csecurechannelclient-class.md) | Uma classe auxiliar que permite que os aplicativos se autententem, criptografem e descriptografem dados e criem MACs.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | A interface de Windows media Gerenciador de Dispositivos para aplicativos.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Estende **IWMDeviceManager fornecendo** métodos de enumeração avançados e outros métodos.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Estende a interface **IWMDeviceManager2** fornecendo um método que define a preferência de enumeração do dispositivo.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Fornece métodos para examinar e explorar um único dispositivo portátil.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Estende **IWMDMDevice,** possibilitando obter os formatos de vídeo com suporte por um dispositivo, encontrar um armazenamento por nome e usar páginas de propriedades.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Estende **IWMDMDevice2** fornecendo métodos para consultar propriedades em um dispositivo, enviar códigos de controle de E/S do dispositivo e também fornecer métodos atualizados para pesquisar armazenamentos e recuperar recursos de formato de dispositivo. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Fornece métodos para controlar dispositivos.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Melhora a eficiência das operações de dispositivo, ao fazer o adendo de várias operações em uma sessão                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Enumera dispositivos portáteis anexados a um computador.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Enumera armazenamentos em um dispositivo.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Define e recupera propriedades de metadados (como o artista, o álbum, o gênero e assim por diante) de um armazenamento.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Obtém e define informações que controlam como os arquivos reproduzíveis no dispositivo são manipulados pela interface **IWMDMDeviceControl**                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Recupera a URL da qual os componentes atualizados podem ser baixados, se uma transferência falhar com um erro de revogação.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Fornece métodos para examinar e explorar um armazenamento (arquivo, pasta, playlist) em um dispositivo.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Estende **O IWMDMStorage** possibilita obter um armazenamento filho por nome e obter e definir atributos estendidos.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Estende **IWMDMStorage2** expondo metadados.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Estende **IWMDMStorage3** fornecendo métodos para recuperar um subconjunto de metadados disponíveis para um armazenamento e para definir e recuperar uma lista de referências a outros armazenamentos.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Usado para inserir, excluir ou mover arquivos dentro de um dispositivo ou entre um dispositivo e o computador.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Estende **IWMDMStorageControl** possibilitando definir o nome do arquivo de destino ao inserir conteúdo em um armazenamento.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Estende **IWMDMStorageControl2,** possibilitando a passagem de um ponteiro de interface **IWMDMMetaData.**                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Fornece métodos para recuperar informações globais sobre uma mídia de armazenamento (como um cartão ROM flash) em um dispositivo.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Permite que um aplicativo execute medição, sincronização de licença e atualização dos componentes drm de um dispositivo.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Estende **IWMDRMDeviceApp** fornecendo uma nova versão do **método QueryDeviceStatus.**                                                                                                                         |



 

Interfaces de retorno de chamada

As interfaces opcionais a seguir são implementadas por um aplicativo para acompanhar o progresso de uma solicitação assíncrona, como uma solicitação de leitura ou gravação.



| Interface                                      | Descrição                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Permite que aplicativos e provedores de serviços recebam notificações quando dispositivos ou armazenamentos de memória (como cartões RAM) estão conectados ou desconectados do computador. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Estende **IWMDMOperation** fornecendo métodos para obter e definir atributos estendidos.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Estende **IWMDMOperation** fornecendo um novo método para transferir dados não criptografados para maior eficiência.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Permite que um aplicativo controle como os dados são lidos ou gravados no computador durante uma transferência de arquivo.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Estende o **método IWMDMProgress::End** fornecendo um indicador de status.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Estende **IWMDMProgress2** fornecendo parâmetros de entrada adicionais para especificar a ID do evento e informações específicas do contexto.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Permite que um aplicativo acompanhe o progresso das operações, como formatação de mídia ou transferências de arquivos.                                                                  |



 

O diagrama a seguir mostra como a maioria das interfaces de aplicativo importantes é adquirida da interface **IWMDeviceManager** raiz. Um aplicativo obtém essa interface raiz cocriando o objeto MediaDevMgr, solicitando a interface **IComponentAuthenticate,** autenticando o componente e solicitando **o IWMDeviceManager** (essas etapas são descritas em Autenticando [o aplicativo](authenticating-the-application.md)). Depois que essa interface raiz tiver sido adquirida, [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) será chamado para criar um objeto que implementa [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). Outras interfaces são obtidas chamando métodos em interfaces na ordem mostrada. Interfaces derivadas, como [**IWMDMDevice2,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) são obtidas chamando **QueryInterface** na interface base.

No diagrama a seguir, as interfaces derivadas são rotuladas por marcas de barra; portanto, "IWMDMStorage/2/3" indicaria **IWMDMStorage,** **IWMDMStorage2** e **IWMDMStorage3**.

![diagrama mostrando como obter as principais interfaces de aplicativo no Gerenciador de Dispositivos de Mídia do Windows.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 




