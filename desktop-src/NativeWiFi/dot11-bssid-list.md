---
description: Contém uma lista de identificadores BSS (conjunto de serviços básicos).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST estrutura (Windot11.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 8abcd2e711d5598c59bb8d4b7aed0f291364f94d04ec17a5fc80de2fd32939eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801386"
---
# <a name="dot11_bssid_list-structure"></a>Estrutura DOT11 \_ BSSID \_ LIST

A **estrutura DOT11 \_ BSSID \_ LIST** contém uma lista de identificadores BSS (conjunto de serviços básicos).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>Membros

<dl> <dt>

**Cabeçalho**
</dt> <dd>

Uma [**estrutura NDIS \_ OBJECT \_ HEADER**](ndis-object-header.md) que contém as informações de tipo, versão e tamanho de uma estrutura NDIS. Para a maioria das estruturas **DOT11 \_ BSSID \_ LIST,** de definido  o membro Type como **NDIS \_ OBJECT TYPE \_ \_ DEFAULT**, de definir o membro de revisão como **DOT11 \_ BSSID \_ LIST REVISION \_ \_ 1** e de definir o membro Size **como sizeof(DOT11 \_ BSSID \_ LIST)**.  

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

O número de entradas nesta estrutura.

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

O número total de entradas com suporte.

</dd> <dt>

**BSSIDs**
</dt> <dd>

Uma lista de identificadores BSS. Um identificador BSS é armazenado como um [**tipo DE \_ \_ ENDEREÇO MAC DOT11.**](dot11-mac-address-type.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP3 \[\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                       |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Windot11.h (inclua Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PARÂMETROS DE \_ CONEXÃO \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




