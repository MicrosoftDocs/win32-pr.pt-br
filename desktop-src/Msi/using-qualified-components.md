---
description: Os componentes qualificados são um método de indireção e podem ser usados para agrupar componentes com funcionalidade paralela em categorias.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Usando componentes qualificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090475"
---
# <a name="using-qualified-components"></a>Usando componentes qualificados

Os componentes qualificados são um método de indireção e podem ser usados para agrupar componentes com funcionalidade paralela em categorias.

Para retornar o caminho completo e instalar um [componente qualificado](qualified-components.md), chame [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).

Para enumerar todos os qualificadores de componente qualificados e cadeias de caracteres descritivas, chame [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

**Para agrupar componentes em uma categoria de componente qualificado**

1.  Deve haver um registro na tabela de [componentes](component-table.md) para cada componente incluído na nova categoria de componentes qualificados. Crie os campos na tabela de componentes da mesma forma que para componentes comuns. Observe que cada componente qualificado deve ter um GUID de ID de componente exclusivo inserido na coluna ComponentID da tabela de componentes.
2.  Gere uma cadeia de texto de qualificador para cada componente qualificado. O qualificador deve ser uma cadeia de caracteres de texto exclusiva que pode ser facilmente gerada ao pesquisar um componente qualificado. Por exemplo, se os componentes na categoria estiverem sendo qualificados por idioma, o LCID (identificador de localidade numérica) será uma cadeia de caracteres de qualificador razoável.
3.  Adicione um registro na [tabela PublishComponent](publishcomponent-table.md) para cada componente qualificado. Insira os identificadores de componente qualificados da coluna componente da tabela componente na \_ coluna componente da tabela PublishComponent. Insira as cadeias de caracteres do qualificador para cada componente qualificado na coluna qualificador. Insira uma cadeia de caracteres localizada a ser exibida para o usuário e descrevendo o componente qualificado na coluna opcional AppData. Uma cadeia de caracteres explicativa deve ser colocada no campo AppData, como "dicionário francês", em vez de apenas o LCID numérico. Insira o nome do recurso que usa esse componente na \_ coluna recurso. O identificador de recurso neste campo também deve estar listado na coluna recurso da tabela de [recursos](feature-table.md).
4.  Gere um GUID de categoria para esta categoria de componentes qualificados. Este deve ser um [GUID](guid.md)válido. Se você usar um utilitário como o GUIDGEN para gerar o GUID, verifique se ele contém apenas letras maiúsculas. Para cada componente qualificado nessa categoria, insira o GUID da categoria no campo ComponentID da [tabela PublishComponent](publishcomponent-table.md).

O exemplo a seguir ilustra como a categoria "modelos de FAX" de componentes qualificados é criada nas tabelas componente, recurso e PublishComponent.

[Tabela PublishComponent](publishcomponent-table.md)



| ComponentId                  | Qualificador | AppData             | Recurso\_   | Componente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {GUID de categoria do modelo de FAX} | 1046      | Modelo em inglês americano | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Modelo japonês   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | Modelo tailandês       | FAXTemplate | FAXTemplateTHA |
|                              | 1031      | Modelo alemão     | FAXTemplate | FAXTemplateDEU |



 

[Tabela de componentes](component-table.md) (tabela parcial)



| Componente      | ComponentId                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*Modelo de fax (inglês americano) GUID do componente*} |
| FAXTemplateJPN | {*GUID do componente do modelo de fax (japonês)*}   |
| FAXTemplateTHA | {*GUID do componente do modelo de fax (tailandês)*}       |
| FAXTemplateDEU | {*GUID do componente do modelo de fax (alemão)*}     |



 

[Tabela de recursos](feature-table.md) (tabela parcial)



| Recurso     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



