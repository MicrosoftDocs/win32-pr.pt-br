---
description: Representa informações do gatilho de teste.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura ExperimentTrigger
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825728"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>Estrutura ExperimentTrigger

Representa informações do gatilho de teste.

## <a name="syntax"></a>Sintaxe


```C++
} ExperimentTrigger;
```

## <a name="members"></a>Membros

**tipo**  
O tipo de experimento (captura) disparado.

**chave**  
Quando Type é igual a EXPERIMENTTRIGGERTYPE:: KEY, a chave usada para disparar a captura.

**frameNumber**  
Quando Type é igual a EXPERIMENTTRIGGERTYPE:: FRAMENUMBER, o número do quadro que irá disparar a captura.

**captureCount**  
O número de quadros sequenciais a serem capturados.

**actionIID**  
A ID do evento de ação (captura de tela, captura de quadros, etc.)

**actionPlayload**  
Um ponteiro para a carga do evento de ação.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



