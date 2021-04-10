---
title: D1104 possível perda
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: A fábrica foi liberada, mas a interface criada a partir dela ainda está ativa. Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode indicar um vazamento de memória.
keywords:
- D1104 possível Direct2D de vazamento
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293078"
---
# <a name="d1104-possible-leak"></a>D1104: possível vazamento

A fábrica de fábrica \[  \] foi liberada, mas a \[ *interface* \] de interface criada a partir dela ainda está ativa. Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode indicar um vazamento de memória.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*padrões*
</dt> <dd>

O endereço da fábrica que foi lançada.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

O endereço da interface que foi criada na *fábrica*.

</dd> </dl> 

|             |             |
|-------------|-------------|
| Nível de erro | Informações do |



 

## <a name="possible-causes"></a>Possíveis causas

A fábrica foi liberada, mas a interface criada a partir dela ainda está ativa.

 

 




