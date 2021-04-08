---
description: Além de reconhecer o texto, os reconhecedores podem reconhecer uma classe de objetos relacionados.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Reconhecedores de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922268"
---
# <a name="object-recognizers"></a>Reconhecedores de objetos

Além de reconhecer o texto, os reconhecedores podem reconhecer uma classe de objetos relacionados. Os reconhecedores de objetos reconhecem formas gerais, de acordo com sua finalidade. Os reconhecedores de objetos são usados para reconhecer:

-   Notas musicais
-   Formas geométricas
-   Equações matemáticas
-   Elementos do fluxograma

Normalmente, os objetos que são reconhecidos por tal reconhecedor estão em uma relação espacial bidimensional ou funcional entre si. Por exemplo, dentro das relações complexas em uma equação matemática, um reconhecedor pode retornar resultados diferentes para um limite superior em uma integral definitiva em oposição a um numerador em uma fração.

Devido à natureza muito geral dessas relações, é extremamente difícil definir o conjunto de interfaces que funcionará para cada reconhecedor de objeto.

A tecnologia do Tablet PC fornece uma estrutura básica para os reconhecedores de objetos na biblioteca gerenciada e nas interfaces de automação. No entanto, você deve desenvolver interfaces personalizadas que descrevam relações espaciais complexas entre objetos reconhecidos para cada reconhecedor de objeto. Especificamente, para os reconhecedores de objetos, a plataforma fornece o objeto [**RecognizerContext**](inkrecognizercontext-class.md) básico para associar o objeto de [**tinta**](inkdisp-class.md) ao contexto do reconhecedor e chamar o reconhecedor para executar o reconhecimento.

 

 



