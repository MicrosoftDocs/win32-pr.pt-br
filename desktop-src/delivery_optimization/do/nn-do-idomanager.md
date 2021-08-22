---
title: Interface IDOManager
description: Usado para criar um novo download e enumerar downloads existentes.
keywords:
- Interface IDOManager
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5fff72067c69345a9852718c377b179d16f398c0eb3b84c73ca82c3af1b08a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047084"
---
# <a name="idomanager-interface"></a>Interface IDOManager

A interface **IDOManager** é usada para criar um novo download e enumerar downloads existentes.

## <a name="methods"></a>Métodos

A interface **IDOManager** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDOManager::CreateDownload](./nf-do-idomanager-createdownload.md) | Cria um novo download. |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | Recupera um ponteiro de interface para um objeto enumerador usado para enumerar downloads existentes. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | Do.h |