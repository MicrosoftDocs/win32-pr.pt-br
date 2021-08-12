---
description: A interface IWiaPropertyStorage fornece métodos para ler e escrever as propriedades de um item WIA (Aquisição de Imagem de Windows). As propriedades do item incluem comandos de dispositivo, informações de formato de item e informações do dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lendo e configurando propriedades do WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e319723023a00c4159687c3dff13fedab8275a0522fdb2254b36b8e62edb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439870"
---
# <a name="reading-and-setting-wia-properties"></a>Lendo e configurando propriedades do WIA

A interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fornece métodos para ler e escrever as propriedades de um item WIA (Aquisição de Imagem de Windows). As propriedades do item incluem comandos de dispositivo, informações de formato de item e informações do dispositivo.

Um aplicativo pode obter um ponteiro para uma interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de um item enumerando as informações do dispositivo ou informações de evento do item chamando [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ou consultando a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) do item. (No WIA 2.0, faça isso chamando [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) ou [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) ou consultando a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item.)

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) herda de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e os métodos herdados são implementados conforme descrito na seção de referência do Structured Armazenamento no SDK (Software Development Kit) do Windows.

> [!Note]
>
> Os aplicativos WIA sempre devem ler os headers de dados de imagem para obter informações precisas sobre a imagem. O driver WIA pode alterar as propriedades do WIA e os headers de dados de imagem durante a transferência de dados.
>
> Se não houver nenhum header de dados de imagem fornecido com o formato especificado, o aplicativo WIA deverá usar as propriedades wia como uma fonte de informações sobre a transferência de dados. O aplicativo WIA deve ler as propriedades wia necessárias após a conclusão da verificação ou captura para obter as configurações atualizadas.

 

As seções a seguir descrevem as várias propriedades do WIA:

-   [Validação da propriedade WIA](-wia-wia-property-validation.md)
-   [Propriedades de informações do dispositivo](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Propriedades do Dispositivo](-wia-device-properties.md)
-   [Propriedades do item](-wia-item-properties.md)
-   [Propriedades wia adicionais](-wia-additional-wia-properties.md)
-   [Definindo propriedades personalizadas](-wia-defining-custom-properties.md)
-   [Usando propriedades personalizadas](-wia-using-custom-properties.md)
-   [Esquema de perfil de verificação](-wia-scan-profile-schema.md)

 

 
