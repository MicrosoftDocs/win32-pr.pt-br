---
title: D1101 identificador desconhecido
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Uma interface não alocada por essa DLL foi passada para ela.
keywords:
- D1101 identificador desconhecido Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 37e84b9e5117732784267374ad9e6618e60d3b4020a6d23863b069b3b8233aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160997"
---
# <a name="d1101-unknown-handle"></a>D1101: identificador desconhecido

Uma interface de interface \[  \] não alocada por essa dll foi passada para ela.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

O endereço da interface.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possíveis causas

Uso de recurso inválido. o recurso criado fora do Direct2D é usado com uma fábrica de Direct2D, ou os recursos criados em uma fábrica foram usados com um recurso criado por outra fábrica.

 

 




