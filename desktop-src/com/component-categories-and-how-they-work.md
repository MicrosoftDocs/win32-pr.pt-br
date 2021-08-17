---
title: Categorias de componentes e como elas funcionam
description: Categorias de componentes e como elas funcionam
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfd5580e12ce3d4a44ca251142e29f6eea8f9f5823cf18999f876a4ef732d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737012"
---
# <a name="component-categories-and-how-they-work"></a>Categorias de componentes e como elas funcionam

As categorias de componentes identificam as áreas de funcionalidade às quais um componente de software dá suporte e requer, uma entrada do registro é usada para cada categoria ou área identificada da funcionalidade. Cada categoria de componente é identificada por um GUID (identificador global exclusivo), quando um controle é instalado, ele se registra como um controle no registro do sistema usando a ID de categoria de componente para controle, consulte [Autoregistro para controles](self-registration-for-controls.md). Dentro dos controles, o auto-registro também registrará as categorias de componentes que ele implementa e as categorias de componentes que ele requer que um contêiner dê suporte para hospedar o controle com êxito.

Quando um contêiner de controle está oferecendo controles ao usuário para inserir, ele só permite que o usuário selecione e instancie esses controles que poderão funcionar adequadamente nesse ambiente. Por exemplo, se o contêiner de controle não oferecer suporte a DataBinding, o contêiner não permitirá que o usuário selecione e instancie esses controles que têm uma entrada no registro, o que significa que eles exigem a categoria de componente DataBinding. Uma caixa de diálogo comum para a inserção de controle e as APIs para manipular as entradas do registro estão disponíveis.

As categorias de componente não são cumulativas ou exclusivas, um controle pode exigir qualquer combinação de categorias de componente para funcionar. Um controle que não tem entradas necessárias para categorias de componentes pode ser capaz de funcionar em qualquer contêiner de controle e não exigir qualquer funcionalidade específica de um contêiner de controle para funcionar.

As categorias de componentes a seguir são identificadas aqui, onde as especificações mais detalhadas necessárias das categorias podem estar disponíveis.

-   Contenção de controle [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) .
-   Associação de dados simples por meio da interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) .
-   DataBinding avançada (como compatível com as interfaces de DataBinding adicionais do VB 4.0).
-   Visual Basic interfaces privadas – [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat), [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Controles de reconhecimento da Internet.
-   Controles sem janela.

Essa não é uma lista definitiva de categorias; outras categorias provavelmente serão definidas no futuro à medida que novos requisitos forem identificados. Uma lista atualizada de categorias de componentes está disponível na Microsoft; Essa lista reflete as categorias de componentes que foram identificadas pela Microsoft e outras que sobre quais fornecedores informaram à Microsoft.

É importante lembrar que os controles devem tentar trabalhar em tantos ambientes quanto possível. Se possível, o controle deve degradar sua funcionalidade quando colocado em um contêiner que não oferece suporte a determinadas interfaces. A finalidade das categorias de componente é evitar uma situação em que o controle seja colocado em um ambiente que não seja adequado e o controle não possa obter a tarefa desejada. Em geral, um controle deve degradar normalmente quando as interfaces não estão presentes, um controle pode optar por aconselhar o usuário com uma caixa de mensagem de que alguma funcionalidade não está disponível ou documentar claramente a funcionalidade necessária de um contêiner de controle para um desempenho ideal.

Observe que controles e contêineres mais antigos não fazem uso de categorias de componente e, em vez disso, dependem da palavra-chave Control que está presente no controle no registro. Para ser reconhecido por controles de contêineres mais antigos pode desejar registrar a palavra-chave Control no registro, os desenvolvedores de controle devem verificar se o controle pode ser hospedado com êxito nesses contêineres antes de fazer isso. Os contêineres que usam categorias de componentes podem usá-los com êxito para hospedar controles mais antigos à medida que a DLL de categoria de componentes manipula o mapeamento, existe uma categoria separada para controles mais antigos do CATID \_ ControlV1 para que um contêiner, opcionalmente, possa excluí-los, se necessário.

Como as categorias de componente são identificadas por GUIDs, é possível que os contêineres que oferecem determinada funcionalidade específica tenham suas próprias IDs de categoria, geradas usando uma ferramenta de geração de GUID. No entanto, isso pode prejudicar a vantagem da interoperabilidade de controles e contêineres, portanto, é preferível que sempre que as categorias de componentes existentes forem usadas. os fornecedores são incentivados a se consultar ao definir novas categorias de componentes para garantir que atendam aos requisitos comuns do marketplace e sigam o espírito de interoperabilidade dos controles de ActiveX.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 




