---
title: Interface IDODownload
description: Usado para iniciar e gerenciar um download.
keywords:
- Interface IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 356d6ae2e01f91eae94d9d2ff01a39dd49708eb73a7287d8c176b4231654a74a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543813"
---
# <a name="idodownload-interface"></a>Interface IDODownload

A interface **IDODownload** é usada para iniciar e gerenciar um download.

## <a name="methods"></a>Métodos

A interface **IDODownload** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDODownload::Abort](./nf-do-idomanager-createdownload.md) | Anula o download. |
| [IDODownload::Finalize](./nf-do-idodownload-finalize.md) | Finaliza o download. |
| [IDODownload::GetProperty](./nf-do-idodownload-getproperty.md) | Recupera um ponteiro para uma **VARIANT que** contém uma propriedade de download específica. |
| [IDODownload::GetStatus](./nf-do-idodownload-getstatus.md) | Recupera um ponteiro para uma **estrutura DO_DOWNLOAD_STATUS** que reflete o status atual do download. |
| [IDODownload::P ause](./nf-do-idodownload-pause.md) | Pausa o download. |
| [IDODownload::SetProperty](./nf-do-idodownload-setproperty.md) | Define uma propriedade de download. |
| [IDODownload::Start](./nf-do-idodownload-start.md) | Inicia ou retoma um download. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | Do.h |