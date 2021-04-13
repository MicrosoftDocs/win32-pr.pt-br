---
title: Objetos (SDK do Windows Media Format 11)
description: Objetos
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- SDK do Windows Media Format, objetos
- ASF (Advanced Systems Format), objetos
- ASF (formato de sistemas avançados), objetos
- objetos, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d73672891395d6491009e1c62fac1f9eb81dfe
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369172"
---
# <a name="objects-windows-media-format-11-sdk"></a>Objetos (SDK do Windows Media Format 11)

O SDK do Windows Media Format usa vários objetos para ler, gravar, editar e indexar arquivos ASF, bem como para criar e editar perfis. Cada objeto dá suporte a várias interfaces. Há suporte para algumas interfaces em vários objetos. Nesses casos, todas as diferenças na implementação são discutidas na seção de referência para a interface.

Os objetos no Windows Media Format SDK são compatíveis COM. Para facilitar o desenvolvimento, cada objeto tem uma função ou um método de criação associado. Você deve criar objetos usando a função ou o método de criação em vez de usar manualmente a função COM **CoCreateInstance**.

Algumas interfaces têm um número acrescentado a seus nomes, como **IWMProfile2** e **IWMWriter3**. Em cada caso, as versões numeradas herdam todos os métodos das versões anteriores e adicionam uma nova funcionalidade.

Em cada página de objeto dessa referência, as interfaces incluídas no objeto COM principal são listadas primeiro, seguidas por interfaces de retorno de chamada que devem ser implementadas pelo aplicativo.

A tabela a seguir lista os objetos com suporte neste SDK com uma descrição da funcionalidade de cada e a função usada para criá-lo.



| Objeto                                                          | Descrição                                                                                                                                              | Função de criação                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Restaurador de backup](backup-restorer-object.md)                   | Faz backup de licenças, normalmente em mídia removível, e restaura essas licenças em um computador diferente.                                           | [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Registro de dispositivo](device-registration-object.md)           | Gerencia o banco de dados de registro de dispositivo, que contém entradas para dispositivos de reprodução de mídia que estão disponíveis por meio de uma conexão de rede.             | [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [Criptografador de DRM](drm-transcryptor-object.md)                 | Converte dados de mídia protegidos por DRM em um fluxo de dados que pode ser enviado para dispositivos que usam o protocolo Windows Media DRM 10 para dispositivos de rede. | [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Indexador](indexer-object.md)                                   | Cria um índice para arquivos ASF para permitir a busca em arquivos com fluxos de vídeo.                                                                            | [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Agente de revogação de licença](license-revocation-agent-object.md) | Gerencia a revogação de licenças.                                                                                                                              | [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Editor de metadados](metadata-editor-object.md)                   | Edita metadados em um cabeçalho de arquivo ASF.                                                                                                                    | [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Gerenciador de Perfis](profile-manager-object.md)                   | Fornece interfaces para criar, carregar e salvar perfis. Um perfil é necessário para gravar um arquivo ASF.                                                      | [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Leitor](reader-object.md)                                     | Lê arquivos ASF. Esse objeto usa um modelo de chamada assíncrona para suas operações.                                                                      | [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Leitor síncrono](synchronous-reader-object.md)             | Lê arquivos ASF usando chamadas síncronas.                                                                                                                 | [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Escritor](writer-object.md)                                     | Grava arquivos ASF.                                                                                                                                        | [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Coletor de arquivos do gravador](writer-file-sink-object.md)                 | Controla arquivos ASF gravados pelo objeto gravador.                                                                                                         | [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Coletor de rede do gravador](writer-network-sink-object.md)           | Controla o streaming de rede ao vivo de arquivos ASF gravados pelo objeto gravador.                                                                               | [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Coletor de push de gravador](writer-push-sink-object.md)                 | Controla a entrega de conteúdo de streaming para servidores de publicação.                                                                                            | [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

A tabela a seguir lista os objetos que dependem de outros objetos. Esses objetos são criados por métodos de objetos existentes.



| Objeto                                                        | Descrição                                                                                                                                                                                                                                                                                                                           | Método de criação                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compartilhamento de largura de banda](bandwidth-sharing-object.md)             | Gerencia informações de compartilhamento de largura de banda em um perfil. Pode existir mais de um objeto de compartilhamento de largura de banda para um perfil. Há métodos diferentes para criar um objeto de compartilhamento de largura de banda, dependendo se você deseja criar um novo objeto de compartilhamento de largura de banda ou acessar um existente.                                           | [**IWMProfile3:: CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) OR<br/> [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | Contém um exemplo de mídia e todas as extensões de unidade de dados associadas. Usado para exemplos de escrita e leitura.                                                                                                                                                                                                                           | [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) OR<br/> [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> OU<br/> [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> OU<br/> Criado automaticamente pelo objeto Reader ou objeto leitor síncrono para entrega de exemplo.<br/> |
| [Propriedades de mídia de entrada](input-media-properties-object.md)   | Gerencia as propriedades de uma entrada. Um objeto de propriedades de entrada pode existir para cada entrada.                                                                                                                                                                                                                                             | [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Exclusão mútua](mutual-exclusion-object.md)               | Gerencia informações de exclusão mútua em um perfil. Os usos comuns para a exclusão mútua são o conteúdo de taxa de bits múltipla e as trilhas sonoras em várias linguagens. Há métodos diferentes para criar um objeto de exclusão mútua dependendo se você deseja criar um novo objeto de exclusão mútua ou acessar um existente.         | [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) OR<br/> [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Propriedades da mídia de saída](output-media-properties-object.md) | Gerencia as propriedades de uma saída. Um objeto de propriedades de mídia de saída pode existir para cada saída. Esses objetos podem ser criados pelo leitor ou pelo leitor síncrono                                                                                                                                                            | [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) OR<br/> [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Perfil](profile-object.md)                                 | Contém os dados em um perfil enquanto ele está sendo manipulado. Os objetos de perfil são criados sempre que o perfil precisa ser manipulado. Há métodos diferentes para criar um objeto de perfil, dependendo se você deseja criar um novo perfil ou acessar um existente.                                                  | [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) OR<br/> [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> OU<br/> [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> OU<br/> [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Configuração de fluxo](stream-configuration-object.md)       | Gerencia as propriedades de um fluxo em um perfil. Os objetos de configuração de fluxo são criados por objetos de fluxo sempre que você precisar acessar as informações sobre um fluxo. Há métodos diferentes para criar um objeto de configuração de fluxo, dependendo se você deseja criar um novo fluxo ou acesso e um existente. | [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) OR<br/> [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> OU<br/> [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Priorização de fluxo](stream-prioritization-object.md)     | Mantém a lista de prioridades de fluxo para um perfil. Os fluxos serão descartados em ordem de prioridade crescente se a largura de banda disponível for restrita. Só pode haver um objeto de priorização de fluxo em um perfil.                                                                                                                  | [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 





