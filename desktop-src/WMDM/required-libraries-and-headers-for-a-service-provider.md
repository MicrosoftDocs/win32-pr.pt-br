---
title: Bibliotecas e cabeçalhos necessários para um provedor de serviços
description: Bibliotecas e cabeçalhos necessários para um provedor de serviços
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Gerenciador de Dispositivos de mídia do Windows, bibliotecas
- Gerenciador de Dispositivos, bibliotecas
- Guia de programação, bibliotecas
- provedores de serviços, bibliotecas
- criando provedores de serviços, bibliotecas
- bibliotecas
- Windows Media Gerenciador de Dispositivos, arquivos de cabeçalho
- Gerenciador de Dispositivos, arquivos de cabeçalho
- Guia de programação, arquivos de cabeçalho
- provedores de serviços, arquivos de cabeçalho
- criando provedores de serviços, arquivos de cabeçalho
- arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292282"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Bibliotecas e cabeçalhos necessários para um provedor de serviços

Esta seção lista as bibliotecas, os arquivos de cabeçalho ou os arquivos IDL que você precisará incluir para desenvolver um aplicativo de Gerenciador de Dispositivos de mídia do Windows ou um plug-in. Conforme mencionado na [compilação dos arquivos IDL fornecidos com o SDK](compiling-the-idl-files-supplied-with-the-sdk.md), o SDK inclui arquivos IDL e arquivos de cabeçalho predefinidos, e seu aplicativo pode usar qualquer um deles. (Observe que alguns arquivos de cabeçalho não têm arquivos IDL correspondentes e você não pode criá-los por conta própria.) Se você estiver criando seus próprios arquivos IDL, inclua as dependências listadas em compilando os arquivos IDL fornecidos com o SDK.

Nem todos os aplicativos precisarão de todos os arquivos; Leia a descrição para saber se seu aplicativo requer um arquivo.



| Cabeçalho ou biblioteca predefinida       | IDL equivalente                                                                | Descrição                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | none                                                                          | Exigido por todos os provedores de serviço. Define os objetos do Windows Media Gerenciador de Dispositivos.                                                                                                                                                                               |
| Initguid. h                       | Nenhum (cabeçalho SDK da plataforma)                                                    | Exigido por todos os provedores de serviços para definir os valores de **GUID** usando o arquivo predefinido Mswmdm. h. Você deve incluir Initguid. h apenas uma vez no seu projeto. Esse cabeçalho redefine a macro **definir \_ GUID** para evitar problemas de nomenclatura de **GUID** externo. |
| mswmdm. h                         | WMDM. idl<br/> WMSP. idl<br/> icomponentauthenticate. idl<br/> | Exigido por todos os provedores de serviço. Define todas as interfaces de provedor de serviços, estruturas, metadados, códigos de erro e outras constantes.                                                                                                                        |
| SAC. h                            | none                                                                          | Exigido por todos os provedores de serviço. Define os protocolos SAC.                                                                                                                                                                                                      |
| scserver. h                       | none                                                                          | Exigido por todos os provedores de serviço. Declara a classe [CSecureChannelServer](csecurechannelserver-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                                                   | Exigido pelos provedores de serviço que usam a interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| WMSDK. h                          | Nenhum (fornecido pelo SDK do Windows Media Format)                                   | Necessário para provedores de serviços que usam métodos do SDK do Windows Media Format.                                                                                                                                                                                      |
| WMVCORE. lib                      | none                                                                          | Exigido por provedores de serviço que usam funções ou objetos do Windows Media Format SDK.                                                                                                                                                                          |
| Mmreg. h                          | Nenhum (cabeçalho SDK da plataforma)                                                    | Exigido pelos provedores de serviço que fazem referência a várias definições padrão de formato de mídia do Windows, como **WAVEFORMATEX**.                                                                                                                                      |
| MtpExt. h                         | none                                                                          | Necessário para provedores de serviços que manipulam [**IMDSPDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) em dispositivos MTP. Define várias constantes e estruturas padrão do MTP.                                                                        |
| Chave. c                            | none                                                                          | Define uma chave e um certificado da Microsoft. A versão fornecida com o SDK inclui uma chave fictícia de teste que permitirá o uso de arquivos de mídia do Windows não protegidos por DRM.                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 





