---
title: Atributos de ponteiro aplicados ao parâmetro
description: Cada atributo de ponteiro (\ ref\ , \ unique\ e \ ptr\ ) tem características que afetam a alocação de memória. A tabela a seguir resume essas características.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcc6649dc663d7b029a7d7f345719330719d2eb19b6b7a63fa02797c17df16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927491"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Atributos de ponteiro aplicados ao parâmetro

Cada atributo de ponteiro ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [exclusivo](/windows/desktop/Midl/unique) \] e \[ [ptr](/windows/desktop/Midl/ptr)) tem \] características que afetam a alocação de memória. A tabela a seguir resume essas características.



| Atributo de ponteiro       | Cliente                                                                                                                                                                                                            | Servidor                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Referência ( \[ **ref** \] ) | O aplicativo cliente deve alocar.                                                                                                                                                                                 | Manipulação especial necessária **\[ para ponteiros \]** de nível out -only nontop. |
| Exclusivo ( \[ **exclusivo** \] ) | Se um parâmetro for , o aplicativo cliente deverá alocar; se inserido, pode ser nulo. Alterar de nulo para não nulo faz com que o stub do cliente seja alocado; alterar de não nulo para nulo pode causar órfãos.<br/> |                                                                     |
| Full ( \[ **ptr** \] )      | Se um parâmetro for , o aplicativo cliente deverá alocar; se inserido, pode ser nulo. Alterar de nulo para não nulo faz com que o stub do cliente seja alocado; alterar de não nulo para nulo pode causar órfãos.<br/> |                                                                     |



 

O **\[ atributo ref \]** indica que o ponteiro aponta para a memória válida. Por definição, o aplicativo cliente deve alocar toda a memória que os ponteiros de referência exigem.

O ponteiro exclusivo pode mudar de nulo para não nulo. Se o ponteiro exclusivo mudar de nulo para não nulo, a nova memória será alocada no cliente. Se o ponteiro exclusivo mudar de não nulo para nulo, o órfão poderá resultar. Para obter mais informações, consulte [Órfão de memória.](memory-orphaning.md)

 

