---
description: Um componente qualificado é um método de indireção de nível único, semelhante a um ponteiro.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Componentes qualificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828253"
---
# <a name="qualified-components"></a>Componentes qualificados

Um componente qualificado é um método de indireção de nível único, semelhante a um ponteiro. Os componentes qualificados são usados principalmente para agrupar componentes com funcionalidade paralela em categorias. Por exemplo, se você tiver 30 componentes listados na [tabela de componentes](component-table.md) que são do mesmo modelo de fax do Microsoft Word localizado em 30 idiomas, poderá agrupá-los em uma categoria de componentes qualificados usando a [tabela PublishComponent](publishcomponent-table.md).

Os componentes qualificados são inseridos na tabela de componentes da mesma maneira que os componentes comuns. Cada componente deve ter um GUID de ID de componente exclusivo e um identificador de componente especificado na tabela de componentes. Além disso, os componentes qualificados são associados a um GUID de categoria e um qualificador de cadeia de caracteres de texto na tabela PublishComponent. Os componentes qualificados são referenciados pelo GUID da categoria e pelo qualificador, que apenas aponta para o componente comum na tabela de componentes.

Por exemplo, um GUID de ID de componente qualificado pode apontar para versões de idioma diferentes de uma DLL de recurso. Nesse caso, o grupo de DLLs de recursos localizadas compreende a categoria e as cadeias de caracteres LCID (identificadores de localidade numérica) geralmente são usadas como qualificadores. Um desenvolvedor poderia criar um pacote de instalação que usa esses componentes qualificados para fazer o seguinte:

-   Localize o caminho para uma versão de idioma específica da DLL de recurso usando [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) e instale o recurso.
-   Determine todas as versões de idioma da DLL de recursos que estão presentes chamando [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).
-   Prepare o aplicativo para dar suporte a idiomas adicionais. Um pacote de idiomas futuro para o aplicativo pode usar o componente qualificado para adicionar mais versões de idioma da DLL de recursos.

Para obter mais informações, consulte [usando componentes qualificados](using-qualified-components.md).

 

 



