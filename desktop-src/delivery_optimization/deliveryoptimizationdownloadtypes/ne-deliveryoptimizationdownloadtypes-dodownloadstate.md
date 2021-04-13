---
title: Enumeração dodownloadstate
description: Especifica a ID do estado de download atual, que faz parte da estrutura de **DO_DOWNLOAD_STATUS** .
keywords:
- Enumeração dodownloadstate, dodownloadstate
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499630"
---
# <a name="dodownloadstate-enumeration"></a>Enumeração dodownloadstate

A enumeração **Dodownloadstate** especifica a ID do estado de download atual, que faz parte da estrutura de **DO_DOWNLOAD_STATUS** .

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a>Constantes

| Requisito | Valor |
|-|-|
| DODownloadState_Created | O objeto de download foi criado, mas ainda não foi iniciado. |
| DODownloadState_Transferring | O download está em andamento. |
| DODownloadState_Transferred | O download é transferido e pode ser iniciado novamente baixando outra parte do arquivo. |
| DODownloadState_Finalized | O download foi finalizado e não pode ser iniciado novamente. |
| DODownloadState_Aborted | O download foi anulado. |
| DODownloadState_Paused | O download foi pausado sob demanda ou devido a um erro transitório. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | DeliveryOptimizationDownloadTypes. h |
