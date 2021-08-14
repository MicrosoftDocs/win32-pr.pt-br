---
title: Interface IDODownloadInternal
description: Usado para obter ou definir propriedades de download estendido.
keywords:
- Interface IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: de9079f7b87822ce950bc4e6c3ece6457e62775c32f7c0d51e76959332298bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755776"
---
# <a name="idodownloadinternal-interface"></a>Interface IDODownloadInternal

> [!IMPORTANT]
> A interface **IDODownloadInternal** foi preterida. Em vez disso, use a interface [IDODownload](../do/nn-do-idodownload.md) .

A interface **IDODownloadInternal** é usada para obter ou definir propriedades de download estendido.

## <a name="methods"></a>Métodos

A interface **IDODownloadInternal** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Recupera um ponteiro para uma **variante** que contém um valor de propriedade de download estendido específico. |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Define uma propriedade de download estendido. O método aceita um ponteiro para uma **variante** que contém um valor de propriedade específico a ser aplicado ao download. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | DODownloadInternal. h |