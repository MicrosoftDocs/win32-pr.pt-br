---
title: Formato do conjunto de propriedades serializadas de armazenamento estruturado
description: Os conjuntos de propriedades persistentes fornecem uma opção para armazenar dados em entidades do sistema de arquivos. É recomendável que, para criá-los e gerenciá-los, você use as interfaces IPropertySetStorage e IPropertyStorage descritas em Propriedades e conjuntos de propriedade.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- Armazenamento estruturado Strctd STG, conceitos básicos, formato de conjunto de propriedades serializadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea03d5ccab337897be801840080e83a6fa86880
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105756132"
---
# <a name="structured-storage-serialized-property-set-format"></a>Formato do conjunto de propriedades serializadas de armazenamento estruturado

Os conjuntos de propriedades persistentes fornecem uma opção para armazenar dados em entidades do sistema de arquivos. É recomendável que, para criá-los e gerenciá-los, você use as interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) descritas em [Propriedades e conjuntos de propriedade](properties-and-property-sets.md).

Os conjuntos de propriedades são compostos de uma seção marcada de valores, com a seção identificada exclusivamente por um identificador de formato (FMTID). Cada propriedade consiste em um identificador de propriedade e um indicador de tipo que representa um valor. Cada valor armazenado em um conjunto de propriedades tem um identificador de propriedade exclusivo que distingue a propriedade. O indicador de tipo descreve a representação dos dados no valor.

Ao usar as interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , você não precisa manipular a estrutura de formato do conjunto de propriedades serializadas com. Para obter mais informações, consulte os tópicos listados:

Todos os elementos de dados dentro de um conjunto de propriedades são armazenados na representação Intel (ou seja, em ordem de byte little-endian).

COM define um formato de dados serializado padrão para conjuntos de propriedades. Ao lidar com o formato serializado, e não com as interfaces, os conjuntos de propriedades têm as seguintes características:

-   Os conjuntos de propriedades permitem que aplicativos diferentes criem seus próprios conjuntos de propriedades independentes para atender ao aplicativo.
-   Os conjuntos de propriedades podem ser armazenados em uma única instância de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ou em uma instância de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) que contenha vários fluxos. Os conjuntos de propriedades são simplesmente outro tipo de dados que pode ser armazenado em muitas formas diferentes de armazenamento em disco ou na memória. Para obter mais informações e convenções recomendadas para criar o nome da cadeia de caracteres para o objeto de armazenamento, consulte [convenções de nomenclatura de objeto de armazenamento](storage-object-naming-conventions.md).
-   Os conjuntos de propriedades permitem que um dicionário de nomes de exibição seja incluído para descrever o conteúdo. É recomendável um conjunto de convenções para escolher nomes de propriedade. Para obter mais informações sobre esse dicionário opcional, consulte [identificadores de propriedade reservada](reserved-property-identifiers.md), incluindo a [ID de propriedade 0](/windows/desktop/Stg/reserved-property-identifiers).

O fluxo do conjunto de propriedades é dividido em três partes principais:

-   parâmetro
-   FORMATid/par de deslocamento
-   Seção que contém os valores reais do conjunto de propriedades

O comprimento geral do fluxo do conjunto de propriedades deve ser menor ou igual a 256K. As seções a seguir, o [cabeçalho do conjunto de propriedades](property-set-header.md), o identificador de [formato/par de deslocamento](format-identifier-offset-pair.md)e a [seção](section.md) (incluindo [identificadores de propriedade/pares de deslocamento](property-identifiers-offset-pairs.md)), com tópicos de suporte, descrevem os componentes individuais que compõem o formato de dados do conjunto de propriedades.

> [!Note]  
> As versões anteriores deste documento descreveram as extensões para o fluxo do conjunto de propriedades com mais de uma seção permitida, mas que foram revisadas para fornecer uma seção no fluxo de propriedades. A única exceção são [os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

 

 