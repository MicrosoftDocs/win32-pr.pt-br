---
description: Este tópico descreve como gravar um manipulador de propriedades de shell personalizado para uma fonte de mídia Microsoft Media Foundation.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Provedores de metadados personalizados para arquivos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1951fd90265299cb53369d521193740b7d4d05e0f1650583965eb670ab375cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777596"
---
# <a name="custom-metadata-providers-for-media-files"></a>Provedores de metadados personalizados para arquivos de mídia

Este tópico descreve como gravar um manipulador de propriedades de shell personalizado para uma fonte de mídia Microsoft Media Foundation.

> [!Note]  
> Para obter informações básicas sobre provedores de metadados no Media Foundation, consulte [metadados de mídia](media-metadata.md). Este tópico discute os manipuladores de propriedades do Shell; Ele não descreve a interface de metadados da versão 1, [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata).

 

Os metadados estão fortemente ligados ao formato do arquivo. No Media Foundation, os formatos de arquivo são representados por fontes de mídia. Se você quiser dar suporte a metadados para um formato sem suporte nativo no Media Foundation, deverá implementar uma fonte de mídia personalizada com um manipulador de propriedades. O manipulador de propriedades permite que o sistema de propriedades do Shell Leia e grave metadados com eficiência.

Um manipulador de propriedades é um objeto COM que implementa as seguintes interfaces:

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Opcionalmente, ele também pode expor a seguinte interface:

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Se o sistema de propriedades do Shell precisar obter metadados para um arquivo, ele chamará [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o manipulador de propriedades e, em seguida, chamará os métodos de leitura e gravação apropriados na interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

O pipeline de Media Foundation usa um mecanismo ligeiramente diferente, porque o pipeline Obtém o manipulador de propriedade diretamente da origem da mídia. Em vez de chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o manipulador de propriedades, o pipeline chama [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na origem da mídia, conforme descrito no tópico [provedores de metadados do Shell](shell-metadata-providers.md).

Para criar um manipulador de propriedade personalizada, faça o seguinte:

-   Implemente a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para expor [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore). O GUID do serviço é o **\_ serviço de \_ manipulador \_ de propriedades MF**.
-   Se a origem da mídia for usada remotamente, ela também deverá expor a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) por meio do método **QueryInterface** da origem de mídia, além de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice).
-   Para disponibilizar o manipulador de propriedades para o sistema de propriedades do Shell, registre a DLL para o manipulador de propriedades, conforme descrito em [registrando e distribuindo manipuladores de propriedade](../properties/prophand-reg-dist.md).
-   A origem da mídia é registrada separadamente, conforme descrito em [manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

### <a name="implementation-tips"></a>Dicas de implementação

Para obter uma lista de chaves de propriedade de metadados, consulte [Propriedades de metadados para arquivos de mídia](metadata-properties-for-media-files.md).

Manipuladores de propriedade devem ser rápidos; Eles devem fornecer acesso eficiente de leitura e gravação aos metadados. (Considere que o Shell pode recuperar metadados de centenas de arquivos.) Portanto, não chame [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) de seu manipulador de propriedade. A função **MFStartup** introduz a latência de inicialização, pois ela cria vários threads de fila de trabalho e aloca memória global.

Em uma implementação típica, o manipulador de propriedades e a origem da mídia compartilharão alguns dos mesmos códigos de análise. No entanto, uma origem de mídia usa chamadas [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) assíncronas para e/s, enquanto o manipulador de propriedades usa a interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Media Foundation fornece um objeto auxiliar que encapsula um fluxo baseado em **IStream** e o expõe como um fluxo **IMFByteStream** . Para criar o wrapper, chame [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream).

Ao atualizar metadados, é recomendável gravar os dados diretamente no fluxo original. Essa recomendação é diferente do comportamento de *Copiar na gravação* da maioria dos manipuladores de propriedade, em que uma cópia dos dados é modificada. Os arquivos de mídia podem ser muito grandes, portanto, a cópia em gravação normalmente é muito lenta para uma implementação eficiente. Para desabilitar a cópia em gravação, defina a configuração do registro **ManualSafeSave** , conforme descrito em [registrando e distribuindo manipuladores de propriedade](../properties/prophand-reg-dist.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Metadados de mídia](media-metadata.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Gravando uma fonte de mídia personalizada](writing-a-custom-media-source.md)
</dt> </dl>

 

 
