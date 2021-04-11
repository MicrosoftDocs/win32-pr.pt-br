---
title: Acessando metadados e atributos no aplicativo
description: Obtendo e configurando metadados e atributos no aplicativo
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Gerenciador de Dispositivos de mídia do Windows, metadados
- Gerenciador de Dispositivos, metadados
- Guia de programação, metadados
- aplicativos de área de trabalho, metadados
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, metadados
- metadata
- Gerenciador de Dispositivos de mídia do Windows, atributos
- Gerenciador de Dispositivos, atributos
- Guia de programação, atributos
- aplicativos de área de trabalho, atributos
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, atributos
- Atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104293630"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>Acessando metadados e atributos no aplicativo

Uma discussão geral de metadados e atributos está disponível para [obter e definir metadados e atributos](getting-and-setting-metadata-and-attributes.md). Esta seção aborda chamadas de método de aplicativo específicas para recuperar ou definir valores.

Os aplicativos podem recuperar atributos ou metadados sobre um armazenamento específico chamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata). **GetMetadata** recupera uma coleção completa de todos os metadados associados a um armazenamento, e o aplicativo pode enumerar por todos os valores ou solicitar valores específicos da coleção. **GetSpecifiedMetadata** cria um objeto de metadados em nome do chamador. O chamador pode solicitar um subconjunto dos dados disponíveis preenchendo o parâmetro *ppwszPropNames* com uma matriz das cadeias de caracteres de propriedades do Windows Media Gerenciador de dispositivos desejadas e a contagem dessa matriz. O objeto de metadados retornado será preenchido com as propriedades que poderiam ser recuperadas. As propriedades que não puderam ser recuperadas estarão ausentes. Os metadados são retornados em uma base de melhor esforço.

Um dispositivo pode definir atributos ou metadados em um armazenamento chamando [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)ou [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata). Observe que não há nenhuma garantia de que os valores definidos serão persistidos, pois eles podem ser armazenados em um repositório de arquivos externo não persistente, os valores podem não ter suporte ou o dispositivo pode não dar suporte às propriedades como graváveis.

Você também pode obter ou definir metadados sobre um dispositivo chamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) ou [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty). Há uma tabela separada de constantes de metadados de dispositivo listadas no final das [constantes de metadados](metadata-constants.md).

Exemplos de como usar esses métodos são fornecidos na documentação de referência de cada método.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Obtendo e configurando metadados e atributos**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




