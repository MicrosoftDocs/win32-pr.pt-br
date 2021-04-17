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
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105755749"
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

Uso de recurso inválido. O recurso criado fora do Direct2D é usado com uma fábrica do Direct2D ou os recursos criados em uma fábrica foram usados com um recurso criado por outra fábrica.

 

 




