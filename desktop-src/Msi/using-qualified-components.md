---
description: Componentes qualificados são um método de indcisão e podem ser usados para agrupar componentes com funcionalidade paralela em categorias.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Usando componentes qualificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c92d165bc06640efea4b8678eeaefa5eb04c36f1b47b6c965faeea00c66adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622942"
---
# <a name="using-qualified-components"></a>Usando componentes qualificados

Componentes qualificados são um método de indcisão e podem ser usados para agrupar componentes com funcionalidade paralela em categorias.

Para retornar o caminho completo e instalar um componente [qualificado,](qualified-components.md)chame [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

Para enumerar todos os qualificadores de componente qualificados e cadeias de caracteres descritivas, chame [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

**Para agrupar componentes em uma categoria de componente qualificado**

1.  Deve haver um registro na tabela [Componente](component-table.md) para cada componente incluído na nova categoria de componentes qualificados. Autor dos campos na tabela Componente da mesma forma que para componentes comuns. Observe que cada componente qualificado deve ter um GUID de ID de componente exclusivo inserido na coluna ComponentId da tabela Component.
2.  Gere uma cadeia de caracteres de texto qualificador para cada componente qualificado. O qualificador deve ser uma cadeia de caracteres de texto exclusiva que pode ser gerada facilmente ao procurar um componente qualificado. Por exemplo, se os componentes na categoria estão sendo qualificados por idioma, o LCID (identificador de localidade numérica) é uma cadeia de caracteres de qualificador razoável.
3.  Adicione um registro na [tabela PublishComponent](publishcomponent-table.md) para cada componente qualificado. Insira os identificadores de componente qualificado da coluna Componente da tabela Componente na coluna Componente \_ da tabela PublishComponent. Insira as cadeias de caracteres do qualificador para cada componente qualificado na coluna Qualificador. Insira uma cadeia de caracteres localizada a ser exibida para o usuário e descrevendo o componente qualificado na coluna AppData opcional. Uma cadeia de caracteres explicativa deve ser colocada no campo AppData, como "Dicionário francês", em vez de apenas o LCID numérico. Insira o nome do recurso que usa esse componente na coluna \_ Recurso. O identificador de recurso nesse campo também deve ser listado na coluna Recurso da [tabela Recurso](feature-table.md).
4.  Gere um GUID de categoria para essa categoria de componentes qualificados. Esse deve ser um [GUID válido.](guid.md) Se você usar um utilitário como GUIDGEN para gerar o GUID, certifique-se de que ele contenha apenas letras maiúsculas. Para cada componente qualificado nessa categoria, insira o GUID da categoria no campo ComponentId da [tabela PublishComponent](publishcomponent-table.md).

O exemplo a seguir ilustra como a categoria "Modelos de FAX" de componentes qualificados é autorada nas tabelas Componente, Recurso e PublishComponent.

[Tabela PublishComponent](publishcomponent-table.md)



| Componentid                  | Qualificador | AppData             | Recurso\_   | Componente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {GUID da Categoria de Modelo de FAX} | 1046      | Modelo em inglês dos EUA | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Modelo japonês   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | Modelo tailandês       | FAXTemplate | FAXTemplateTHA |
|                              | 1031      | Modelo alemão     | FAXTemplate | FAXTemplateDEU |



 

[Tabela de componentes](component-table.md) (tabela parcial)



| Componente      | Componentid                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*MODELO DE FAX (INGLÊS DOS EUA) componente GUID*} |
| FAXTemplateJPN | {*MODELO DE FAX (japonês) GUID do componente*}   |
| FAXTemplateTHA | {*MODELO DE FAX (tailandês) GUID do componente*}       |
| FAXTemplateDEU | {*MODELO DE FAX (alemão) GUID do componente*}     |



 

[Tabela de recursos](feature-table.md) (tabela parcial)



| Recurso     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



