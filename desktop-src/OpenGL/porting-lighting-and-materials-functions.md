---
title: Portando funções de iluminação e materiais
description: As funções OpenGL para iluminação e materiais diferem substancialmente das funções da íris GL. Diferentemente do íris GL, o OpenGL tem funções separadas para definir luzes, modelos leves e materiais.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Portabilidade do íris GL, iluminação
- portando do íris GL, iluminação
- portando para OpenGL do íris GL, iluminação
- Portabilidade OpenGL do íris GL, iluminação
- Portabilidade do íris GL, materiais
- portando do íris GL, materiais
- portando para OpenGL do íris GL, materiais
- Portabilidade OpenGL do íris GL, materiais
- iluminação
- materiais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c775670b7ae49e41fed35c192385c72e72e880b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822828"
---
# <a name="porting-lighting-and-materials-functions"></a>Portando funções de iluminação e materiais

As funções OpenGL para iluminação e materiais diferem substancialmente das funções da íris GL. Diferentemente do íris GL, o OpenGL tem funções separadas para definir luzes, modelos leves e materiais.

Tenha os seguintes pontos em mente ao portar funções de iluminação e materiais:

-   O OpenGL não tem nenhuma tabela de definições armazenadas. Você pode usar listas de exibição para imitar o mecanismo de definição/ligação do íris GL. Para obter mais informações sobre defs e associações, consulte [portando defs, associações e conjuntos](porting-defs--binds--and-sets.md).
-   Com o OpenGL, a atenuação é associada a cada fonte de luz, em vez do modelo de iluminação geral.
-   Os componentes difuso e especular são separados em fontes de luz OpenGL.
-   As fontes de luz OpenGL têm um componente alfa. Ao portar seu código de íris GL, defina este componente alfa como 1,0, indicando 100% opaco. Os valores Alfa são determinados pelo componente alfa somente de seus materiais, de modo que os objetos em sua cena terão a mesma aparência que faziam no íris GL.

A tabela a seguir lista as funções de iluminação e materiais da íris GL e suas funções OpenGL equivalentes.



| Função GL de íris                 | Função OpenGL                               | Significado                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef (deflight**,... **)**    | [glLight](gllight-functions.md)              | Defina uma fonte de luz.                                        |
| **Imdef (DEFLMODEL**,... **)**   | [glLightModel](gllightmodel-functions.md)    | Defina um modelo de iluminação.                                      |
| **Desassociar**                       | [**glEnable**](glenable.md) (GL \_ leve *i*) | Habilitar leve *i*.                                             |
| **Desassociar**                       | **glEnable**( \_ iluminação GL)                  | Habilitar iluminação.                                              |
| **Imdef (DEFMATERIAL**,... **)** | [**glMaterial**](glmaterial-functions.md)    | Defina um material.                                            |
| **Imcolorização**                      | [**glColorMaterial**](glcolormaterial.md)    | Alterar o efeito de comandos de cor enquanto a iluminação estiver ativa. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Obter parâmetros de material.                                      |



 

A tabela a seguir lista vários parâmetros de material do íris GL e seus parâmetros OpenGL equivalentes.



| Índice de Imdef  | parâmetro glMaterial                              | Padrão              | Significado                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| Alfa        | \_difusão GL                                       |                      | O quarto valor no parâmetro de \_ difusão GL especifica o valor alfa.                      |
| TEMPERATURA      | \_ambiente GL                                       | (0,2, 0,2, 0,2, 1,0) | Cor do ambiente.                                                                                |
| DIFUSA      | \_difusão GL                                       | (0,8, 0,8, 0,8, 1,0) | Cor difusa.                                                                                |
| Alce     | \_ESPECULA GL                                      | (0,0, 0,0, 0,0, 1,0) | Cor emissiva.                                                                               |
| LUMINOSIDADE    | GL \_ SHININESSGL \_ ambiente \_ e \_ difuso<br/> | 0.0                  | Expoente especular. Equivalente a chamar **glMaterial** duas vezes com os mesmos valores.<br/> |
| COLORINDEXES | \_índices de cores GL \_                                |                      | Índices de cores para iluminação ambiente, difusa e especular.                                    |



 

Quando o primeiro parâmetro de **Imdef** é DEFMODEL, a conversão OpenGL equivalente é a função [**glLightModel**](gllightmodel-functions.md). A exceção é quando o parâmetro seguinte DEFMODEL é ATENUAtion: a função OpenGL equivalente é [**glLight**](gllight-functions.md).

A tabela a seguir lista os parâmetros de modelo de iluminação equivalentes para íris GL e OpenGL.



| Índice de Imdef | parâmetro glLightModel          | Padrão              | Significado                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| TEMPERATURA     | \_ambiente de \_ modelo \_ Light GL       | (0,2, 0,2, 0,2, 1,0) | Cor do ambiente da cena.                          |
| ATENUAÇÃO |                                 |                      | Consulte [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | \_ \_ Visualizador local de modelo Light \_ GL \_ | GL \_ falso            | Visualizador local (**true**) ou infinito (**false**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ dois \_ lados       | GL \_ falso            | Use a iluminação em dois lados quando **for verdadeiro**.            |



 

Quando o primeiro parâmetro de **Imdef** é deflight, a conversão OpenGL equivalente é a função [**glLight**](gllight-functions.md) .

A tabela a seguir lista os parâmetros de iluminação equivalentes para íris GL e OpenGL.



| Índice de Imdef           | parâmetro glLight                                                                                 | Padrão                                                                             | Significado                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| TEMPERATURA               | GL \_ AMBIENTGL \_ difuso<br/> \_ESPECULA GL<br/>                                         | (0,0, 0,0, 0,0, 1,0) (1,0, 1,0, 1,0, 1,0)<br/> (1,0, 1,0, 1,0, 1,0)<br/> | Intensidade de ambiente. Intensidade difusa.<br/> Intensidade especular.<br/> |
| LCOLOR                | Não há equivalência.                                                                                    |                                                                                     |                                                                                |
| PROPOSTAS              | \_posição GL                                                                                      | (0,0, 0,0, 1,0, 0,0)                                                                | Posição de luz.                                                             |
| SPOTDIRECTION         | \_direção de spot GL \_                                                                               | (0, 0, 1)                                                                           | Direção do Spotlight.                                                        |
| LUZ             | \_corte de \_ spot de EXPONENTGL Spot \_ de GL \_<br/>                                                     | 0180<br/>                                                                     | Distribuição de intensidade. Ângulo de propagação máximo da fonte de luz.<br/>        |
| DEFMODEL, ATENUAÇÃO | \_ \_ atenuação de constante ATTENUATIONGL \_ linear \_ ingl<br/> \_atenuação quadrática do GL \_<br/> | (1, 0, 0)                                                                           | Fatores de atenuação.                                                           |



 

 

 





