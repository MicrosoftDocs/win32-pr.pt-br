---
title: Estrutura de BG_FILE_PROGRESS (Deliveryoptimization. h)
description: A estrutura de BG_FILE_PROGRESS fornece informações de progresso relacionadas a arquivos, como o número de bytes transferidos.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Estrutura de BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644991"
---
# <a name="bg_file_progress-structure"></a>Estrutura de BG_FILE_PROGRESS

A estrutura de **BG_FILE_PROGRESS** fornece informações de progresso relacionadas a arquivos, como o número de bytes transferidos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a>Membros

<dl> <dt>

**BytesTotal**
</dt> <dd>

Tamanho do arquivo em bytes. Se o não puder determinar o tamanho do arquivo (por exemplo, se o arquivo ou o servidor não existir), o valor será DO_UNKNOWN_FILE_SIZE.

Se você estiver baixando intervalos de um arquivo, **bytesTotal** refletirá o número total de bytes que você deseja baixar do arquivo.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Número de bytes transferidos.

</dd> <dt>

**Concluído**
</dt> <dd>

Para downloads, o valor será **true** se o arquivo estiver disponível para o usuário; caso contrário, o valor será **false**. Os arquivos estão disponíveis para o usuário depois de chamar o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) . Se o método **Complete** gerar um erro transitório, os arquivos processados antes do erro estarão disponíveis para o usuário; os outros não são. Use o membro **concluído** para determinar se o arquivo está disponível para o usuário quando a **conclusão** falhar.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para determinar se o arquivo foi transferido, você pode:

-   Compare **bytesTransferred** com **bytesTotal**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





