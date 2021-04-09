---
title: Arquivos de biblioteca e de cabeçalho necessários para um aplicativo
description: Arquivos de biblioteca e de cabeçalho necessários para um aplicativo
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Gerenciador de Dispositivos de mídia do Windows, bibliotecas
- Gerenciador de Dispositivos, bibliotecas
- Guia de programação, bibliotecas
- aplicativos de área de trabalho, bibliotecas
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, bibliotecas
- bibliotecas
- Windows Media Gerenciador de Dispositivos, arquivos de cabeçalho
- Gerenciador de Dispositivos, arquivos de cabeçalho
- Guia de programação, arquivos de cabeçalho
- aplicativos de área de trabalho, arquivos de cabeçalho
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, arquivos de cabeçalho
- arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a8a04ee6c3fe603d52139e83f81a49d78dc45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005647"
---
# <a name="required-library-and-header-files-for-an-application"></a>Arquivos de biblioteca e de cabeçalho necessários para um aplicativo

Esta seção lista as bibliotecas, os arquivos de cabeçalho ou os arquivos IDL que você precisará incluir para desenvolver um aplicativo de Gerenciador de Dispositivos de mídia do Windows ou um plug-in. Conforme mencionado na [compilação dos arquivos IDL fornecidos com o SDK](compiling-the-idl-files-supplied-with-the-sdk.md), o SDK inclui arquivos IDL e arquivos de cabeçalho predefinidos, e seu aplicativo pode usar qualquer um deles. (Observe que alguns arquivos de cabeçalho não têm arquivos IDL correspondentes e você não pode criá-los por conta própria.) Se você estiver criando seus próprios arquivos IDL, inclua as dependências listadas em compilando os arquivos IDL fornecidos com o SDK.

Nem todos os aplicativos precisarão de todos os arquivos; Leia a descrição para saber se seu aplicativo requer um arquivo.



| Cabeçalho ou biblioteca predefinida       | IDL equivalente                                | Descrição                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | nenhum                                          | Exigido por todos os aplicativos. Contém os objetos do Windows Media Gerenciador de Dispositivos.                                                                                                                                                                              |
| WMVCORE. lib                      | nenhum                                          | Exigido por aplicativos que usam funções ou objetos do Windows Media Format SDK.                                                                                                                                                                          |
| Initguid. h                       | Nenhum (cabeçalho SDK da plataforma)                    | Exigido por todos os aplicativos para definir os valores de **GUID** usando o arquivo predefinido Mswmdm. h. Você deve incluir Initguid. h apenas uma vez no seu projeto. Esse cabeçalho redefine a macro **definir \_ GUID** para evitar problemas de nomenclatura de **GUID** externo. |
| Mmreg. h                          | Nenhum (cabeçalho SDK da plataforma)                    | Exigido por aplicativos que fazem referência a várias definições padrão de formato de mídia do Windows, como **WAVEFORMATEX**.                                                                                                                                      |
| mswmdm. h                         | WMDM. idlicomponentauthenticate. idl<br/> | Exigido por todos os aplicativos. Define todas as interfaces de aplicativo, bem como estruturas, metadados, erros e outras constantes.                                                                                                                        |
| SAC. h                            | nenhum                                          | Exigido por todos os aplicativos. Define os protocolos SAC.                                                                                                                                                                                                      |
| scclient. h                       | nenhum                                          | Exigido por todos os aplicativos. Declara a classe [CSecureChannelClient](csecurechannelclient-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                   | Exigido por aplicativos que usam a interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| wmdrmdeviceapp. h                 | WMDRMDeviceApp. idl                            | Exigido por aplicativos ou plug-ins que atualizam os componentes DRM ou as contagens de planos de execução em dispositivos.                                                                                                                                                          |
| WMSDK. h                          | Nenhum (fornecido pelo SDK do Windows Media Format)   | Necessário para aplicativos que usam os métodos do SDK do Windows Media Format.                                                                                                                                                                                      |
| MtpExt. h                         | nenhum                                          | Necessário para aplicativos que chamam [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) em dispositivos MTP. Define várias constantes e estruturas padrão do MTP.                                                                          |
| Chave. c                            | nenhum                                          | Define uma chave e um certificado da Microsoft. A versão fornecida com o SDK inclui uma chave fictícia de teste que permitirá o uso de arquivos de mídia do Windows não protegidos por DRM.                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 





