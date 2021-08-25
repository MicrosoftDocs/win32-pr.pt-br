---
title: Arquivos de biblioteca e de header necessários para um aplicativo
description: Arquivos de biblioteca e de header necessários para um aplicativo
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Bibliotecas Gerenciador de Dispositivos mídia
- Gerenciador de Dispositivos, bibliotecas
- guia de programação, bibliotecas
- aplicativos da área de trabalho, bibliotecas
- criando Windows aplicativos de Gerenciador de Dispositivos mídia, bibliotecas
- bibliotecas
- Windows Arquivos Gerenciador de Dispositivos mídia, arquivos de header
- Gerenciador de Dispositivos, arquivos de header
- guia de programação, arquivos de header
- aplicativos da área de trabalho, arquivos de header
- criando Windows mídia Gerenciador de Dispositivos aplicativos, arquivos de header
- arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b6630f4ff752b53ed69633d1e63a62093e4a4fbd16f65ccb1cc709aae120a07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863066"
---
# <a name="required-library-and-header-files-for-an-application"></a>Arquivos de biblioteca e de header necessários para um aplicativo

Esta seção lista as bibliotecas, arquivos de header ou arquivos IDL que você precisará incluir para desenvolver um aplicativo ou plug-in Windows Media Gerenciador de Dispositivos. Conforme mencionado em Compilando os arquivos IDL fornecidos com o SDK , o [SDK](compiling-the-idl-files-supplied-with-the-sdk.md)inclui arquivos IDL e arquivos de header pré-compilados, e seu aplicativo pode usar qualquer um deles. (Observe que alguns arquivos de header não têm arquivos IDL correspondentes e você não pode criar eles por conta própria.) Se estiver criando seus próprios arquivos IDL, inclua as dependências listadas em Compilando os arquivos IDL fornecidos com o SDK.

Nem todos os aplicativos exigirão todos os arquivos; leia a descrição para saber se seu aplicativo requer um arquivo.



| Biblioteca ou header pré-construído       | IDL equivalente                                | Descrição                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp.lib                     | nenhum                                          | Exigido por todos os aplicativos. Contém Windows mídia Gerenciador de Dispositivos objetos.                                                                                                                                                                              |
| wmvcore.lib                      | nenhum                                          | Exigido por aplicativos que usam Windows objetos ou funções do SDK de Formato de Mídia.                                                                                                                                                                          |
| initguid.h                       | none (header do SDK da Plataforma)                    | Exigido por todos os aplicativos para definir **os valores guid** usando o arquivo Mswmdm.h pré-construído. Você deve incluir initguid.h uma vez e apenas uma vez em seu projeto. Esse header redefine a macro **DEFINE \_ GUID** para evitar problemas externos de nomeação de **GUID.** |
| mmreg.h                          | none (header do SDK da Plataforma)                    | Exigido por aplicativos que referenciam várias definições Windows formato de mídia padrão, como **WAVEFORMATEX.**                                                                                                                                      |
| mswmdm.h                         | WMDM.idlicomponentauthenticate.idl<br/> | Exigido por todos os aplicativos. Define todas as interfaces do aplicativo, bem como estruturas, metadados, erro e outras constantes.                                                                                                                        |
| sac.h                            | nenhum                                          | Exigido por todos os aplicativos. Define protocolos SAC.                                                                                                                                                                                                      |
| scclient.h                       | nenhum                                          | Exigido por todos os aplicativos. Declara a [classe CSecureChannelClient.](csecurechannelclient-class.md)                                                                                                                                                  |
| wmdmlog.hwmdmlog \_ i.c<br/> | Wmdmlog.idl                                   | Exigido por aplicativos que usam a interface [**IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                       |
| wmdrmdeviceapp.h                 | WMDRMDeviceApp.idl                            | Exigido por aplicativos ou plug-ins que atualizem componentes DRM ou contagens de reprodução de medidor em dispositivos.                                                                                                                                                          |
| wmsdk.h                          | none (fornecido pelo Windows SDK de Formato de Mídia)   | Necessário para aplicativos que usam Windows SDK de Formato de Mídia.                                                                                                                                                                                      |
| MtpExt.h                         | nenhum                                          | Necessário para aplicativos que chamam [**IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) em dispositivos MTP. Define várias constantes e estruturas MTP padrão.                                                                          |
| Key.c                            | nenhum                                          | Define uma chave e um certificado da Microsoft. A versão enviada com o SDK inclui uma chave fiada de teste que permitirá o uso de arquivos de mídia não Windows DRM.                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 





