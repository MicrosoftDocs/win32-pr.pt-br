---
description: É obsoleto e não deve ser usado.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Estrutura de endereço (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 899d68cb4d041c032ce17ac82866488dfd443071e5368d4ba87950de66a32ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796528"
---
# <a name="address-structure"></a>Estrutura de endereço

A estrutura de **endereço** está obsoleta e não deve ser usada.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo de endereço. Pode conter um dos seguintes valores:

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

Exibição dos dados expressos como um endereço MAC bruto.

</dd> <dt>

**EndereçoIP**
</dt> <dd>

Exibição dos dados expressos como um endereço IP bruto.

</dd> <dt>

**IPXRawAddress**
</dt> <dd>

Exibição dos dados expressos como um Endereço IPX bruto.

</dd> <dt>

**IPXAddress**
</dt> <dd>

Exibição dos dados expressos como um valor de Endereço IPX decodificado.

</dd> <dt>

**VinesIPRawAddress**
</dt> <dd>

Exibição dos dados expressos como um endereço IP de Vines brutos.

</dd> <dt>

**VinesIPAddress**
</dt> <dd>

Exibição dos dados expressos como um endereço IP de Vines decodificados.

</dd> <dt>

**EthernetSrcAddress**
</dt> <dd>

Exibição dos dados expressos como um endereço de origem da Ethernet.

</dd> <dt>

**EthernetDstAddress**
</dt> <dd>

Exibição dos dados expressos como um endereço de destino de Ethernet.

</dd> <dt>

**TokenringSrcAddress**
</dt> <dd>

Uma exibição dos dados como um endereço de origem do token ring.

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

Uma exibição dos dados como um endereço de destino do token ring.

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

Exibição dos dados expressos como um endereço de origem FDDI.

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

Exibição dos dados expressos como um endereço de destino FDDI.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Um conjunto de sinalizadores que modificam as propriedades de endereço.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




