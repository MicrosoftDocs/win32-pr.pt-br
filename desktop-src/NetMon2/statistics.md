---
description: A estrutura STATISTICS fornece estatísticas para a captura. Algumas dessas estatísticas são geradas por Monitor de Rede, enquanto outras são geradas pela NIC à que o NPP está conectado.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: Estrutura STATISTICS (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATISTICS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 273e6ba9e32337cc65b3dce979d2ff407b904595237b60025e42fc58e57d9823
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778276"
---
# <a name="statistics-structure"></a>Estrutura STATISTICS

A **estrutura STATISTICS** fornece estatísticas para a captura. Algumas dessas estatísticas são geradas por Monitor de Rede, enquanto outras são geradas pela NIC à que o NPP está conectado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STATISTICS {
  __int64 TimeElapsed;
  DWORD   TotalFramesCaptured;
  DWORD   TotalBytesCaptured;
  DWORD   TotalFramesFiltered;
  DWORD   TotalBytesFiltered;
  DWORD   TotalMulticastsFiltered;
  DWORD   TotalBroadcastsFiltered;
  DWORD   TotalFramesSeen;
  DWORD   TotalBytesSeen;
  DWORD   TotalMulticastsReceived;
  DWORD   TotalBroadcastsReceived;
  DWORD   TotalFramesDropped;
  DWORD   TotalFramesDroppedFromBuffer;
  DWORD   MacFramesReceived;
  DWORD   MacCRCErrors;
  __int64 MacBytesReceivedEx;
  DWORD   MacFramesDropped_NoBuffers;
  DWORD   MacMulticastsReceived;
  DWORD   MacBroadcastsReceived;
  DWORD   MacFramesDropped_HwError;
} STATISTICS, *LPSTATISTICS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tempo Decorrido**
</dt> <dd>

Tempo decorrido, em microssegundos.

</dd> <dt>

**TotalFramesCaptured**
</dt> <dd>

Número total de quadros armazenados no momento. Esse número é limitado pelo tamanho do arquivo de captura ou buffer usado para armazenar os quadros.

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

Número total de bytes armazenados no momento. Esse número é limitado pelo tamanho do arquivo de captura ou buffer usado para armazenar os quadros.

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

Número total de quadros que passaram pelo filtro de captura atual. Se um filtro não for usado, esse valor será o mesmo que **TotalFramesSeen.**

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

Número total de quadros que passaram pelo filtro de captura atual. Se um filtro não for usado, esse valor será o mesmo que **TotalBytesSeen.**

</dd> <dt>

**TotalMulticastsFiltered**
</dt> <dd>

Este membro está obsoleto.

</dd> <dt>

**TotalBroadcastsFiltered**
</dt> <dd>

Este membro está obsoleto.

</dd> <dt>

**TotalFramesSeen**
</dt> <dd>

Número total de quadros manipulados pela NIC.

</dd> <dt>

**TotalBytesSeen**
</dt> <dd>

Número total de bytes manipulados pela NIC.

</dd> <dt>

**TotalMulticastsReceived**
</dt> <dd>

Este membro está obsoleto.

</dd> <dt>

**TotalBroadcastsReceived**
</dt> <dd>

Este membro está obsoleto.

</dd> <dt>

**TotalFramesDropped**
</dt> <dd>

Número total de quadros descartados (quadros que passaram pelo filtro, mas não foram salvos).

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

Número de quadros descartados do arquivo de captura ou do buffer. Quando o buffer está cheio, quadros mais antigos são removidos para dar espaço para novos.

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

Número de quadros que a NIC relata ter recebido.

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

Número de erros de CRC relatados pela NIC.

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

Número de bytes que a NIC relata ter recebido.

</dd> <dt>

**MacFramesDropped \_ NoBuffers**
</dt> <dd>

Número de quadros que a NIC relata ter descartado devido à falta de espaço em buffer.

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

Número de multicasts que os relatórios NIC receberam.

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

Número de transmissões que os relatórios da NIC receberam.

</dd> <dt>

**MacFramesDropped \_ HwError**
</dt> <dd>

Número de quadros que a NIC relata como tendo sido descartado devido a erros de hardware.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada para recuperar [*o total de estatísticas*](t.md)e para pausar ou parar a captura atual.

As estatísticas totais não podem ser recuperadas ao usar a interface [NPP I LTD.](iesp.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats::GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[I LTD::P ause](iesp-pause.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> <dt>

[IRIA::Stop](iesp-stop.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> <dt>

[IStatsC::Stop](istats-stop.md)
</dt> </dl>

 

 




