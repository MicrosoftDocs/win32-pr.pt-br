---
title: Gerenciando conjuntos de propriedades
description: Um conjunto de propriedades persistentes contém dados relacionados como propriedades.
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- Gerenciando conjuntos de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b6b81c466232d4fd325d53a3cfe67ebb1cbc60c757a6dfe135a021ab7892a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960880"
---
# <a name="managing-property-sets"></a>Gerenciando conjuntos de propriedades

Um conjunto de propriedades persistentes contém dados relacionados como propriedades. Cada conjunto de propriedades é identificado com um FMTID e um identificador global exclusivo (GUID) que habilita aplicativos, acessando o conjunto de propriedades, para identificar o conjunto de propriedades. Com essa identificação, o aplicativo interpreta as propriedades que o conjunto contém.

Por exemplo, as propriedades de formatação de caracteres em um processador de texto ou os atributos de renderização de um elemento em um programa de desenho são conjuntos de propriedades.

COM define a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para facilitar o gerenciamento de conjuntos de propriedades. Por meio dos métodos dessa interface, você pode criar um novo conjunto de propriedades ou abrir ou excluir um conjunto de propriedades existente. Além disso, ele fornece um método que cria um enumerador e fornece um ponteiro para sua interface [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Você pode chamar os métodos dessa interface para enumerar estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) em seu objeto, o que fornecerá informações sobre todos os conjuntos de propriedades no objeto.

Quando você cria ou abre uma instância de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), é semelhante a abrir um objeto que dá suporte a [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), pois você precisa especificar o modo de armazenamento no qual você está abrindo a interface. Para **IStorage**, isso inclui o modo de transação, o modo de leitura/gravação e o modo de compartilhamento.

Quando você cria um conjunto de propriedades com uma chamada para [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), especifica se o conjunto de propriedades é simples ou não simples. um conjunto de propriedades simples contém tipos que podem ser gravados totalmente dentro do fluxo do conjunto de propriedades, que deve ser limitado em tamanho e não pode ser maior que 256 KB em Windows NT 4,0 e anteriores, ou 1 MB em Windows 2000, Windows XP e Windows Server 2003. No entanto, quando você precisar armazenar uma quantidade maior de informações no conjunto de propriedades, poderá especificar que o conjunto de propriedades não é simples. Isso permite que você use um ou mais dos tipos que especificam apenas um ponteiro para um objeto de armazenamento ou de fluxo. Esses tipos são o \_ fluxo VT, o \_ objeto transmitido VT, o \_ armazenamento VT e o \_ objeto armazenado VT \_ .

os dados armazenados nessas propriedades não são contados em relação ao limite de tamanho do conjunto de propriedades de 256 KB em Windows NT 4,0 ou anterior ou ao limite de 1 MB no Windows 2000, Windows XP e Windows Server 2003. No entanto, os dados sobre a propriedade, como seu nome, se aplicam. Além disso, se você precisar de uma atualização transacionada, o conjunto de propriedades deverá ser não simples. É claro que há uma certa penalidade de desempenho para a abertura desses tipos, pois ele requer a abertura do fluxo ou objeto de armazenamento ao qual você tem o ponteiro.

Se seu aplicativo usar arquivos compostos, você poderá usar a implementação fornecida pelo COM dessas interfaces, que são implementadas no objeto de armazenamento de arquivo composto COM.

Cada conjunto de propriedades consiste principalmente em um grupo de propriedades logicamente conectado, conforme descrito em [Gerenciando Propriedades](managing-properties.md).

Para obter mais informações sobre conjuntos de propriedades em COM, consulte:

-   [Implementações de conjunto de propriedades em COM](property-set-implementations-in-com.md)
-   [Considerações sobre o conjunto de propriedades](property-set-considerations.md)
-   [Considerações sobre implementação do IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Armazenando conjuntos de propriedades](storing-property-sets.md)
-   [Características de desempenho](performance-characteristics.md)
-   [Implementando o conjunto de propriedades de informações de resumo](implementing-the-summary-information-property-set.md)

 

 