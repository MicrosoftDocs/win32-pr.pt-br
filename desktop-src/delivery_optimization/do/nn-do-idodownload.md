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
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294102"
---
# <a name="idodownload-interface"></a>Interface IDODownload

A interface **IDODownload** é usada para iniciar e gerenciar um download.

## <a name="methods"></a>Métodos

A interface **IDODownload** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDODownload:: Abort](./nf-do-idomanager-createdownload.md) | Anula o download. |
| [IDODownload:: Finalize](./nf-do-idodownload-finalize.md) | Finaliza o download. |
| [IDODownload:: GetProperty](./nf-do-idodownload-getproperty.md) | Recupera um ponteiro para uma **variante** que contém uma propriedade de download específica. |
| [IDODownload:: GetStatus](./nf-do-idodownload-getstatus.md) | Recupera um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que reflete o status atual do download. |
| [IDODownload::P ause](./nf-do-idodownload-pause.md) | Pausa o download. |
| [IDODownload:: SetProperty](./nf-do-idodownload-setproperty.md) | Define uma propriedade de download. |
| [IDODownload:: iniciar](./nf-do-idodownload-start.md) | Inicia ou retoma um download. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |