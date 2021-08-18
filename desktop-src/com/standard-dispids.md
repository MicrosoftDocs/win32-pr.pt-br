---
title: DISPIDS Padrão
description: Vários dispids padrão foram definidos para a especificação de controles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af35ce4e4cad884b54bb0982037721608364a0249d3be6dd566f3aac766bb1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129778"
---
# <a name="standard-dispids"></a>DISPIDS Padrão

Vários dispids padrão foram definidos para a especificação de controles.

## <a name="dispid_mousepointer"></a>DISPID \_ MOUSEPOINTER

Propriedade do tipo integer.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

A propriedade Mousepointer identifica ícones de mouse padrão.



| Valor         | Descrição                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | (Padrão) Forma determinada pelo objeto .<br/>                       |
| 1<br/>  | Seta<br/>                                                           |
| 2<br/>  | Cruzado (ponteiro de pelos cruzados)<br/>                                      |
| 3<br/>  | I (I)"10<br/>                                                          |
| 4<br/>  | Ícone (quadrado pequeno dentro de um quadrado)<br/>                             |
| 5<br/>  | Tamanho (seta de quatro pontos apontando para norte, sul, leste e oeste)<br/> |
| 6<br/>  | Tamanho da SW do NE (seta dupla apontando para o sudeste e o sudeste)<br/>      |
| 7<br/>  | Tamanho N S (seta dupla apontando para norte e sul)<br/>                |
| 8<br/>  | Tamanho NW, ES<br/>                                                     |
| 9<br/>  | Tamanho E W (seta dupla apontando para leste e oeste)<br/>                  |
| 10<br/> | Seta para Cima<br/>                                                        |
| 11<br/> | Ampulheta (espera)<br/>                                                |
| 12<br/> | Sem soltar<br/>                                                         |
| 13<br/> | Seta e ampulheta<br/>                                             |
| 14<br/> | Seta e ponto de interrogação<br/>                                         |
| 15<br/> | Tamanho de todos<br/>                                                        |
| 99<br/> | Ícone personalizado especificado pela propriedade MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>DISPID \_ MOUSEICON

Propriedade do tipo picture.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>DISPID \_ PICTURE

Propriedade do tipo picture.

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ VALID

Usado para determinar se o controle tem dados válidos ou não.

Propriedade do tipo BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>DISPID \_ AMBIENT \_ PALETTE

Usado para permitir que o controle receba a HPAL do contêiner. Se o contêiner fornece uma paleta de ambiente, essa é a única paleta que pode ser realizada em primeiro plano. Os controles que querem realizar suas próprias paletas devem fazer isso em segundo plano. Se não houver nenhuma paleta de ambiente fornecida pelo contêiner, o controle ativo poderá perceber sua paleta em primeiro plano. A manipulação de paleta é discutida ainda mais em Comportamento da paleta para controles OLE que está no SDK ActiveX dados.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





