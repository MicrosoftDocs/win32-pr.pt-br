---
title: Funções do SDK do Windows Media Format
description: Funções
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows SDK de Formato de Mídia, funções
- ASF (Advanced Systems Format), functions
- ASF (Formato de Sistemas Avançados), funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560756451ee2f5b49d26b5611b38a40a45cac7643b101fdbe8ae492386901689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708256"
---
# <a name="windows-media-format-sdk-functions"></a>Funções do SDK do Windows Media Format

O Windows SDK de Formato de Mídia inclui funções para criar objetos e funções auxiliares para simplificar alguns procedimentos.

Esse SDK dá suporte às seguintes funções para a criação inicial de objetos. Se um objeto não estiver listado abaixo, você deverá criar usando uma interface de outro objeto. Para saber mais, confira [Objetos](objects.md).



| Função                                                                             | Descrição                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Examina a extensão de nome de arquivo na URL ou no nome do arquivo que é passado como um argumento                                                               |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Examina um protocolo de rede e o compara a uma lista interna de esquemas com suporte                                                                    |
| [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Cria um objeto do restaurador de backup.                                                                                                                       |
| [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Envolve os certificados do usuário em um objeto .                                                                                                           |
| [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Cria um objeto de registro de dispositivo.                                                                                                                   |
| [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Cria um objeto de transscriptografador DRM.                                                                                                                      |
| [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Cria um objeto do editor de metadados.                                                                                                                       |
| [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Cria um objeto indexador.                                                                                                                              |
| [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Cria um objeto do agente de revogação de licença.                                                                                                              |
| [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Cria um objeto do gerenciador de perfil.                                                                                                                       |
| [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Cria um objeto de leitor.                                                                                                                                |
| [**WMCreateSecureChannel**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Cria um objeto que implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**CERTIFICADO WMCreateSecureChannel \_**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Cria um objeto que implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**WMCreateSecureChannel \_ Certified \_ DES**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Cria um objeto que implementa [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)..                                                                        |
| [**WMCreateSecureChannel \_ DES**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Cria um objeto que implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Cria um objeto de leitor síncrono.                                                                                                                    |
| [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Cria um objeto de autor.                                                                                                                                |
| [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Cria um objeto de sink de arquivo de writer.                                                                                                                      |
| [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Cria um objeto de sink de rede de writer.                                                                                                                   |
| [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Cria um objeto de sink de push do autor.                                                                                                                      |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Verifica se um arquivo ASF pode ser tocado de uma cópia armazenada em cache.                                                                                             |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Verifica se há conteúdo protegido por DRM em um arquivo.                                                                                                                |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | Verifica se os dados do início de um arquivo são consistentes com a seção de header de um tipo de arquivo compatível com o SDK Windows Formato de Mídia. |



 

As funções a seguir fornecem atalhos convenientes para analisar arquivos.



| Função                                             | Descrição                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | Tenta determinar se um arquivo pode ser lido pelos objetos do SDK Windows Formato de Mídia, com base na extensão de nome de arquivo.              |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | Determina se um protocolo de rede é suportado pelos objetos do SDK Windows Formato de Mídia.                                           |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Determina se um arquivo está disponível para reprodução offline.                                                                                 |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Verifica se há conteúdo protegido por DRM em um arquivo.                                                                                                     |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | Tenta determinar se um arquivo pode ser lido pelos objetos do SDK Windows Formato de Mídia, analisando dados no início do arquivo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 
