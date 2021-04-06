---
title: Armazenando conjuntos de propriedades
description: Os aplicativos podem expor alguns dos dados de estado de seus documentos para que outros aplicativos possam localizar e ler esses dados.
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- Armazenando conjuntos de propriedades armazenamento estruturado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60710b84b52fcc709f8ba3ad1e930d6f5a50a4cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822358"
---
# <a name="storing-property-sets"></a>Armazenando conjuntos de propriedades

Os aplicativos podem expor alguns dos dados de estado de seus documentos para que outros aplicativos possam localizar e ler esses dados. Alguns exemplos são um conjunto de propriedades que descreve o autor, o título e as palavras-chave de um documento criado com um processador de texto ou a lista de fontes usadas em um documento. Este recurso não está restrito a documentos; Ele também pode ser usado em objetos inseridos. Em geral, o acesso aos conjuntos de propriedades deve ser por meio das interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , mas esta seção descreve a maneira recomendada anteriormente.

> [!Note]  
> Se estiver armazenando um conjunto de propriedades que é interno ao seu aplicativo, talvez você não queira usar as diretrizes a seguir. Para expor seu conjunto de propriedades para outros aplicativos, siga estas diretrizes.

 

**Para armazenar um conjunto de propriedades em um arquivo composto**

1.  Crie uma instância [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no mesmo nível da estrutura de armazenamento que seus fluxos de dados. Siga o nome da sua instância de **IStorage** ou **IStream** com " \\ 005". Os nomes de fluxo e armazenamento que começam com 0x05 são reservados para conjuntos de propriedades comuns que podem ser compartilhados entre aplicativos. Além disso, os fluxos que começam com esse valor são limitados a 256 KB. Os nomes podem ser selecionados de nomes e formatos publicados ou atribuindo a propriedade definir um FMTID e derivando o nome de FMTID de acordo com as convenções descritas em [convenções de nomenclatura de objeto de armazenamento](storage-object-naming-conventions.md).
2.  Um conjunto de propriedades pode ser armazenado em uma única instância de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ou em uma instância de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) que contém vários fluxos e armazenamentos. No caso de uma instância **IStorage** , o fluxo contido, denominado Contents, é o fluxo principal que contém os valores de propriedade, em que alguns valores podem ser nomes de outros fluxos ou instâncias de armazenamento no armazenamento para esse conjunto de propriedades.
3.  Especifique o CLSID da classe de objeto que pode exibir ou fornecer acesso programático aos valores de propriedade. Se não houver nenhuma classe, o CLSID deverá ser definido como o identificador de formato do conjunto de propriedades. Para um conjunto de propriedades que usa uma instância de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , defina o CLSID da instância de **IStorage** para ser o mesmo que o armazenado no fluxo de conteúdo ou para **CLSID \_ NULL**; o valor em uma instância **IStorage** recém-criada.
4.  Você tem a opção de especificar nomes exibíveis que formam o conteúdo do dicionário.

Alguns aplicativos podem ler apenas as implementações de conjuntos de propriedades armazenados como instâncias de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) . Os aplicativos devem ser escritos para esperar que um conjunto de propriedades possa ser armazenado em uma instância [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou **IStream** , a menos que a definição do conjunto de propriedades indique o contrário. Por exemplo, a definição do conjunto de propriedades de informações resumidas declara que ela só pode ser armazenada em uma instância de **IStream** nomeada. Nos casos em que você está procurando um conjunto de propriedades e não sabe se ele é um armazenamento ou fluxo, procure uma instância de **IStream** com seu nome de conjunto de propriedades primeiro. Se isso falhar, procure uma instância de **IStorage** .

Para entender melhor o armazenamento de conjuntos de propriedades em uma implementação [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , suponha que exista uma classe de aplicativos que edite informações sobre animais. Primeiro, um CLSID (CLSID \_ AnimalApp) é definido para esse conjunto de aplicativos, para que eles possam indicar que eles entendem os conjuntos de propriedades que contêm informações de animais (**FMTID \_ AnimalInfo**) e outros que contêm informações médicas (**FMTID \_ MedicalInfo**).

``` syntax
IStorage (File): "C:\OLE\REVO.DOC" 
  IStorage: "\005AnimalInfo", CLSID = CLSID_AnimalApp 
    IStream: "Contents" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = FMTID_AnimalInfo 
      Property: Type = PID_ANIMALTYPE, Type = VT_LPWSTR, 
              Value = L"Dog" 
      Property: Type = PID_ANIMALNAME, Type = VT_LPWSTR, 
              Value = L"Revo" 
      Property: Type = PID_MEDICALHISTORY, Type = VT_STREAMED_OBJECT, 
              Value = "MedicalInfo" 
      ... 
    IStream: "MedicalInfo" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = CLSID_MedicalInfo 
      Property: Type = PID_VETNAME, Type = VT_LPWSTR, 
              Value = L"Dr. Woof" 
      Property: Type = PID_LASTEXAM, Type = VT_DATE, Value = ...
```

Lembre-se de que o CLSID da interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e os dois conjuntos de propriedades são **CLSID \_ AnimalApp**. Isso identifica qualquer aplicativo que possa exibir e/ou fornecer acesso programático a esses conjuntos de propriedades. Qualquer aplicativo pode ler os dados dentro dos conjuntos de Propriedades (o ponto atrás dos conjuntos de propriedades), mas somente os aplicativos identificados com o identificador de classe de CLSID \_ AnimalApp podem entender o significado dos dados nos conjuntos de propriedades.

 

 




