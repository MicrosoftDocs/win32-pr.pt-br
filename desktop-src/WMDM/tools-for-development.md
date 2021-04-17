---
title: Ferramentas para desenvolvimento
description: Ferramentas para desenvolvimento
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Gerenciador de Dispositivos, ferramentas de desenvolvimento
- Gerenciador de Dispositivos, ferramentas de desenvolvimento
- Gerenciador de Dispositivos de mídia do Windows, certificados
- Gerenciador de Dispositivos, certificados
- Gerenciador de Dispositivos de mídia do Windows, chaves
- Gerenciador de Dispositivos, chaves
- Gerenciador de Dispositivos de mídia do Windows, bibliotecas
- Gerenciador de Dispositivos, bibliotecas
- Windows Media Gerenciador de Dispositivos, Software Development Kit (SDK)
- Gerenciador de Dispositivos, Software Development Kit (SDK)
- SDK do Windows Media Gerenciador de Dispositivos
- SDK do Gerenciador de Dispositivos
- SDK do Windows Media Player
- SDK do Windows Media Format
- SDK do Windows Media Rights Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105811361"
---
# <a name="tools-for-development"></a>Ferramentas para desenvolvimento

Esta seção descreve os vários certificados e chaves, bibliotecas e SDKs que você precisará programar usando o SDK do Windows Media Gerenciador de Dispositivos.

Certificados e chaves

O SDK do Windows Media Gerenciador de Dispositivos é fornecido com um par de chave/certificado de teste (no arquivo Key. c) que pode ser usado por um aplicativo ou um provedor de serviços para usar os métodos do Windows Media Gerenciador de Dispositivos em conteúdo desprotegido. Esse par de chave/certificado permite que o aplicativo ou provedor de serviços use a maior parte da funcionalidade do Windows Media Gerenciador de Dispositivos.

No entanto, para desenvolver um aplicativo ou provedor de serviços que possa lidar com conteúdo protegido por DRM, você deve solicitar um ou mais certificados (cada um com uma chave) na [página de licenciamento do Windows Media](https://www.microsoft.com/licensing/default). Os certificados são necessários para os seguintes aplicativos ou objetos:

-   Provedores de serviço que manipulam conteúdo protegido por DRM exigem um certificado (e chave) do provedor de serviços do Windows Media Gerenciador de Dispositivos
-   Os aplicativos que transferem conteúdo protegido por DRM exigem um certificado (e chave) de transferência do Windows Media Gerenciador de Dispositivos
-   Os aplicativos que executam conteúdo protegido por DRM exigem um certificado DRM (e chave).
-   Os componentes de medição de licença exigem um certificado de medição. Isso é fornecido por um serviço de medição de licença criado no SDK do Windows Media Rights Manager, que pode ser solicitado na página de licenciamento do Windows Media.

Bibliotecas e cabeçalhos

Além das bibliotecas e dos cabeçalhos mencionados nos [arquivos de biblioteca e de cabeçalho necessários para um aplicativo](required-library-and-header-files-for-an-application.md) ou [bibliotecas e cabeçalhos necessários para um provedor de serviços](required-libraries-and-headers-for-a-service-provider.md), qualquer aplicativo ou plug-in que tenha sido vinculado anteriormente a WMDRMSDK. lib para chamar as funções do Windows Media Format SDK agora deve vincular a WMDRMSDKStub. lib. Esse arquivo de biblioteca é usado para acessar arquivos protegidos por DRM. Você também pode solicitar essa biblioteca na página de licenciamento do Windows Media.

SDKs relacionados

Os SDKs da Microsoft a seguir fornecem elementos que podem ser necessários na criação de soluções para dispositivos de mídia portáteis.



| SDK necessário                     | Necessário para...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SDK do Windows Media Gerenciador de Dispositivos | Aplicativos de player de mídia de desktop que se comunicam com dispositivos portáteis<br/> Aplicativos de área de trabalho que podem trocar arquivos ou informações com dispositivos portáteis<br/> Objetos COM de medição do Windows Media Player<br/> |
| SDK do Windows Media Player         | Plug-ins do Windows Media Player<br/> Objetos COM de medição do Windows Media Player<br/> Capas do Windows Media Player<br/>                                                                                                   |
| SDK do Windows Media Format         | Players de áudio ou vídeo que podem criar ou reproduzir arquivos (particularmente arquivos ASF)<br/> Aplicativos de edição de áudio ou vídeo<br/>                                                                                               |
| SDK do Windows Media Rights Manager | Aplicativos ou plug-ins que o medidor de execução conta no desktop ou dispositivo.                                                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](getting-started.md)
</dt> </dl>

 

 





