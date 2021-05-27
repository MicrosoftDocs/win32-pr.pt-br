---
title: D1104 Possível Vazamento
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: A fábrica foi liberada, mas a interface criada a partir dela ainda está a vivo. Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode ser um indicativo de uma perda de memória.
keywords:
- D1104 Possível Vazamento Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548671"
---
# <a name="d1104-possible-leak"></a>D1104: Possível vazamento

A fábrica \[ *de fábrica* \] foi lançada, mas a interface de \[ *interface* criada a partir dela \] ainda está a vivo. Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode ser um indicativo de uma perda de memória.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*Fábrica*
</dt> <dd>

O endereço da fábrica que foi liberada.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interface*
</dt> <dd>

O endereço da interface que foi criada na *fábrica.*

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Nível de erro | Informações |



 

## <a name="possible-causes"></a>Possíveis causas

A fábrica foi liberada, mas a interface criada a partir dela ainda está a vivo.

 

 




