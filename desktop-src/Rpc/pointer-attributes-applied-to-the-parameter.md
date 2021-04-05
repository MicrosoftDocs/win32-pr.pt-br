---
title: Atributos de ponteiro aplicados ao parâmetro
description: Cada atributo de ponteiro (\ ref \, \ Unique \ e \ PTR \) tem características que afetam a alocação de memória. A tabela a seguir resume essas características.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007995"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Atributos de ponteiro aplicados ao parâmetro

Cada atributo de ponteiro ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] e \[ [PTR](/windows/desktop/Midl/ptr) \] ) tem características que afetam a alocação de memória. A tabela a seguir resume essas características.



| Atributo de ponteiro       | Cliente                                                                                                                                                                                                            | Servidor                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Referência ( \[ **ref** \] ) | O aplicativo cliente deve alocar.                                                                                                                                                                                 | Tratamento especial necessário para ponteiros de nível nontop somente **\[ out \]**. |
| Exclusivo ( \[ **exclusivo** \] ) | Se um parâmetro, o aplicativo cliente deve alocar; se inserido, pode ser nulo. A alteração de NULL para non-null faz com que o stub do cliente seja alocado; alterar de não nulo para nulo pode causar órfãos.<br/> |                                                                     |
| Completo ( \[ **PTR** \] )      | Se um parâmetro, o aplicativo cliente deve alocar; se inserido, pode ser nulo. A alteração de NULL para non-null faz com que o stub do cliente seja alocado; alterar de não nulo para nulo pode causar órfãos.<br/> |                                                                     |



 

O atributo **\[ ref \]** indica que o ponteiro aponta para uma memória válida. Por definição, o aplicativo cliente deve alocar toda a memória que os ponteiros de referência exigem.

O ponteiro exclusivo pode mudar de nulo para não nulo. Se o ponteiro exclusivo mudar de nulo para não nulo, a nova memória será alocada no cliente. Se o ponteiro exclusivo mudar de não nulo para nulo, o órfão poderá resultar. Para obter mais informações, consulte [órfãos de memória](memory-orphaning.md).

 

