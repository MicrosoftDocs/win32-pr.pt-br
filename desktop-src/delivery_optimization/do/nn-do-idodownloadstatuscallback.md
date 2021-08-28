---
title: Interface IDODownloadStatusCallback
description: Usado para receber notificações sobre um download.
keywords:
- Interface IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: d91ff44e3b4f4247983ec81d53257347c8bcfa523f85855dcd0d37074f4b38fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498946"
---
# <a name="idodownloadstatuscallback-interface"></a>Interface IDODownloadStatusCallback

A interface **IDODownloadStatusCallback** é usada para receber notificações sobre um download.

## <a name="methods"></a>Métodos

A interface **IDODownloadStatusCallback** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | O DO chama sua implementação desse método sempre que um status de download é alterado. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | Do.h |