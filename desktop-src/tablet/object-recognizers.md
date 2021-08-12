---
description: Além de reconhecer o texto, os reconhecedores podem reconhecer uma classe de objetos relacionados.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Reconhecedores de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabfd44a5eb126d48df70efd1c391584d12afc94e5e21c714aa0c740a7d486f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449657"
---
# <a name="object-recognizers"></a>Reconhecedores de objetos

Além de reconhecer o texto, os reconhecedores podem reconhecer uma classe de objetos relacionados. Os reconhecedores de objetos reconhecem formas gerais, de acordo com sua finalidade. Os reconhecedores de objetos são usados para reconhecer:

-   Notas musicais
-   Formas geométricas
-   Equações matemáticas
-   elementos do gráfico de Flow

Normalmente, os objetos que são reconhecidos por tal reconhecedor estão em uma relação espacial bidimensional ou funcional entre si. Por exemplo, dentro das relações complexas em uma equação matemática, um reconhecedor pode retornar resultados diferentes para um limite superior em uma integral definitiva em oposição a um numerador em uma fração.

Devido à natureza muito geral dessas relações, é extremamente difícil definir o conjunto de interfaces que funcionará para cada reconhecedor de objeto.

A tecnologia do Tablet PC fornece uma estrutura básica para os reconhecedores de objetos na biblioteca gerenciada e nas interfaces de automação. No entanto, você deve desenvolver interfaces personalizadas que descrevam relações espaciais complexas entre objetos reconhecidos para cada reconhecedor de objeto. Especificamente, para os reconhecedores de objetos, a plataforma fornece o objeto [**RecognizerContext**](inkrecognizercontext-class.md) básico para associar o objeto de [**tinta**](inkdisp-class.md) ao contexto do reconhecedor e chamar o reconhecedor para executar o reconhecimento.

 

 



