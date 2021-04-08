---
description: A estrutura STATIONSTATS fornece estatísticas sobre uma estação específica descrita pela captura atual.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Estrutura STATIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010830"
---
# <a name="stationstats-structure"></a>Estrutura STATIONSTATS

A estrutura **STATIONSTATS** fornece estatísticas sobre uma [*estação*](s.md) específica descrita pela captura atual.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a>Membros

<dl> <dt>

**NextStationStats**
</dt> <dd>

Índice da próxima estação registrada na matriz de estrutura **STATIONSTATS** .

</dd> <dt>

**SessionPartnerList**
</dt> <dd>

Índice da lista de parceiros de estação.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Este membro está obsoleto.

</dd> <dt>

**StationAddress**
</dt> <dd>

O endereço MAC da estação.

</dd> <dt>

**Bloco**
</dt> <dd>

Alinhamento de **DWORD** .

</dd> <dt>

**TotalPacketsReceived**
</dt> <dd>

Número total de pacotes enviados para a estação.

</dd> <dt>

**TotalDirectedPacketsSent**
</dt> <dd>

Número total de pacotes direcionados enviados pela estação.

</dd> <dt>

**TotalBroadcastPacketsSent**
</dt> <dd>

Número total de pacotes direcionados à difusão (endereço MAC FF FF FF FF TT FF) enviados pela estação.

</dd> <dt>

**TotalMulticastPacketsSent**
</dt> <dd>

Número total de pacotes multicast (conjunto de bits do grupo no endereço de destino) enviados pela estação.

</dd> <dt>

**TotalBytesReceived**
</dt> <dd>

Número total de bytes enviados à estação.

</dd> <dt>

**TotalBytesSent**
</dt> <dd>

Número total de bytes enviados pela estação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Monitor de Rede armazena informações de sessão e de estação em duas matrizes associadas. cujos elementos são estruturas [SESSIONSTATS](sessionstats.md) e **STATIONSTATS** , respectivamente. Os membros dessas estruturas podem ser usados para navegar entre eles. Por exemplo, para mover para a próxima estação, use **NextStationStats**. Para saltar para a lista de parceiros de sessão na matriz SESSIONSTATS, use o índice fornecido em **SessionPartnerList**.

> [!Note]  
> A matriz **STATIONSTATS** contém um elemento para cada estação usada durante a captura atual. O algoritmo que Monitor de Rede usa para adicionar elementos a essa matriz baseia-se na maneira mais eficiente de registrar informações enquanto a captura está em andamento. Consequentemente, a próxima estação nem sempre é o próximo elemento na matriz.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




