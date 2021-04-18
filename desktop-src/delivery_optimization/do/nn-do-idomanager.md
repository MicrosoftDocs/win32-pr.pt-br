---
title: Interface IDOManager
description: Usado para criar um novo download e para enumerar downloads existentes.
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
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105773918"
---
# <a name="idomanager-interface"></a>Interface IDOManager

A interface **IDOManager** é usada para criar um novo download e para enumerar downloads existentes.

## <a name="methods"></a>Métodos

A interface **IDOManager** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDOManager:: createdownload](./nf-do-idomanager-createdownload.md) | Cria um novo download. |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | Recupera um ponteiro de interface para um objeto enumerador que é usado para enumerar os downloads existentes. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |