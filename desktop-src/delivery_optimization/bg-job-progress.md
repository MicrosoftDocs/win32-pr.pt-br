---
title: Estrutura de BG_JOB_PROGRESS (Deliveryoptimization. h)
description: A estrutura de BG_JOB_PROGRESS fornece informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos. Para trabalhos de carregamento, o progresso se aplica ao arquivo de carregamento, não ao arquivo de resposta.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Estrutura de BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499631"
---
# <a name="bg_job_progress-structure"></a>Estrutura de BG_JOB_PROGRESS

A estrutura de **BG_JOB_PROGRESS** fornece informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos. Para trabalhos de carregamento, o progresso se aplica ao arquivo de carregamento, não ao arquivo de resposta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a>Membros

<dl> <dt>

**BytesTotal**
</dt> <dd>

Número total de bytes a serem transferidos para todos os arquivos no trabalho. Se o valor for BG_SIZE_UNKNOWN, o tamanho total de todos os arquivos no trabalho não será determinado. Não definirá esse valor se ele não puder determinar o tamanho de um dos arquivos. Por exemplo, se o arquivo ou servidor especificado não existir, o não poderá determinar o tamanho do arquivo.

Se você estiver baixando intervalos do arquivo, o **bytesTotal** incluirá o número total de bytes que você deseja baixar do arquivo.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Número de bytes transferidos.

</dd> <dt>

**FilesTotal**
</dt> <dd>

Número total de arquivos a serem transferidos para esse trabalho.

</dd> <dt>

**FilesTransferred**
</dt> <dd>

Número de arquivos transferidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





