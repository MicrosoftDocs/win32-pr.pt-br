---
title: Implementação do Gerenciador de categorias de componentes
description: À medida que aumenta o número de componentes disponíveis, torna-se cada vez mais difícil gerenciar esses componentes. Em termos das interfaces que expõem, bem como as tarefas que eles executam, muitos componentes oferecem funcionalidade semelhante.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941ba5f422a4305a3bb6056d1d02648dde3bffc9c9f872fe7f7804ebb90a19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679206"
---
# <a name="component-categories-manager-implementation"></a>Implementação do Gerenciador de categorias de componentes

À medida que aumenta o número de componentes disponíveis, torna-se cada vez mais difícil gerenciar esses componentes. Em termos das interfaces que expõem, bem como as tarefas que eles executam, muitos componentes oferecem funcionalidade semelhante.

Geralmente, é necessário enumerar os componentes que podem ser usados em um determinado contexto. Exemplos disso são a caixa de diálogo **Inserir objeto** usada em documentos OLE compostos e a caixa de diálogo **controle de inserção** usada em controles OLE. Essas caixas de diálogo listam todos os componentes que atendem (ou alegam atender) os contratos de interface para documentos ou controles compostos. Essas categorias existentes (documento OLE, controle OLE) não implicam uma assinatura de interface exata. Documentos OLE precisam expor um determinado conjunto de interfaces principais (por exemplo, [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) ou [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)), mas também podem expor interfaces adicionais, como [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink).

No passado, os componentes foram marcados com a adição de um nome legível ("Insertável", "Control" e assim por diante) como uma subchave ao **\_ CLSID raiz da classe HKEY \_ \\ \\ {...}** chave do registro correspondente ao componente. Isso funciona bem para uma definição central de categorias, mas o nome dos riscos é colisões quando muitas partes independentes definem novas categorias. Como em outras áreas do COM, a solução para fornecer um namespace extensível está no uso de GUIDs (identificadores globais exclusivos). Em vez de usar um nome legível, um número exclusivo (CATID) é atribuído a cada categoria.

Outra limitação da categorização existente é que ela é limitada a expressar os recursos do próprio componente. Muitos componentes exigem certos recursos dos contêineres. Quando esse componente é inserido em um contêiner, a inserção pode falhar ou se comportar inesperadamente, mesmo que o componente atenda aos contratos implícitos por uma de suas categorias. Para enumerar os componentes que podem ser usados com êxito em determinadas situações, os recursos do componente e do contêiner devem ser considerados.

Devido a essas considerações, as seguintes alterações foram feitas na categorização existente:

-   As categorias são indicadas usando CATIDs que são identificadores globalmente exclusivos.
-   Na subchave **componentes** da chave do registro do **\_ \_ \\ CLSID da classe HKEY** , duas subchaves separadas, "categorias implementadas" e "categorias necessárias", foram desenvolvidas. Essas subchaves contêm as listas de CATIDs fornecidas pelo componente ou que o contêiner do componente deve fornecer.

Para facilitar o gerenciamento das categorias de componentes, as categorias são listadas em um local central no registro: **\_ categorias de \_ \\ componentes raiz de classes hKey**. Essa chave lista as categorias instaladas com seu CATID e com nomes localizados e legíveis.

Para obter mais informações, consulte estes tópicos:

-   [Categorizando por recursos de componente](categorizing-by-component-capabilities.md)
-   [Categorizando por recursos de contêiner](categorizing-by-container-capabilities.md)
-   [O Gerenciador de categorias de componentes](the-component-categories-manager.md)
-   [Classes e associações padrão](default-classes-and-associations.md)
-   [Definindo categorias de componentes](defining-component-categories.md)
-   [Associando ícones a uma categoria](associating-icons-with-a-category.md)

 

 




