---
title: DISPIDs padrão
description: Vários DISPIDs padrão foram definidos para a especificação de controles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764542"
---
# <a name="standard-dispids"></a>DISPIDs padrão

Vários DISPIDs padrão foram definidos para a especificação de controles.

## <a name="dispid_mousepointer"></a>\_MOUSEPOINTER DISPID

Propriedade do tipo inteiro.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

A propriedade MousePointer identifica os ícones padrão do mouse.



| Valor         | Descrição                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | Os Forma determinada pelo objeto.<br/>                       |
| 1<br/>  | Seta<br/>                                                           |
| 2<br/>  | Cruzada (ponteiro cruzado)<br/>                                      |
| 3<br/>  | Eu feixe<br/>                                                          |
| 4<br/>  | Ícone (pequeno quadrado dentro de um quadrado)<br/>                             |
| 5<br/>  | Tamanho (seta de quatro pontas apontando para norte, Sul, leste e oeste)<br/> |
| 6<br/>  | Tamanho NE SW (seta dupla apontando para nordeste e sudoeste)<br/>      |
| 7<br/>  | Tamanho N S (seta dupla apontando para norte e Sul)<br/>                |
| 8<br/>  | Tamanho NW, SE<br/>                                                     |
| 9<br/>  | Tamanho E W (seta dupla apontando para o leste e o oeste)<br/>                  |
| 10<br/> | Seta para Cima<br/>                                                        |
| 11<br/> | Ampulheta (espera)<br/>                                                |
| 12<br/> | Sem drop<br/>                                                         |
| 13<br/> | Seta e ampulheta<br/>                                             |
| 14<br/> | Seta e ponto de interrogação<br/>                                         |
| 15<br/> | Dimensionar tudo<br/>                                                        |
| 99<br/> | Ícone personalizado especificado pela propriedade MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>\_MOUSEICON DISPID

Propriedade do tipo imagem.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>\_imagem DISPID

Propriedade do tipo imagem.

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ válida

Usado para determinar se o controle tem dados válidos ou não.

Propriedade do tipo BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>\_paleta de ambiente DISPID \_

Usado para permitir que o controle obtenha o HPAL do contêiner. Se o contêiner fornecer uma paleta de ambiente, essa será a única paleta que pode ser realizada em primeiro plano. Os controles que desejam perceber suas próprias paletas devem fazer isso em segundo plano. Se não houver nenhuma paleta de ambiente fornecida pelo contêiner, o controle ativo poderá perceber sua paleta em primeiro plano. A manipulação de paleta é discutida mais detalhadamente em comportamento de paleta para controles OLE, que está no SDK do ActiveX.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





