---
title: Uso de conteúdo de medição
description: Uso de conteúdo de medição
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Gerenciador de Dispositivos de mídia do Windows, uso de conteúdo de medição
- Gerenciador de Dispositivos, uso de conteúdo de medição
- Guia de programação, medição do uso de conteúdo
- aplicativos de área de trabalho, medição do uso de conteúdo
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, medição do uso de conteúdo
- uso de conteúdo de medição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649eee810e7bbdbc2ea93a32c6368ec345fa7364
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105794534"
---
# <a name="metering-content-usage"></a>Uso de conteúdo de medição

Com a tecnologia Windows Media 10, agora você pode medir o uso de conteúdo em um dispositivo portátil. Se uma licença do Windows Media 10 permitir a medição, o dispositivo poderá armazenar a contagem de execuções de músicas e carregar o uso de volta para o emissor da licença pela Internet. Esse sistema permite que os provedores de conteúdo ajustem suas tarifas de royalty ao medir com precisão o uso do conteúdo.

Para medir o conteúdo, o aplicativo deve ter um certificado de medição fornecido por um serviço de licenciamento criado no SDK do Windows Media Rights Manager 10. Somente o conteúdo licenciado por esse mesmo serviço pode ser medido. Para obter mais informações sobre como funciona a medição e como criar um serviço de medição de licença, consulte a [documentação do SDK do Windows Media Rights Manager](/previous-versions/ms986509(v=msdn.10)) no msdn. O SDK pode ser adquirido preenchendo as informações necessárias na [página de licenciamento do Windows Media](https://www.microsoft.com/licensing/default).

Um aplicativo pode ter medição incorporada a ele, ou você pode criar um plug-in COM para um aplicativo existente, como o Windows Media Player, se o aplicativo aceitar plug-ins de medição.

Um aplicativo deve avisar os usuários se o uso do conteúdo for medido. Para obter mais informações, consulte as páginas da Web da Microsoft listadas na [política de privacidade](privacy-statement.md).

A aquisição de dados de medição de um dispositivo pode ser lenta. Portanto, se um aplicativo for de uso, ele deve fazer isso com frequência para evitar que grandes quantidades de dados sejam acumuladas no dispositivo e reduzindo a transferência de dados. Para evitar transferências de dados que seriam muito lentas, os fabricantes de dispositivos podem enviar subconjuntos de dados de medição disponíveis. O aplicativo deve monitorar os sinalizadores recuperados por [**IWMDRMDeviceApp::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md) para ver se mais dados de medição permanecem no dispositivo.

As etapas a seguir mostram como um aplicativo pode medir o uso de conteúdo.

1.  Como a medição só está disponível em dispositivos que dão suporte ao Windows Media DRM 10 para dispositivos portáteis, seu aplicativo deve, em algum momento, chamar **QueryDeviceStatus**, conforme descrito em [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md), para garantir que o dispositivo seja válido e atualizado.
2.  Solicite informações de medição do dispositivo chamando [**IWMDRMDeviceApp:: GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Envie os dados de medição recuperados para o serviço de medição na URL recuperada por **GenerateMeterChallenge**. O formato dos dados enviados ao serviço depende do script nesse serviço em particular. Por exemplo, alguns serviços podem exigir os dados enviados como um comando POST como um par de nome/valor. O provedor de serviços deve permitir que você conheça seus requisitos de formatação específicos.
4.  Obtenha uma resposta do serviço de medição e envie-a para o dispositivo chamando [**IWMDRMDeviceApp::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md). Isso faz com que o dispositivo redefina as contagens de reprodução e também retorna um valor que indica se há mais dados de medição no dispositivo que devem ser recuperados chamando **GenerateMeterChallenge** novamente.

Para obter informações abrangentes e exemplos de código para medição, consulte o [site do Windows Media](/previous-versions//bb614723(v=vs.85)).

 

 