---
title: Bibliotecas e cabeçalhos necessários para um provedor de serviços
description: Bibliotecas e cabeçalhos necessários para um provedor de serviços
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Gerenciador de Dispositivos de mídia, bibliotecas
- Gerenciador de Dispositivos, bibliotecas
- Guia de programação, bibliotecas
- provedores de serviços, bibliotecas
- criando provedores de serviços, bibliotecas
- bibliotecas
- Windows Gerenciador de Dispositivos de mídia, arquivos de cabeçalho
- Gerenciador de Dispositivos, arquivos de cabeçalho
- Guia de programação, arquivos de cabeçalho
- provedores de serviços, arquivos de cabeçalho
- criando provedores de serviços, arquivos de cabeçalho
- arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72628d2f8582e7d729e27d7745ff1716c376d475afcaa48e52099f6cf63d2d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903926"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Bibliotecas e cabeçalhos necessários para um provedor de serviços

esta seção lista as bibliotecas, os arquivos de cabeçalho ou os arquivos IDL que você precisará incluir para desenvolver um Windows mídia Gerenciador de Dispositivos aplicativo ou plug-in. Conforme mencionado na [compilação dos arquivos IDL fornecidos com o SDK](compiling-the-idl-files-supplied-with-the-sdk.md), o SDK inclui arquivos IDL e arquivos de cabeçalho predefinidos, e seu aplicativo pode usar qualquer um deles. (Observe que alguns arquivos de cabeçalho não têm arquivos IDL correspondentes e você não pode criá-los por conta própria.) Se você estiver criando seus próprios arquivos IDL, inclua as dependências listadas em compilando os arquivos IDL fornecidos com o SDK.

Nem todos os aplicativos precisarão de todos os arquivos; Leia a descrição para saber se seu aplicativo requer um arquivo.



| Cabeçalho ou biblioteca predefinida       | IDL equivalente                                                                | Descrição                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | nenhum                                                                          | Exigido por todos os provedores de serviço. define Windows Gerenciador de Dispositivos objetos de mídia.                                                                                                                                                                               |
| Initguid. h                       | Nenhum (cabeçalho SDK da plataforma)                                                    | Exigido por todos os provedores de serviços para definir os valores de **GUID** usando o arquivo predefinido Mswmdm. h. Você deve incluir Initguid. h apenas uma vez no seu projeto. Esse cabeçalho redefine a macro **definir \_ GUID** para evitar problemas de nomenclatura de **GUID** externo. |
| mswmdm. h                         | WMDM. idl<br/> WMSP. idl<br/> icomponentauthenticate. idl<br/> | Exigido por todos os provedores de serviço. Define todas as interfaces de provedor de serviços, estruturas, metadados, códigos de erro e outras constantes.                                                                                                                        |
| SAC. h                            | nenhum                                                                          | Exigido por todos os provedores de serviço. Define os protocolos SAC.                                                                                                                                                                                                      |
| scserver. h                       | nenhum                                                                          | Exigido por todos os provedores de serviço. Declara a classe [CSecureChannelServer](csecurechannelserver-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                                                   | Exigido pelos provedores de serviço que usam a interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| WMSDK. h                          | nenhum (fornecido pelo SDK do formato de mídia Windows)                                   | necessário para provedores de serviços que usam Windows métodos do SDK de formato de mídia.                                                                                                                                                                                      |
| WMVCORE. lib                      | nenhum                                                                          | exigido por provedores de serviço que usam Windows funções ou objetos do Media Format SDK.                                                                                                                                                                          |
| Mmreg. h                          | Nenhum (cabeçalho SDK da plataforma)                                                    | exigido pelos provedores de serviço que fazem referência a várias definições de formato de mídia padrão Windows, como **WAVEFORMATEX**.                                                                                                                                      |
| MtpExt. h                         | nenhum                                                                          | Necessário para provedores de serviços que manipulam [**IMDSPDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) em dispositivos MTP. Define várias constantes e estruturas padrão do MTP.                                                                        |
| Chave. c                            | nenhum                                                                          | Define uma chave e um certificado da Microsoft. a versão fornecida com o SDK inclui uma chave fictícia de teste que permitirá o uso de arquivos de mídia de Windows não protegidos por DRM.                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 





