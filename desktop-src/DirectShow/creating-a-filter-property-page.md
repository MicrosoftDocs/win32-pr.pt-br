---
description: Criando uma página de propriedades de filtro
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Criando uma página de propriedades de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d891c42a6cdb2f1c636278a8270fb13a69580697a31fe78f2f3687246f20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108256"
---
# <a name="creating-a-filter-property-page"></a>Criando uma página de propriedades de filtro

Esta seção descreve como criar uma página de propriedades para um filtro DirectShow personalizado, usando a [**classe CBasePropertyPage.**](cbasepropertypage.md) O código de exemplo nesta seção mostra todas as etapas necessárias para criar uma página de propriedades. O exemplo mostra uma página de propriedades para um filtro de efeito de vídeo hipotético que dá suporte a uma propriedade de saturação. A página de propriedades tem um controle deslizante, que o usuário pode mover para ajustar o nível de saturação do filtro.

Esta seção contém os seguintes tópicos:

-   [Etapa 1. Definir um mecanismo para definir a propriedade](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Etapa 2. Implementar ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [Etapa 3. Suporte a QueryInterface](step-3--support-queryinterface.md)
-   [Etapa 4. Criar a página de propriedades](step-4--create-the-property-page.md)
-   [Etapa 5. Armazenar um ponteiro para o filtro](step-5--store-a-pointer-to-the-filter.md)
-   [Etapa 6. Inicializar a caixa de diálogo](step-6--initialize-the-dialog.md)
-   [Etapa 7. Manipular mensagens de janela](step-7--handle-window-messages.md)
-   [Etapa 8. Aplicar alterações de propriedade](step-8--apply-property-changes.md)
-   [Etapa 9. Desconectar a página de propriedades](step-9--disconnect-the-property-page.md)
-   [Etapa 10. Suporte ao registro COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



