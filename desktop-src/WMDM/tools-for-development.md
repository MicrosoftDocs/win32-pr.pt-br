---
title: Ferramentas para desenvolvimento
description: Ferramentas para desenvolvimento
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Mídia Gerenciador de Dispositivos, ferramentas de desenvolvimento
- Gerenciador de Dispositivos,ferramentas de desenvolvimento
- Windows Mídia Gerenciador de Dispositivos, certificados
- Gerenciador de Dispositivos, certificados
- Windows Mídia Gerenciador de Dispositivos, chaves
- Gerenciador de Dispositivos, chaves
- Windows Bibliotecas Gerenciador de Dispositivos mídia
- Gerenciador de Dispositivos, bibliotecas
- Windows SDK (kit Gerenciador de Dispositivos de mídia), software development kit (SDK)
- Gerenciador de Dispositivos,SDK (software development kit)
- Windows SDK Gerenciador de Dispositivos mídia
- SDK do Gerenciador de Dispositivos
- Windows Media Player Sdk
- Windows SDK de formato de mídia
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e517a97246c2bf9b2ac5670a7cf696e714777a2f5926a37e1b2d37ecbe45c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031606"
---
# <a name="tools-for-development"></a>Ferramentas para desenvolvimento

Esta seção descreve os vários certificados e chaves, bibliotecas e SDKs que você precisará programar usando o SDK Windows Media Gerenciador de Dispositivos.

Certificados e chaves

O SDK do Gerenciador de Dispositivos Media Windows é emitido com um par de certificados/chaves de teste (no arquivo key.c) que pode ser usado por um aplicativo ou provedor de serviços para usar métodos Gerenciador de Dispositivos media Windows em conteúdo desprotegido. Esse par de chave/certificado permite que o aplicativo ou provedor de serviços use a maioria das funcionalidades Windows mídia Gerenciador de Dispositivos mídia.

No entanto, para desenvolver um aplicativo ou provedor de serviços que possa lidar com conteúdo protegido por DRM, você deve solicitar um ou mais certificados (cada um com uma chave) da Página de Licenciamento de Mídia do [Windows](https://www.microsoft.com/licensing/default). Os certificados são necessários para os seguintes aplicativos ou objetos:

-   Provedores de serviços que lidam com conteúdo protegido por DRM exigem um certificado Windows de provedor de serviços Gerenciador de Dispositivos mídia (e chave)
-   Aplicativos que transferem conteúdo protegido por DRM exigem Windows mídia Gerenciador de Dispositivos Transferir Certificado (e chave)
-   Aplicativos que reproduzem conteúdo protegido por DRM exigem um Certificado DRM (e uma chave).
-   Os componentes de medição de licença exigem um certificado de medição. Isso é fornecido por um serviço de medição de licença criado no SDK do Windows Media Rights Manager, que pode ser solicitado na página Windows licenciamento de mídia.

Bibliotecas e cabeçalhos

Além das bibliotecas e dos [](required-library-and-header-files-for-an-application.md) títulos mencionados em Arquivos necessários de biblioteca e de título para um aplicativo ou bibliotecas e títulos necessários para um provedor de [serviços,](required-libraries-and-headers-for-a-service-provider.md)qualquer aplicativo ou plug-in que anteriormente vinculado a WMDRMSDK.lib para chamar funções do SDK de Formato de Mídia do Windows agora deve vincular a WMDRMSDKStub.Lib. Esse arquivo de biblioteca é usado para acessar arquivos protegidos por DRM. Você também pode solicitar essa biblioteca na página Windows licenciamento de mídia.

SDKs relacionados

Os SDKs da Microsoft a seguir fornecem elementos que podem ser necessários na criação de soluções para dispositivos de mídia portáteis.



| SDK obrigatório                     | Necessário para...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows SDK Gerenciador de Dispositivos mídia | Aplicativos de player de mídia da área de trabalho que se comunicam com dispositivos portáteis<br/> Aplicativos da área de trabalho que podem trocar arquivos ou informações com dispositivos portáteis<br/> Windows Media Player objetos COM de medição<br/> |
| Windows Media Player Sdk         | Windows Media Player plug-ins<br/> Windows Media Player objetos COM de medição<br/> Windows Media Player capas<br/>                                                                                                   |
| Windows SDK de formato de mídia         | Players de áudio ou vídeo que podem criar ou reproduzir arquivos (especialmente arquivos ASF)<br/> Aplicativos de edição de áudio ou vídeo<br/>                                                                                               |
| Windows Media Rights Manager SDK | Aplicativos ou plug-ins que a reprodução do medidor conta na área de trabalho ou no dispositivo.                                                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Ponto de Partida**](getting-started.md)
</dt> </dl>

 

 





