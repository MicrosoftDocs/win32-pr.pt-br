---
description: Um componente qualificado é um método de ind indireta de nível único, semelhante a um ponteiro.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Componentes qualificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c9a5ccd757516402a951afa3a105d51e3a0b3d22a88614983997dbcd6d07f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376299"
---
# <a name="qualified-components"></a>Componentes qualificados

Um componente qualificado é um método de ind indireta de nível único, semelhante a um ponteiro. Componentes qualificados são usados principalmente para agrupar componentes com funcionalidade paralela em categorias. Por exemplo, se você tiver 30 componentes listados na tabela Componente que são o mesmo modelo de fax Microsoft Word localizado em 30 idiomas, você poderá agrupar esses componentes em uma categoria de componentes qualificados usando a tabela [PublishComponent](publishcomponent-table.md). [](component-table.md)

Os componentes qualificados são inseridos na tabela Componente da mesma maneira que os componentes comuns. Cada componente deve ter um GUID de ID de componente exclusivo e um identificador de componente especificados na tabela Componente. Além disso, os componentes qualificados são associados a um GUID de categoria e um qualificador de cadeia de caracteres de texto na tabela PublishComponent. Os componentes qualificados são referenciados pelo GUID da categoria e pelo qualificador, que apenas aponta para o componente comum na tabela Componente.

Por exemplo, um GUID de ID de componente qualificado pode apontar para diferentes versões de linguagem de uma DLL de recurso. Nesse caso, o grupo de DLLs de recursos localizados consiste na categoria e as cadeias de caracteres LCID (identificadores de localidade numérica) são comumente usadas como qualificadores. Um desenvolvedor pode ter um pacote de instalação que usa esses componentes qualificados para fazer o seguinte:

-   Encontre o caminho para uma versão de linguagem específica da DLL de recurso usando [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) e instale o recurso.
-   Determine todas as versões de idioma da DLL de recurso que estão presentes chamando [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).
-   Prepare o aplicativo para dar suporte a idiomas adicionais. Um pacote de idiomas futuro para o aplicativo pode usar o componente qualificado para adicionar mais versões de linguagem da DLL de recurso.

Para obter mais informações, consulte [Usando componentes qualificados](using-qualified-components.md).

 

 



