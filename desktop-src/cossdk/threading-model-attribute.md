---
description: O COM+ gerencia threads para você. Cada componente COM tem uma propriedade ThreadingModel que você pode especificar ao desenvolver o componente. Essa propriedade determina como os objetos de componentes são atribuídos a threads para execução de método.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Atributo de modelo de Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370390"
---
# <a name="threading-model-attribute"></a>Atributo de modelo de Threading

O COM+ gerencia threads para você. Cada componente COM tem uma propriedade **ThreadingModel** que você pode especificar ao desenvolver o componente. Essa propriedade determina como os objetos do componente são atribuídos a threads para execução de método.

Você pode usar a ferramenta administrativa serviços de componentes para exibir a propriedade Threading-Model clicando com o botão direito do mouse em um componente na pasta **componentes** , clicando em **Propriedades** e, em seguida, clicando na guia **simultaneidade** . No **modelo de Threading**, os valores possíveis são os seguintes:

-   **Principal thread apartment**
-   **Single thread apartment**
-   **Thread apartment gratuito**
-   **Apartamento neutro**
-   **Qualquer apartamento**

O modelo de Threading preferencial para COM+ é o [apartamento neutro](neutral-apartments.md). No entanto, se você não especificar um modelo de threading para seu componente, o COM+ usará o principal thread apartment, que é o padrão.

> [!Note]  
> Para obter informações mais detalhadas, consulte [escolhendo o modelo de Threading](/windows/desktop/com/choosing-the-threading-model).

 

A tabela a seguir mostra o modelo de programação para Apartments no COM+.



| Modelar                     | Sta                                                 | Gratuita                               | Ambos                               | Neutro                      | Não especificado                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| Thread único, não principal | Criado no apartamento atual                              | Criado em apartamento multithread | Criado no apartamento atual       | Criado em apartamento neutro | Criado no Apartment segmentado principal |
| Thread único, principal     | Criado no apartamento atual                              | Criado em apartamento multithread | Criado no apartamento atual       | Criado em apartamento neutro | Criado no apartamento atual       |
| Multithread             | Criado em um apartamento de thread único de host                 | Criado em apartamento multithread | Criado em apartamento multithread | Criado em apartamento neutro | Criado no Apartment segmentado principal |
| Neutro (no thread STA)   | Criado no Apartment de thread único do host para este thread | Criado em apartamento multithread | Criado em apartamento neutro       | Criado em apartamento neutro | Criado no Apartment segmentado principal |
| Neutro (no thread MTA)   | Criado em um apartamento de thread único de host                 | Criado em apartamento multithread | Criado em apartamento neutro       | Criado em apartamento neutro | Criado no Apartment segmentado principal |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
