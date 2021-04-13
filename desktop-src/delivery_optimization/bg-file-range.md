---
title: Estrutura de BG_FILE_RANGE (Deliveryoptimization. h)
description: A estrutura de BG_FILE_RANGE identifica um intervalo de bytes para baixar de um arquivo.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Estrutura de BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369833"
---
# <a name="bg_file_range-structure"></a>Estrutura de BG_FILE_RANGE

A estrutura de **BG_FILE_RANGE** identifica um intervalo de bytes para baixar de um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>Membros

<dl> <dt>

**InitialOffset**
</dt> <dd>

Deslocamento de base zero para o início do intervalo de bytes a ser baixado de um arquivo.

</dd> <dt>

**Comprimento**
</dt> <dd>

O comprimento do intervalo, em bytes. Não especifique um comprimento de byte zero. Para indicar que o intervalo se estende até o final do arquivo, especifique **BG_LENGTH_TO_EOF**.

</dd> </dl>

## <a name="remarks"></a>Comentários

O intervalo deve existir no arquivo ou gerar um erro de **DO_E_INVALID_RANGE** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile2::GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





