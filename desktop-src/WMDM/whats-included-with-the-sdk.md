---
title: O que está incluído no SDK
description: O que está incluído no SDK
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Media Gerenciador de Dispositivos, Software Development Kit (SDK)
- Gerenciador de Dispositivos, Software Development Kit (SDK)
- SDK do Windows Media Gerenciador de Dispositivos
- SDK do Gerenciador de Dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac1698336e1cf3966e3ab69ad3ae7c46f95e469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005146"
---
# <a name="whats-included-with-the-sdk"></a>O que está incluído no SDK

A tabela a seguir descreve o conteúdo do SDK do Windows Media Gerenciador de Dispositivos. Todos os arquivos ou pastas são descritos em relação ao caminho de instalação do SDK raiz.



| Arquivo                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Pasta de nível superior para o SDK do Windows Media Gerenciador de Dispositivos. Essa pasta inclui o makefile para a criação de todos os aplicativos de exemplo.                                                                                                                                                                                                                                                                                                              |
| inseri\\                      | Pasta que contém todos os arquivos IDL necessários para criar cabeçalhos necessários para os métodos do Windows Media Gerenciador de Dispositivos. No entanto, em vez de usar esses arquivos, você pode usar os arquivos de cabeçalho fornecidos na \\ pasta Inc.<br/> Para ver uma lista desses arquivos IDL e saber quais arquivos de cabeçalho são criados a partir de quais arquivos IDL, consulte [compilando os arquivos IDL fornecidos com o SDK](compiling-the-idl-files-supplied-with-the-sdk.md).<br/> |
| Inc \\ ...<br/>       | Pasta que inclui todos os cabeçalhos que definem as interfaces e os tipos de dados neste SDK.                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm. h                   | Define todas as interfaces de aplicativo, interfaces de provedor de serviço, interfaces de provedor de conteúdo seguro, códigos de erro, constantes, estruturas e a interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .                                                                                                                                                                                                                            |
| mswmdm \_ i. c                | Define a interface [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) .                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt. h                   | Define estruturas específicas de MTP necessárias para aplicativos que chamam [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol).                                                                                                                                                                                                                                                                                                            |
| recurso. h                 | Define várias constantes de recurso usadas pelas amostras do SDK.                                                                                                                                                                                                                                                                                                                                                                                         |
| SAC. h                      | Define dados de canal autenticados seguros exigidos por todos os aplicativos e provedores de serviços.                                                                                                                                                                                                                                                                                                                                                       |
| scclient. h                 | Define a classe [CSecureChannelClient](csecurechannelclient-class.md) exigida por todos os aplicativos.                                                                                                                                                                                                                                                                                                                                              |
| scserver. h                 | Define a classe [CSecureChannelServer](csecurechannelserver-class.md) exigida por todos os provedores de serviço.                                                                                                                                                                                                                                                                                                                                         |
| WMDM \_ ver. h                | Informações de versão opcionais sobre o Windows Media Gerenciador de Dispositivos.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog. h, wmdmlog \_ i. c    | Necessário para aplicativos ou provedores de serviço que usam a interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp. h           | Necessário para aplicativos que lidam com a medição de conteúdo (consulte [medição do uso de conteúdo](metering-content-usage.md)).                                                                                                                                                                                                                                                                                                                                  |
| wmsstd. h                   | Define as macros auxiliares usadas pelas amostras do SDK.                                                                                                                                                                                                                                                                                                                                                                                                      |
| lib\\                      | Pasta que contém as bibliotecas de Gerenciador de Dispositivos de mídia do Windows.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp. lib               | A biblioteca estática exigida por todos os aplicativos do Windows Media Gerenciador de Dispositivos e provedores de serviços.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto. lib              | A biblioteca estática exigida por todos os aplicativos do Windows Media Gerenciador de Dispositivos e provedores de serviço que usam DRM.                                                                                                                                                                                                                                                                                                                                    |
| MDSP \\ ...<br/>      | Pasta que contém o código para um provedor de serviços de exemplo. Para obter informações sobre esse exemplo, incluindo como compilá-lo e executá-lo, consulte [exemplo de provedor de serviços](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| aplicativos \\ ....<br/>      | Pasta que contém duas subpastas que contêm duas metades do código para um aplicativo de área de trabalho de exemplo fornecido com o SDK. Para obter informações sobre esse exemplo, incluindo como compilá-lo, consulte [exemplo de aplicativo de desktop](sample-desktop-application.md).                                                                                                                                                                                      |
| DeviceKit \\ ...<br/> | Pasta que contém um conjunto de ferramentas para testar seu dispositivo portátil usando o Windows Media Gerenciador de Dispositivos 11. O teste inclui enumeração e transferência de dispositivo e arquivo, recursos DRM e conformidade MTP. Essas ferramentas têm seu próprio arquivo de documentação.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](getting-started.md)
</dt> </dl>

 

 





