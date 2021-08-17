---
title: Medição do uso de conteúdo
description: Medição do uso de conteúdo
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Mídia Gerenciador de Dispositivos, medição de uso de conteúdo
- Gerenciador de Dispositivos, medição de uso de conteúdo
- guia de programação, uso de conteúdo de medição
- aplicativos da área de trabalho, medição de uso de conteúdo
- criando Windows mídia Gerenciador de Dispositivos aplicativos, medição do uso de conteúdo
- uso de conteúdo de medição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029bae2bcdd69f9dc58c4a64317f974538c672b1d27597fbdc1915074aff0278
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957196"
---
# <a name="metering-content-usage"></a>Medição do uso de conteúdo

Com Windows de Mídia 10, agora você pode medição do uso de conteúdo em um dispositivo portátil. Se uma licença Windows Mídia 10 permitir medição, o dispositivo poderá armazenar a contagem de reprodução para músicas e carregar o uso de volta para o emissor da licença pela Internet. Esse sistema permite que os provedores de conteúdo ajustem seus valores de royalties medindo com precisão o uso de conteúdo.

Para medição de conteúdo, o aplicativo deve ter um certificado de medição fornecido por um serviço de licenciamento criado no SDK Windows Media Rights Manager 10. Somente o conteúdo licenciado por esse mesmo serviço pode ser monitorado. Para obter mais informações sobre como funciona a medição e como criar um serviço de medição de licença, consulte a documentação do [SDK](/previous-versions/ms986509(v=msdn.10)) do Windows Media Rights Manager no MSDN. O SDK pode ser adquirido preenchendo as informações necessárias na página [Windows Licenciamento de Mídia.](https://www.microsoft.com/licensing/default)

Um aplicativo pode ter medição própria ou você pode criar um plug-in COM para um aplicativo existente, como o Windows Media Player, se o aplicativo aceitar plug-ins de medição.

Um aplicativo deve avisar os usuários se o uso de conteúdo será monitorado. Para obter mais informações, consulte as páginas da Web da Microsoft listadas na Política [de Privacidade](privacy-statement.md).

A aquisição de dados de medição de um dispositivo pode ser lenta. Portanto, se um aplicativo monitora o uso, ele deve fazer isso com frequência para impedir que grandes quantidades de dados se acumulem no dispositivo e reduzam a transferência de dados. Para evitar transferências de dados que seriam muito lentas, os fabricantes de dispositivos podem enviar subconjunto de dados de medição disponíveis. O aplicativo deve monitorar os sinalizadores recuperados por [**IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md) para ver se mais dados de medição permanecem no dispositivo.

As etapas a seguir mostram como um aplicativo pode medição do uso de conteúdo.

1.  Como a medição só está disponível em dispositivos que são compatíveis com o Windows DRM de Mídia 10 para Dispositivos Portáteis, seu aplicativo deve, em algum momento, chamar **QueryDeviceStatus**, conforme descrito em Manipulando conteúdo protegido no [aplicativo,](handling-protected-content-in-the-application.md)para garantir que o dispositivo seja válido e atualizado.
2.  Solicite informações de medição do dispositivo chamando [**IWMDRMDeviceApp::GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Envie os dados de medição recuperados para o serviço de medição na URL recuperada por **GenerateMeterChallenge**. O formato dos dados enviados ao serviço depende do script desse serviço específico. Por exemplo, alguns serviços podem exigir os dados enviados como um comando POST como um par nome/valor. O provedor de serviços deve permitir que você conheça seus requisitos de formatação específicos.
4.  Receba uma resposta do serviço de medição e envie-a para o dispositivo chamando [**IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md). Isso faz com que o dispositivo redefinir contagens de reprodução e também retorna um valor que indica se existem mais dados de medição no dispositivo que devem ser recuperados chamando **GenerateMeterChallenge** novamente.

Para obter informações abrangentes e código de exemplo para medição, [consulte o site Windows Media](/previous-versions//bb614723(v=vs.85)).

 

 