---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750dbfee36039337025a03b9f77573a2134f85d15a56d77b2d512482c7bb0e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751450"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>IAgentAudioOutputProperties::GetUsingSoundEffects

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

Recupera um valor que indica se a saída de efeitos de som está habilitada.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*
</dt> <dd>

Endereço de uma variável que recebe **True se a** saída de efeitos de som estiver habilitada no momento e **False** se desabilitada.

</dd> </dl>

Os efeitos de som para a animação de um caractere são atribuídos no Editor de Caracteres do Microsoft Agent. Como essa configuração afeta a saída de efeitos de som para todos os caracteres, somente o usuário pode alterar essa propriedade na folha de propriedades do Microsoft Agent.

 

 




