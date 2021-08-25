---
title: Constantes de navegação (OleAcc. h)
description: Este tópico descreve os valores constantes, definidos em OleAcc. h, que indicam a direção espacial (acima, abaixo, esquerda e direita) ou lógica (primeiro filho, última, próxima e anterior) observada quando os clientes usam o IAccessible accNavigate para navegar de um elemento de interface do usuário para outro dentro do mesmo contêiner.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e5c3a39c1b628ea03d1e036265ba7787e15bb70ce550e06b43b8efcd02c14a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998166"
---
# <a name="navigation-constants"></a>Constantes de navegação

Este tópico descreve os valores constantes, definidos em OleAcc. h, que indicam a direção *espacial* (acima, abaixo, esquerda e direita) ou *lógica* (primeiro filho, última, próxima e anterior) observada quando os clientes usam [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para navegar de um elemento de interface do usuário para outro dentro do mesmo contêiner. Para obter mais informações, consulte [Propriedades e métodos de navegação de objetos](object-navigation-properties-and-methods.md).

As constantes de navegação da Microsoft Acessibilidade Ativa são as seguintes:



| Constante                                                                                                                                                                  | Descrição                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**NAVDIR \_ para baixo**</dt> </dl>                   | Navegue até o objeto irmão que está localizado abaixo do objeto inicial.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ FIRSTCHILD**</dt> </dl> | Navegue até o primeiro filho deste objeto. Quando esse sinalizador é usado, o membro **lVal** do parâmetro *VARSTART* deve ser filhaid por \_ conta própria.<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**NAVDIR \_ LASTCHILD**</dt> </dl>    | Navegue até o último filho deste objeto. Ao usar esse sinalizador, o membro **lVal** do parâmetro *VARSTART* deve ser filhaid por \_ conta própria.<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**NAVDIR \_ à esquerda**</dt> </dl>                   | Navegue até o objeto irmão localizado à esquerda do objeto inicial.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ próximo**</dt> </dl>                   | Navegar para o próximo objeto lógico; em geral, é um irmão do objeto inicial.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ anterior**</dt> </dl>       | Navegar até o objeto lógico anterior; em geral, é um irmão do objeto inicial.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR \_ à direita**</dt> </dl>                | Navegue até o objeto irmão que está localizado à direita do objeto inicial.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**NAVDIR \_ up**</dt> </dl>                         | Navegue até o objeto irmão que está localizado acima do objeto inicial.<br/>                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>OleAcc. h</dt> </dl> |



 

 





