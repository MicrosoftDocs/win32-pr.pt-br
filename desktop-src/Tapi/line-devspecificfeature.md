---
description: A mensagem de DEVSPECIFICFEATURE de linha TAPI \_ é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Mensagem de LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c1ec56a41d6e57c6e090c9af682cb91c8ffdb891e376fcd9760ff1b51c5d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012526"
---
# <a name="line_devspecificfeature-message"></a>Mensagem de DEVSPECIFICFEATURE de linha \_

A mensagem **de \_ DEVSPECIFICFEATURE de linha** TAPI é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para um dispositivo de linha ou uma chamada. Este é um dispositivo específico.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem \_ DEVSPECIFICFEATURE de linha** é usada por um provedor de serviços em conjunto com a função [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) . Seu significado é específico ao dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




