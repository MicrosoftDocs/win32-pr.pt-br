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
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084731"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | DODownloadInternal. h |