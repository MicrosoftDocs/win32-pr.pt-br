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
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366067"
---
# <a name="idodownloadstatuscallback-interface"></a>Interface IDODownloadStatusCallback

A interface **IDODownloadStatusCallback** é usada para receber notificações sobre um download.

## <a name="methods"></a>Métodos

A interface **IDODownloadStatusCallback** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDODownloadStatusCallback:: onstatuschanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | O chama sua implementação desse método sempre que um status de download for alterado. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |