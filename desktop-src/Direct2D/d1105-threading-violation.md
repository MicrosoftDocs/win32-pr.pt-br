---
title: Violação de Threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Uma interface segmentada de aluguel foi acessada simultaneamente de vários threads.
keywords:
- D1105 de violação de Threading Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105749171"
---
# <a name="d1105-threading-violation"></a>D1105: violação de Threading

Uma interface de interface threadada \[  \] de aluguel foi acessada simultaneamente de vários threads.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

O endereço da interface que foi acessada por vários threads.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possíveis causas

Usando uma instância de objeto da mesma fábrica de thread único de dois threads diferentes.

 

 




