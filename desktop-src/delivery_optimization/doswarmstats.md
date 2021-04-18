---
title: Estrutura DOSwarmStats (Deliveryoptimization. h)
description: Contém campos para baixar e carregar estatísticas para um arquivo.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Estrutura DOSwarmStats
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105793934"
---
# <a name="doswarmstats-structure"></a>Estrutura DOSwarmStats

Contém campos para baixar e carregar estatísticas para um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a>Membros

<dl> <dt>

**fileId**
</dt> <dd>

Cadeia de caracteres terminada em nulo que foi especificada com a chamada **AddFileWithRanges** .

</dd> <dt>

**sourceURL**
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo no servidor (por exemplo, https:// &lt; Server &gt; / &lt; Path &gt; /File.ext).

</dd> <dt>

**Tamanho**
</dt> <dd>

Tamanho do arquivo em bytes.

</dd> <dt>

**totalBytesDownloaded**
</dt> <dd>

Número total de bytes transferidos.

</dd> <dt>

**bytesFromLanPeers**
</dt> <dd>

Número de bytes transferidos de pares de LAN.

</dd> <dt>

**bytesFromGroupPeers**
</dt> <dd>

Número de bytes transferidos de pares de grupo.

</dd> <dt>

**bytesFromInternetPeers**
</dt> <dd>

Número de bytes transferidos de pares da Internet.

</dd> <dt>

**bytesFromHttp**
</dt> <dd>

Número de bytes transferidos do http.

</dd> <dt>

**bytesFromDoinc**
</dt> <dd>

Somente para uso interno.

</dd> <dt>

**bytesToLanPeers**
</dt> <dd>

Número de bytes transferidos para pares de LAN.

</dd> <dt>

**bytesToGroupPeers**
</dt> <dd>

Número de bytes transferidos para pares de grupos.

</dd> <dt>

**bytesToInternetPeers**
</dt> <dd>

Número de bytes transferidos para pares da Internet.

</dd> <dt>

**httpConnectionCount**
</dt> <dd>

Contagem de conexões http.

</dd> <dt>

**doincConnectionCount**
</dt> <dd>

Somente para uso interno.

</dd> <dt>

**lanConnectionCount**
</dt> <dd>

Contagem de conexões de LAN.

</dd> <dt>

**groupConnectionCount**
</dt> <dd>

Contagem de conexões de grupo.

</dd> <dt>

**internetConnectionCount**
</dt> <dd>

Contagem de conexões com a Internet.

</dd> <dt>

**downloadDuration**
</dt> <dd>

Duração da transferência de arquivo em milissegundos.

</dd> <dt>

**downloadMode**
</dt> <dd>

O modo de download usado, consulte [**downloadmode**](downloadmode.md).

</dd> <dt>

**status**
</dt> <dd>

O status de uma transferência de arquivo, consulte [**SwarmStatus**](swarmstatus.md).

</dd> <dt>

**IsBackground**
</dt> <dd>

True, se esta for uma transferência em segundo plano.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





