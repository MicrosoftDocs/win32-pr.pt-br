---
title: BG_FILE_PROGRESS (Deliveryoptimization.h)
description: A BG_FILE_PROGRESS fornece informações de progresso relacionadas ao arquivo, como o número de bytes transferidos.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS estrutura
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
ms.openlocfilehash: dd0bec0f21fb652ccc5c8d543f04816468fff9bc28db74a68a1d05c072a895a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047244"
---
# <a name="bg_file_progress-structure"></a>BG_FILE_PROGRESS estrutura

A **BG_FILE_PROGRESS** fornece informações de progresso relacionadas ao arquivo, como o número de bytes transferidos.

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

Tamanho do arquivo em bytes. Se DO não puder determinar o tamanho do arquivo (por exemplo, se o arquivo ou o servidor não existir), o valor será DO_UNKNOWN_FILE_SIZE.

Se você estiver baixando intervalos de um arquivo, **BytesTotal** refletirá o número total de bytes que você deseja baixar do arquivo.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Número de bytes transferidos.

</dd> <dt>

**Concluído**
</dt> <dd>

Para downloads, o valor será **TRUE** se o arquivo estiver disponível para o usuário; caso contrário, o valor será **FALSE.** Os arquivos ficam disponíveis para o usuário depois de chamar o [**método IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md) Se o **método Complete** gerar um erro transitório, esses arquivos processados antes do erro ocorrer estarão disponíveis para o usuário; os outros não são. Use o **membro Concluído** para determinar se o arquivo está disponível para o usuário quando **Concluir** falhar.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para determinar se DO transferiu o arquivo, você pode:

-   Compare **BytesTransferred com** **BytesTotal.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





