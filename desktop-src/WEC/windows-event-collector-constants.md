---
title: Windows Constantes do Coletor de Eventos (Evcoll.h)
description: O Windows SDK do Coletor de Eventos contém as constantes a seguir.
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
ms.openlocfilehash: 8d168ecb16c293c524c4dffcb16aee7db2924e23219e42d402939ab26b4bbecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005976"
---
# <a name="windows-event-collector-constants"></a>Windows Constantes do Coletor de Eventos

O Windows SDK do Coletor de Eventos contém as constantes a seguir.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**MÁSCARA \_ DE TIPO VARIANTE DE \_ \_ EC**
</dt> <dd> <dl> <dt>

0x7f
</dt> <dt>



Usado para mascarar o bit da matriz da **propriedade Type** de uma [**EC \_ VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) para extrair o tipo do valor de variante.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**MATRIZ \_ DE TIPO VARIANTE DE \_ \_ EC**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Quando esse bit é definido na propriedade **Type** de uma [**EC \_ VARIANT,**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)a variante contém um ponteiro para uma matriz de valores, em vez do próprio valor.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**ACESSO \_ DE LEITURA DA \_ EC**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Permissão de controle de acesso de leitura que permite que as informações sejam lidas do coletor de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**ACESSO \_ DE GRAVAÇÃO DE \_ EC**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Permissão de controle de acesso de gravação que permite que as informações sejam escritas no coletor de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ OPEN \_ ALWAYS**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Abre uma assinatura existente ou cria a assinatura se ela não existir. Usado pelo [**método EcOpenSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ CREATE \_ NEW**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Um sinalizador passado para a [**função EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) especificando que uma nova assinatura deve ser criada.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ OPEN \_ EXISTENTE**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Um sinalizador passado para a [**função EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) especificando que uma assinatura existente deve ser aberta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Evcoll.h</dt> </dl> |



 

 





