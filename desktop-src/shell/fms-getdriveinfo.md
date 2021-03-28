---
description: Contém informações sobre a unidade selecionada na janela do Active File Manager (a janela de diretório ou a janela de resultados da pesquisa).
title: Estrutura de FMS_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967937"
---
# <a name="fms_getdriveinfo-structure"></a>\_Estrutura GETdriveinfo do FMS

Contém informações sobre a unidade selecionada na janela do Active File Manager (a janela de diretório ou a janela de resultados da pesquisa).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwTotalSpace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A quantidade total de espaço de armazenamento, em bytes, no disco associado à unidade.

</dd> <dt>

**dwFreeSpace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A quantidade de espaço de armazenamento livre, em bytes, no disco associado à unidade.

</dd> <dt>

**szPath**
</dt> <dd>

Tipo: **TCHAR \[ 260 \]**

</dd> <dd>

o caminho de término nulo do diretório atual.

</dd> <dt>

**szVolume**
</dt> <dd>

Tipo: **TCHAR \[ 14 \]**

</dd> <dd>

O rótulo de volume com terminação nula do disco associado à unidade.

</dd> <dt>

**szShare**
</dt> <dd>

Tipo: **TCHAR \[ 128 \]**

</dd> <dd>

O nome finalizado por nulo do recurso de rede (se a unidade estiver sendo acessada por meio de uma rede).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETdriveinfo**](fm-getdriveinfo.md)
</dt> </dl>

 

 




