---
description: A interface IWiaPropertyStorage fornece métodos para ler e gravar as propriedades de um item de aquisição de imagem do Windows (WIA). As propriedades do item incluem comandos de dispositivo, informações de formato de item e informações de dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lendo e definindo propriedades WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090497"
---
# <a name="reading-and-setting-wia-properties"></a>Lendo e definindo propriedades WIA

A interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fornece métodos para ler e gravar as propriedades de um item de aquisição de imagem do Windows (WIA). As propriedades do item incluem comandos de dispositivo, informações de formato de item e informações de dispositivo.

Um aplicativo pode obter um ponteiro para uma interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de um item enumerando as informações do dispositivo ou informações de evento do item chamando [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ou consultando a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) do item. (No WIA 2,0, faça isso chamando [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) ou [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) ou consultando a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item.)

O [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) herda de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e os métodos herdados são implementados conforme descrito na seção de referência de armazenamento estruturado no SDK (Software Development Kit) do Windows.

> [!Note]
>
> Os aplicativos WIA sempre devem ler cabeçalhos de dados de imagem para obter informações precisas sobre a imagem. O driver WIA pode alterar as propriedades de WIA e os cabeçalhos de dados de imagem durante a transferência de dados.
>
> Se não houver nenhum cabeçalho de dados de imagem fornecido com o formato especificado, o aplicativo WIA deverá usar as propriedades WIA como uma fonte de informações sobre a transferência de dados. O aplicativo WIA deve ler novamente as propriedades de WIA necessárias depois que a verificação ou captura for concluída para obter as configurações atualizadas.

 

As seções a seguir descrevem as várias propriedades de WIA:

-   [Validação da propriedade WIA](-wia-wia-property-validation.md)
-   [Propriedades de informações do dispositivo](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Propriedades do Dispositivo](-wia-device-properties.md)
-   [Propriedades do item](-wia-item-properties.md)
-   [Propriedades de WIA adicionais](-wia-additional-wia-properties.md)
-   [Definindo propriedades personalizadas](-wia-defining-custom-properties.md)
-   [Usando propriedades personalizadas](-wia-using-custom-properties.md)
-   [Esquema do perfil de verificação](-wia-scan-profile-schema.md)

 

 
