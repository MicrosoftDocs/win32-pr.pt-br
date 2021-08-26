---
title: O que está incluído no SDK
description: O que está incluído no SDK
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows SDK (kit Gerenciador de Dispositivos de mídia), software development kit (SDK)
- Gerenciador de Dispositivos,SDK (software development kit)
- Windows SDK Gerenciador de Dispositivos mídia
- SDK do Gerenciador de Dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36e621ac4de7fee296bf9d2c3ffb4e1d357824510b37a6ded73efd66b91f38d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004896"
---
# <a name="whats-included-with-the-sdk"></a>O que está incluído no SDK

A tabela a seguir descreve o conteúdo do SDK Windows Media Gerenciador de Dispositivos. Todos os arquivos ou pastas são descritos em relação ao caminho de instalação do SDK raiz.



| Arquivo                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Pasta de nível superior para o SDK Windows Media Gerenciador de Dispositivos. Essa pasta inclui o makefile para criar todos os aplicativos de exemplo.                                                                                                                                                                                                                                                                                                              |
| Idl\\                      | Pasta que contém todos os arquivos IDL necessários para criar os headers necessários para Windows mídia Gerenciador de Dispositivos métodos. No entanto, em vez de usar esses arquivos, você pode usar os arquivos de header fornecidos na pasta \\ inc.<br/> Para ver uma lista desses arquivos IDL e saber quais arquivos de header são compilados com base em quais arquivos IDL, consulte Compilando os arquivos IDL fornecidos com o [SDK](compiling-the-idl-files-supplied-with-the-sdk.md).<br/> |
| inc \\ ....<br/>       | Pasta que inclui todos os headers que definem as interfaces e os tipos de dados neste SDK.                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm.h                   | Define todas as interfaces do aplicativo, as interfaces do provedor de serviços, as interfaces do provedor de conteúdo seguro, os códigos de erro, as constantes, as estruturas e a interface [**IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)                                                                                                                                                                                                                            |
| mswmdm \_ i.c                | Define a interface [**IWMDMNotification.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt.h                   | Define as estruturas específicas do MTP necessárias para aplicativos que chamam [**IWMDMDevice3::D eviceIoControl.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol)                                                                                                                                                                                                                                                                                                            |
| resource.h                 | Define várias constantes de recurso usadas pelos exemplos do SDK.                                                                                                                                                                                                                                                                                                                                                                                         |
| sac.h                      | Define os dados de canal autenticados seguros exigidos por todos os aplicativos e provedores de serviços.                                                                                                                                                                                                                                                                                                                                                       |
| scclient.h                 | Define a [classe CSecureChannelClient](csecurechannelclient-class.md) exigida por todos os aplicativos.                                                                                                                                                                                                                                                                                                                                              |
| scserver.h                 | Define a [classe CSecureChannelServer](csecurechannelserver-class.md) exigida por todos os provedores de serviços.                                                                                                                                                                                                                                                                                                                                         |
| wmdm \_ ver.h                | Informações de versão opcionais sobre Windows mídia Gerenciador de Dispositivos.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog.h, wmdmlog \_ i.c    | Necessário para aplicativos ou provedores de serviços que usam a interface [**IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp.h           | Necessário para aplicativos que lidam com a medição de conteúdo (consulte [Uso de conteúdo de medição).](metering-content-usage.md)                                                                                                                                                                                                                                                                                                                                  |
| wmsstd.h                   | Define macros auxiliares usadas pelos exemplos do SDK.                                                                                                                                                                                                                                                                                                                                                                                                      |
| Lib\\                      | Pasta que contém as bibliotecas Windows Media Gerenciador de Dispositivos.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp.lib               | A biblioteca estática exigida por todos os Windows mídia Gerenciador de Dispositivos aplicativos e provedores de serviços.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto.lib              | A biblioteca estática exigida por todos os Windows mídia Gerenciador de Dispositivos aplicativos e provedores de serviços que usam DRM.                                                                                                                                                                                                                                                                                                                                    |
| mdsp \\ ....<br/>      | Pasta que contém o código de um provedor de serviços de exemplo. Para obter informações sobre este exemplo, incluindo como compilá-lo e executar, consulte [Provedor de Serviços de Exemplo](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| aplicativos \\ ....<br/>      | Pasta que contém duas subpastas que contêm duas metades do código para um aplicativo de área de trabalho de exemplo fornecido com o SDK. Para obter informações sobre este exemplo, incluindo como compilá-lo, consulte [Aplicativo de área de trabalho de exemplo.](sample-desktop-application.md)                                                                                                                                                                                      |
| devicekit \\ ....<br/> | Pasta que contém um conjunto de ferramentas para testar seu dispositivo portátil usando Windows Mídia Gerenciador de Dispositivos 11. O teste inclui enumeração e transferência de dispositivos e arquivos, funcionalidades de DRM e conformidade com MTP. Essas ferramentas têm seu próprio arquivo de documentação.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Ponto de Partida**](getting-started.md)
</dt> </dl>

 

 





