---
title: Portando funções de iluminação e materiais
description: As funções OpenGL para iluminação e materiais diferem substancialmente das funções IRIS GL. Ao contrário do IRIS GL, o OpenGL tem funções separadas para definir luzes, modelos de luz e materiais.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Portação IRIS GL, iluminação
- portando do IRIS GL, iluminação
- portando para OpenGL do IRIS GL, iluminação
- Portação openGL de IRIS GL, iluminação
- Portação IRIS GL, materiais
- portando do IRIS GL, materiais
- portando para OpenGL do IRIS GL, materiais
- Portação openGL de IRIS GL, materiais
- iluminação
- materiais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45041dde0902f983648c6d258f4c4a8220085d0d8bbeddc6fbdbc970033a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118933026"
---
# <a name="porting-lighting-and-materials-functions"></a>Portando funções de iluminação e materiais

As funções OpenGL para iluminação e materiais diferem substancialmente das funções IRIS GL. Ao contrário do IRIS GL, o OpenGL tem funções separadas para definir luzes, modelos de luz e materiais.

Lembre-se dos seguintes pontos ao portar funções de iluminação e materiais:

-   O OpenGL não tem nenhuma tabela de definições armazenadas. Você pode usar listas de exibição para imitar o mecanismo de def/bind do IRIS GL. Para obter mais informações sobre defs e binds, consulte [Portando Defs, Binds e Sets](porting-defs--binds--and-sets.md).
-   Com o OpenGL, a atenuação é associada a cada fonte de luz, em vez do modelo de iluminação geral.
-   Componentes difusos e especulantes são separados em fontes de luz OpenGL.
-   As fontes de luz OpenGL têm um componente alfa. Ao portar o código IRIS GL, de definir esse componente alfa como 1,0, indicando 100% opaco. Os valores alfa são determinados apenas pelo componente alfa de seus materiais, de modo que os objetos em sua cena terão a mesma aparência que no IRIS GL.

A tabela a seguir lista as funções de materiais e iluminação IRIS GL e suas funções equivalentes do OpenGL.



| Função IRIS GL                 | Função OpenGL                               | Significado                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef(DEFLIGHT,**... **)**    | [glLight](gllight-functions.md)              | Defina uma fonte de luz.                                        |
| **Imdef(DEFLMODEL,**... **)**   | [glLightModel](gllightmodel-functions.md)    | Defina um modelo de iluminação.                                      |
| **Imbind**                       | [**glEnable**](glenable.md) ( GL \_ LIGHT *i*) | Habilitar light *i*.                                             |
| **Imbind**                       | **glEnable**( GL \_ LIGHTING )                  | Habilitar a iluminação.                                              |
| **Imdef(DEFMATERIAL,**... **)** | [**glMaterial**](glmaterial-functions.md)    | Defina um material.                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | Altere o efeito dos comandos de cor enquanto a iluminação está ativa. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Obter parâmetros de material.                                      |



 

A tabela a seguir lista vários parâmetros de material IRIS GL e seus parâmetros equivalentes do OpenGL.



| Índice Imdef  | Parâmetro glMaterial                              | Padrão              | Significado                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| Alfa        | GL \_ DIFUSO                                       |                      | O quarto valor no parâmetro GL \_ DIFFUSE especifica o valor alfa.                      |
| Ambiente      | GL \_ AMBIENT                                       | (0.2, 0.2, 0.2, 1.0) | Cor do ambiente.                                                                                |
| Difusa      | GL \_ DIFUSO                                       | (0.8, 0.8, 0.8, 1.0) | Cor difusa.                                                                                |
| Especular     | GL \_ SPECULAR                                      | (0.0, 0.0, 0.0, 1.0) | Cor emissiva.                                                                               |
| Brilho    | \_GLINESSGL \_ AMBIENTE E \_ \_ DIFUSO<br/> | 0,0                  | Expoente especular. Equivalente a chamar **glMaterial** duas vezes com os mesmos valores.<br/> |
| COLORINDEXES | ÍNDICES \_ DE \_ CORES GL                                |                      | Índices de cores para iluminação ambiente, difusa e especular.                                    |



 

Quando o primeiro parâmetro de **Imdef** é DEFMODEL, a tradução openGL equivalente é a [**função glLightModel.**](gllightmodel-functions.md) A exceção é quando o parâmetro a seguir DEFMODEL é ATTENUATION: a função Equivalente do OpenGL é [**glLight.**](gllight-functions.md)

A tabela a seguir lista os parâmetros de modelo de iluminação equivalentes para IRIS GL e OpenGL.



| Índice Imdef | Parâmetro glLightModel          | Padrão              | Significado                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| Ambiente     | AMBIENTE \_ DO MODELO DE LUZ \_ \_ GL       | (0.2, 0.2, 0.2, 1.0) | Cor do ambiente da cena.                          |
| Atenuação |                                 |                      | Consulte [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | VISUALIZADOR \_ LOCAL DO MODELO DE LUZ \_ \_ \_ GL | GL \_ FALSE            | Visualizador local (**TRUE**) ou infinito (**FALSE**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ TWO \_ SIDE       | GL \_ FALSE            | Use a iluminação de dois lados quando **TRUE.**            |



 

Quando o primeiro parâmetro de **Imdef** é DEFLIGHT, a tradução openGL equivalente é a [**função glLight.**](gllight-functions.md)

A tabela a seguir lista os parâmetros de iluminação equivalentes para IRIS GL e OpenGL.



| Índice Imdef           | Parâmetro glLight                                                                                 | Padrão                                                                             | Significado                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Ambiente               | GL \_ AMBIENTGL \_ DIFUSO<br/> GL \_ SPECULAR<br/>                                         | (0.0, 0.0, 0.0, 1.0) (1.0, 1.0, 1.0, 1.0)<br/> (1.0, 1.0, 1.0, 1.0)<br/> | Intensidade do ambiente. Intensidade difusa.<br/> Intensidade especular.<br/> |
| LCOLOR                | Não há equivalência.                                                                                    |                                                                                     |                                                                                |
| Posição              | POSIÇÃO \_ GL                                                                                      | (0.0, 0.0, 1.0, 0.0)                                                                | Posição da luz.                                                             |
| SPOTDIRECTION         | DIREÇÃO \_ DO SPOT \_ GL                                                                               | (0, 0, 1)                                                                           | Direção do destaque.                                                        |
| Holofotes             | CORTE \_ SPOT DE GL SPOT \_ EXPONENTGL \_ \_<br/>                                                     | 0180<br/>                                                                     | Distribuição de intensidade. Ângulo máximo de propagação da fonte de luz.<br/>        |
| DEFMODEL, ATENUAÇÃO | ATENUAÇÃO \_ LINEAR GL CONSTANT \_ ATTENUATIONGL \_ \_<br/> \_ATENUAÇÃO \_ QUADRÁTICA GL<br/> | (1, 0, 0)                                                                           | Fatores de atenuação.                                                           |



 

 

 





