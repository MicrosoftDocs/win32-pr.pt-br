---
description: A mensagem de DEVSPECIFIC de linha TAPI \_ é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: Mensagem de LINE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810461"
---
# <a name="line_devspecific-message"></a>Mensagem de DEVSPECIFIC de linha \_

A mensagem **de \_ DEVSPECIFIC de linha** TAPI é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.


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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem \_ DEVSPECIFIC de linha** é usada por um provedor de serviços em conjunto com a função [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) . Seu significado é específico ao dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




