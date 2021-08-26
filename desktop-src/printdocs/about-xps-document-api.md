---
description: a API de documento xps implementa o modelo de objeto xps e permite que os desenvolvedores criem um om xps, manipulem conteúdo de documento xps em programas nativos de Windows \\ \\ e salvem o om xps em um arquivo ou fluxo como um documento XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Sobre a API de documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b2363bba55fed184b1cf80bfc81fac9474444f77c9b867b461940e6b72d8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950906"
---
# <a name="about-xps-document-api"></a>Sobre a API de documento XPS

a [API de documento xps](documents-xps.md) implementa o modelo de objeto xps e permite que os desenvolvedores criem um om xps, manipulem conteúdo de documento xps em programas nativos de Windows \\ \\ e salvem o om xps em um arquivo ou fluxo como um documento XPS. Os desenvolvedores de módulos de pipeline de filtro XPSDrv também podem usar a API de documento XPS para manipular o conteúdo do documento XPS em um filtro de driver de impressora XPSDrv.

## <a name="xps-document-api-overview"></a>Visão geral da API de documento XPS

O modelo de objeto XPS é o modelo de informações de um documento XPS. O modelo de informações do documento XPS é separado do modelo de marcação que é usado dentro das partes do documento. O modelo de objeto XPS descreve a organização dos componentes internos que compõem um documento XPS e o modelo de marcação descreve o conteúdo desses componentes.

Em um programa, o modelo de objeto XPS é instanciado como um OM XPS. O OM XPS é essencialmente uma versão na memória do conteúdo de um documento XPS. Embora seja semelhante em uma organização lógica a um documento XPS, um OM XPS não é considerado um documento XPS até ser serializado para um arquivo ou um fluxo.

A estrutura exata da marcação não está disponível para o OM XPS quando um documento XPS é desserializado de marcação para um OM XPS. Por exemplo, se a propriedade foi representada como um elemento ou um atributo na marcação, o valor da propriedade de um objeto de documento é apresentado pelo OM XPS exatamente da mesma maneira.

A [API de documento XPS](documents-xps.md) pode ser dividida nas seguintes categorias:

-   [Interfaces de tronco do XPS OM](xps-om-trunk-interfaces.md)

    As interfaces de tronco fornecem acesso aos componentes de nível superior da estrutura do documento XPS. Essas interfaces também fornecem os meios para serializar um OM XPS e desserializar um documento XPS.

-   [Interfaces de página do XPS OM](xps-object-model-page-interfaces.md)

    As interfaces de página fornecem acesso ao conteúdo de uma página em um documento XPS. As interfaces que descrevem o conteúdo da página também estão incluídas com as interfaces de página.

-   [Assinaturas digitais do XPS OM](using-the-xps-digital-signatures.md)

    O OM XPS dá suporte a assinaturas digitais. No entanto, você pode acessar assinaturas digitais em um documento XPS diretamente sem criar um OM XPS. Para obter mais informações sobre como acessar as assinaturas digitais XPS sem um OM XPS, consulte [API de assinatura digital XPS](xps-digital-signatures.md).

-   [Interfaces de tíquete de impressão XPS OM](xps-object-model-print-ticket-interfaces.md)

    Os documentos XPS dão suporte a tíquetes de impressão no nível do pacote (trabalho), documento e página. Os tíquetes de impressão contêm informações sobre como formatar o conteúdo do documento para impressão ou exibição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Nesta seção**
</dt> <dt>

[Interfaces de tronco do XPS OM](xps-om-trunk-interfaces.md)
</dt> <dt>

[Interfaces de página do XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Assinaturas digitais do XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Interfaces de tíquete de impressão XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**Outros tópicos relacionados**
</dt> <dt>

[Inicializar um OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Assinaturas digitais do XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Referência da API do documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



