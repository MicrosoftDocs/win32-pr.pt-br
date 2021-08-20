---
description: Contém informações sobre a unidade selecionada na janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa).
title: FMS_GETDRIVEINFO (Wfext.h)
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
ms.openlocfilehash: a9225799eeb7d093d706dcb7063f998a2813eab4b2117e2ca776244e4fcf72a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679605"
---
# <a name="fms_getdriveinfo-structure"></a>Estrutura \_ GETDRIVEINFO do FMS

Contém informações sobre a unidade selecionada na janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa).

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

A quantidade de espaço livre de armazenamento, em bytes, no disco associado à unidade.

</dd> <dt>

**Szpath**
</dt> <dd>

Tipo: **TCHAR \[ 260 \]**

</dd> <dd>

o caminho terminado em nulo do diretório atual.

</dd> <dt>

**szVolume**
</dt> <dd>

Tipo: **TCHAR \[ 14 \]**

</dd> <dd>

O rótulo de volume terminado em nulo do disco associado à unidade.

</dd> <dt>

**szShare**
</dt> <dd>

Tipo: **TCHAR \[ 128 \]**

</dd> <dd>

O nome finalizado em nulo do recurso de rede (se a unidade estiver sendo acessada por meio de uma rede).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETDRIVEINFO**](fm-getdriveinfo.md)
</dt> </dl>

 

 




