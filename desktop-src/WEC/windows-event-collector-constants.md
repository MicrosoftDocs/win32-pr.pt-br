---
title: Constantes do coletor de eventos do Windows (Evcoll. h)
description: O SDK do coletor de eventos do Windows contém as seguintes constantes.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644210"
---
# <a name="windows-event-collector-constants"></a>Constantes do coletor de eventos do Windows

O SDK do coletor de eventos do Windows contém as seguintes constantes.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_máscara de \_ tipo de variante do EC \_**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Usado para mascarar o bit da matriz da propriedade **Type** de uma [**\_ variante do EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) para extrair o tipo do valor da variante.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_matriz de \_ tipo de variante do EC \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Quando esse bit é definido na propriedade **Type** de uma [**\_ variante do EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), a variante contém um ponteiro para uma matriz de valores, em vez do próprio valor.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_acesso de leitura do EC \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Permissão de controle de acesso de leitura que permite que informações sejam lidas do coletor de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_acesso de gravação do EC \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Permissão de controle de acesso de gravação que permite que as informações sejam gravadas no coletor de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**\_sempre abrir o EC \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Abre uma assinatura existente ou cria a assinatura se ela não existir. Usado pelo método [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**\_criar \_ novo EC**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Um sinalizador passado para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) especificando que uma nova assinatura deve ser criada.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ Open \_ existente**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Um sinalizador passado para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) especificando que uma assinatura existente deve ser aberta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





