---
description: A estrutura ADDRESSPAIR constrói um filtro de captura.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Estrutura ADDRESSPAIR (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bbfc455951e76548694415434e0ee4b53893d594b8f0f31419e516bc466ed2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744847"
---
# <a name="addresspair-structure"></a>Estrutura ADDRESSPAIR

A **estrutura ADDRESSPAIR** constrói um filtro de captura.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>Membros

<dl> <dt>

**AddressFlags**
</dt> <dd>

Sinalizadores que descrevem os endereços usados por um filtro de captura. Consulte Comentários para obter mais informações.



| Valor                                                                                                                                                                                                         | Significado                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**SINALIZADORES \_ DE \_ ENDEREÇOS \_ CORRESPONDEREM A DST**</dt> </dl>                 | Corresponde ao endereço de destino.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**SINALIZADORES \_ DE ENDEREÇO \_ \_ CORRESPONDEREM AO SRC**</dt> </dl>                 | Corresponde ao endereço de origem.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**SINALIZADORES \_ DE ENDEREÇO \_ EXCLUÍDOS**</dt> </dl>                     | Excluirá o quadro se esse endereço for encontrado.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**COMPLEMENTO \_ DE \_ GRUPO DST \_ \_ SINALIZADORES DE ENDEREÇO**</dt> </dl> | Corresponde somente ao bit do grupo. Use isso para mensagens de tipo de difusão.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**OS \_ SINALIZADORES DE \_ ENDEREÇO \_ CORRESPONDEREM A AMBOS**</dt> </dl>              | Corresponde aos endereços de origem e de destino.<br/>                     |



 

</dd> <dt>

**NalReserved**
</dt> <dd>

Isso é reservado.

</dd> <dt>

**DstAddress**
</dt> <dd>

Endereço de destino do elemento de par de endereços.

</dd> <dt>

**SrcAddress**
</dt> <dd>

Endereço de origem do elemento de par de endereços.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os sinalizadores do membro **AddressFlags** podem ser combinados. Por exemplo, a configuração a seguir excluirá o quadro se o endereço de origem especificado for detectado.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Para obter mais informações sobre como implementar essa estrutura, consulte [Capturar filtros](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




