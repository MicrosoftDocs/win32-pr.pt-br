---
description: Contém uma lista de identificadores básicos do conjunto de serviços (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Estrutura de DOT11_BSSID_LIST (Windot11. h)
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
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813139"
---
# <a name="dot11_bssid_list-structure"></a>Estrutura da lista de DOT11 \_ BSSID \_

A estrutura de **\_ \_ lista de DOT11 BSSID** contém uma lista de identificadores de BSS (conjunto de serviços básicos).

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

Uma estrutura de [**\_ \_ cabeçalho de objeto NDIS**](ndis-object-header.md) que contém o tipo, a versão e as informações de tamanho de uma estrutura de NDIS. Para a maioria das estruturas de **\_ \_ lista de DOT11 BSSID** , defina o membro de **tipo** como padrão de  tipo de objeto de **NDIS \_ \_ \_**, defina o membro de revisão para a **lista de DOT11 \_ BSSID \_ \_ revisão \_ 1** e defina o membro de **tamanho** como **sizeof (lista de DOT11 \_ BSSID \_ )**.

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

Uma lista de identificadores de BSS. Um identificador de BSS é armazenado como um tipo de [**\_ \_ endereço MAC DOT11**](dot11-mac-address-type.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                       |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Windot11. h (incluir Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_parâmetros de conexão WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




