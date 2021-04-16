---
description: Criando uma página de propriedades de filtro
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Criando uma página de propriedades de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105751099"
---
# <a name="creating-a-filter-property-page"></a>Criando uma página de propriedades de filtro

Esta seção descreve como criar uma página de propriedades para um filtro do DirectShow personalizado, usando a classe [**CBasePropertyPage**](cbasepropertypage.md) . O código de exemplo nesta seção mostra todas as etapas necessárias para criar uma página de propriedades. O exemplo mostra uma página de propriedades para um filtro de efeito de vídeo hipotético que dá suporte a uma propriedade de saturação. A página de propriedades tem um controle deslizante, que o usuário pode mover para ajustar o nível de saturação do filtro.

Esta seção contém os seguintes tópicos:

-   [Etapa 1. Definir um mecanismo para definir a propriedade](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Etapa 2. Implementar ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [Etapa 3. Suporte a QueryInterface](step-3--support-queryinterface.md)
-   [Etapa 4. Criar a página de propriedades](step-4--create-the-property-page.md)
-   [Etapa 5. Armazenar um ponteiro para o filtro](step-5--store-a-pointer-to-the-filter.md)
-   [Etapa 6. Inicializar a caixa de diálogo](step-6--initialize-the-dialog.md)
-   [Etapa 7. Processar mensagens de janela](step-7--handle-window-messages.md)
-   [Etapa 8. Aplicar alterações de propriedade](step-8--apply-property-changes.md)
-   [Etapa 9. Desconectar a página de propriedades](step-9--disconnect-the-property-page.md)
-   [Etapa 10. Suporte ao registro COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



