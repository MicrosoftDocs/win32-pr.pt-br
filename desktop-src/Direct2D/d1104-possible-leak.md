---
title: D1104 possível perda
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: A fábrica foi liberada, mas a interface criada a partir dela ainda está ativa. Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode indicar um vazamento de memória.
keywords:
- D1104 possível perda Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b3c8b49256b3e7009985e9acf6d2b581e2fe436e50325c26f1f7de59cb3b0b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075560"
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

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Nível de erro | Informações |



 

## <a name="possible-causes"></a>Possíveis causas

A fábrica foi liberada, mas a interface criada a partir dela ainda está ativa.

 

 




