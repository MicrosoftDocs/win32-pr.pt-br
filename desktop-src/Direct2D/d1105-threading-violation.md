---
title: Violação de threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Uma interface threaded de aluguel foi acessada simultaneamente de vários threads.
keywords:
- Violação de threading D1105 Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 12e7321fd40437bc262439c6ddb319a0aa6dba145d05d3feebba2813c904bbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537966"
---
# <a name="d1105-threading-violation"></a>D1105: Violação de threading

Uma interface de interface threaded \[ *de aluguel* \] foi acessada simultaneamente de vários threads.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interface*
</dt> <dd>

O endereço da interface que foi acessada por vários threads.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possíveis causas

Usando uma instância de objeto da mesma fábrica de thread único de dois threads diferentes.

 

 




