---
description: O modelo conceitual
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: O modelo conceitual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a653d3658e0785fcc729be335fc4d648ea9bc91af676678aece0c43ce046f419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806538"
---
# <a name="the-conceptual-model"></a>O modelo conceitual

Esta seção descreve os objetos, as propriedades e os recursos que constituem o modelo conceitual WPD.

### <a name="objects"></a>Objetos

No WPD, entidades lógicas em dispositivos são conhecidas como objetos. Normalmente, mas nem sempre, eles representam dados no dispositivo. Os objetos têm propriedades e são referenciados por identificadores de objeto. Exemplos de objetos incluem imagens e pastas em uma câmera, músicas e playlists em um player de mídia, contatos em um telefone celular e assim por diante.

Os objetos também podem representar partes funcionais ou informacionais do dispositivo. Exemplos disso incluem controles de player (reprodução/registro/pausa), configurações de câmera, recursos de SMS de um telefone celular e assim por diante.

Os dois tópicos a seguir dão exemplos e ilustrações de dois tipos de objetos: o objeto Image e o objeto Mediacast.

### <a name="image-object"></a>Objeto Image

Um objeto de imagem representa uma imagem ainda. O diagrama a seguir mostra as relações entre um objeto Image, suas propriedades e seus recursos.

![diagrama mostrando um objeto wpd e sua relação com suas propriedades e recursos](images/wpd-overview-figure2.gif)

Para obter mais informações sobre o objeto Image e suas propriedades, consulte o [**tópico WPD \_ CONTENT TYPE \_ \_ IMAGE.**](wpd-content-type-image.md)

### <a name="mediacast-object"></a>Objeto Mediacast

Um objeto Mediacast pode ser pensado como um objeto de contêiner que grupos de conteúdo relacionado, assim como uma música de grupos de playlists. Geralmente, um objeto Mediacast é usado para agrupar o conteúdo de mídia que foi publicado online. Por exemplo, um canal RSS pode ser representado como um objeto Mediacast cujas referências de objeto apontam para objetos de conteúdo que representam cada item no canal. O diagrama a seguir mostra a relação entre um objeto Mediacast e os três objetos de áudio que ele contém.

![diagrama mostrando a estrutura hierárquica de um objeto de cada vez e três objetos que ele contém](images/mediacast1.gif)

As referências ao objeto de áudio são especificadas na propriedade [WPD \_ OBJECT \_ REFERENCES](object-properties.md) para o objeto Mediacast. Para obter mais informações sobre as propriedades com suporte de um objeto Mediacast, consulte o [**tópico WPD \_ CONTENT TYPE \_ MEDIA \_ \_ CAST.**](wpd-content-type-media-cast.md)

### <a name="properties"></a>Propriedades

As propriedades do objeto fornecem um mecanismo para trocar metadados que descrevem o objeto. Por exemplo, um objeto de imagem pode incluir propriedades que descrevem seu nome de arquivo, tamanho, formato, largura em pixels e assim por diante.

As propriedades têm um valor atual, bem como atributos. WPD define um conjunto de propriedades padrão que comem as definições de API e DDI. Os fornecedores não estão limitados às propriedades predefinidos do WPD e são livres para adicionar suas próprias propriedades.

### <a name="property-attributes"></a>Atributos de propriedade

Atributos de propriedade descrevem os direitos de acesso, valores válidos e outras informações relacionadas a uma propriedade. Por exemplo, a propriedade que representa a taxa de bits pode ser um intervalo de 8 quilobits por segundo (Kbps) a 20 Kbps com um valor de etapa de 1 Kbps.

Os direitos de acesso indicam se os chamadores podem ler, gravar e/ou excluir a propriedade. Valores válidos indicam restrições para valores de propriedade. Os valores válidos são considerados de um formulário específico. Os formulários de valor válidos incluem Range (ou seja, a propriedade pode levar um valor de Mín. para Máx. com a Etapa especificada), Enumeração (ou seja, o valor da propriedade é um dos valores na Lista especificada) e Nenhum (ou seja, não há valores válidos específicos).

### <a name="resources"></a>Recursos

Os recursos são espaço reservados para dados binários. Um objeto pode ter mais de um recurso. Por exemplo, se o objeto representasse um arquivo de imagem com uma anotação de áudio, os recursos desse objeto poderiam ser os seguinte:

-   Um recurso padrão. Esse recurso representa todo o arquivo de imagem. (Isso inclui todos os dados inseridos, como anotações de áudio, miniaturas e assim por diante)
-   Um recurso em miniatura. Esse recurso representa os dados em miniatura para a imagem.
-   Um recurso de anotação de áudio. Esse recurso representa os dados de áudio associados à imagem.

### <a name="resource-attributes"></a>Atributos de recurso

Semelhante aos atributos de propriedade, os atributos de recurso descrevem os direitos de acesso, o tamanho, o formato e outras informações relacionadas a um recurso. Por exemplo, os atributos de um recurso de anotação de áudio em um objeto de imagem podem especificar a taxa de bits, a contagem de canais e o formato de dados do áudio.

### <a name="rendering-profiles-and-resource-attributes"></a>Perfis de renderização e atributos de recurso

O perfil de renderização é um método que os aplicativos usam para descobrir os atributos válidos para um determinado recurso. Por exemplo, um telefone celular pode dar suporte a bitmaps com restrições específicas nos valores mínimo e máximo de largura e altura. Consultando os perfis de renderização para o objeto bitmap, um aplicativo pode recuperar esses valores exatos.

A saída de exemplo a seguir identifica as informações do perfil de renderização que o dispositivo retornaria se tivesse suporte para bitmaps com uma altura mínima de 10 pixels, uma largura mínima de 20 pixels, uma altura máxima de 1000 pixels e uma largura máxima de 2000 pixels.


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



Consulte [o](retrieving-the-rendering-capabilities-supported-by-a-device.md) tópico Recuperando as funcionalidades de renderização com suporte por um dispositivo no guia de programação para obter uma descrição de como seu aplicativo pode recuperar um perfil de renderização (e os atributos de recurso associados).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> </dl>

 

 



