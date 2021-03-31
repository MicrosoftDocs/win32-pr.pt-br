---
title: Implementações de conjunto de propriedades em COM
description: Implementações de conjunto de propriedades em COM
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Armazenamento estruturado Strctd STG, using, conjunto de propriedades usado em COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917406"
---
# <a name="property-set-implementations-in-com"></a>Implementações de conjunto de propriedades em COM

Embora o potencial para usos de conjuntos de propriedades persistentes não seja totalmente tocado, atualmente, há dois usos principais:

-   Armazenando informações resumidas com um objeto, como um documento
-   Transferindo dados de propriedade entre objetos

Os conjuntos de propriedades COM foram projetados para armazenar dados adequados à representação como uma coleção de valores refinados de tamanho moderado. Os conjuntos de dados muito grandes para que isso seja viável devem ser divididos em fluxos, armazenamentos e/ou conjuntos de propriedades separados. O formato de dados do conjunto de propriedades COM não foi criado para fornecer um substituto para um banco de dado de muitos objetos pequenos.

O COM fornece implementações das interfaces do conjunto de propriedades para vários objetos, juntamente com três funções auxiliares. A seção a seguir descreve algumas características de desempenho dessas implementações. Para obter mais informações sobre interfaces específicas e como obter um ponteiro para essas interfaces, consulte o seguinte na seção de referência COM:

-   [IPropertySetStorage – implementação de arquivo composto](ipropertysetstorage-compound-file-implementation.md)

    A implementação do arquivo composto, que fornece as interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , também fornece as interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Dada uma implementação de arquivo composto de **IStorage**, a interface **IPropertySetStorage** pode ser obtida chamando-se [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

-   [IPropertySetStorage – implementação do sistema de arquivos NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)

    As interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) também podem ser obtidas para arquivos NTFS que não são arquivos compostos. Portanto, é possível obter essas interfaces para todos os arquivos em um volume NTFS.

-   [IPropertySetStorage – implementação autônoma](ipropertysetstorage-stand-alone-implementation.md)

    Quando essa implementação de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) é instanciada, ela recebe um ponteiro para um objeto que dá suporte à interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Em seguida, ele manipula os armazenamentos do conjunto de propriedades dentro desse objeto de armazenamento. Portanto, é possível acessar e manipular conjuntos de propriedades em qualquer objeto compatível com o.

-   [Considerações sobre implementação do IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

    Há vários problemas a serem considerados no fornecimento de uma implementação da interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Consulte essas considerações de *implementação* na seção de referência com.

Além disso, há quatro funções auxiliares, projetadas para ajudar a lidar com propriedades que foram lidas de uma propriedade definida na memória (em uma estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ):

-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

As seções a seguir discutem as implementações do conjunto de propriedades em COM COM mais detalhes:

-   [Gerenciando conjuntos de propriedades](managing-property-sets.md)
-   [Considerações sobre o conjunto de propriedades](property-set-considerations.md)
-   [Armazenando conjuntos de propriedades](storing-property-sets.md)
-   [Características de desempenho](performance-characteristics.md)
-   [Implementando o conjunto de propriedades de informações de resumo](implementing-the-summary-information-property-set.md)
-   [Considerações sobre implementação do IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

 

 