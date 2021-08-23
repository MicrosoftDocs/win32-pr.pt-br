---
description: Entendendo a internacionalização
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Entendendo a internacionalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed47364da56e2c5ab5e13001b1b49360b23caa39997484e5058022516f437b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638786"
---
# <a name="understanding-internationalization"></a>Entendendo a internacionalização

O desenvolvimento de produtos de software internacionalizados requer não apenas a produção do código correto, mas também um design que permite que o produto ofereça suporte a várias localidades. Os desenvolvedores e seus gerentes devem estar cientes do nível de esforço e de atenção para os detalhes necessários para criar aplicativos preparados para o mundo, sejam eles entregues como binários únicos prontos para uso em vários mercados diferentes, ou como vários binários específicos de uma localidade. Como desenvolvedor, certifique-se de que seu gerenciamento entenda que a internacionalização envolve mais do que apenas o desenvolvimento de código. A criação de internacionalização no início do seu ciclo de produto economiza tempo, dinheiro e esforço.

A **internacionalização** é a criação de software que se adapta a localidades em todo o mundo. Uma **localidade** é uma coleção de preferências de usuário relacionadas a idiomas. Uma localidade é especificada pelo emparelhamento de um idioma e uma região geográfica. Por exemplo, inglês (Estados Unidos) e inglês (Reino Unido) são duas localidades diferentes, como Inglês (Canadá) e francês (Canadá).

O software internacionalizado tem estes atributos:

-   **A preparação para o mundo** abrange o design e a implementação que separam código independente de localidade de recursos dependentes de localidade e abrange duas áreas principais:
    -   A **globalização** é o processo de desenvolvimento de um núcleo de programa com recursos e design de código que são independentes de idioma ou localidade. Em vez disso, o design dá suporte à entrada, exibição e saída de scripts de idioma com suporte Unicode, bem como a dados relacionados a localidades específicas.
    -   A **possibilidade de localização** é o design da base de código de software e dos recursos, de modo que um programa possa ser localizado, conforme definido abaixo, em diferentes edições de idioma, sem nenhuma alteração no código-fonte. Por exemplo, buffers de cadeia de caracteres no código, e caixas de texto na interface do usuário, devem ser grandes o suficiente para acomodar cadeias de caracteres de texto mais longas em linguagens como alemão ou holandês.
-   **Localização** Isso envolve a tradução e a personalização de um produto para um mercado específico, e trata-se principalmente da criação de arquivos de recursos em vez de escrever código-fonte.

Por exemplo, o uso do NLS (suporte ao idioma nacional) fornecido pela API do Microsoft Win32 é um processo de desenvolvimento de software que dá suporte à preparação para o mundo, ao passo que modificar os elementos da interface do usuário, traduzir texto e padronização de terminologia são etapas de localização geralmente executadas por alguém que é especialista em idioma, como um tradutor. Mesmo quando o seu desenvolvimento de código enfatiza a preparação para o mundo, você precisa entender a localização porque suas decisões de design afetam o trabalho do tradutor.

 

 



