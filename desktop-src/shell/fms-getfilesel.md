---
description: Contém informações sobre um arquivo selecionado na janela do Gerenciador de arquivos ativo (a janela de diretório ou a janela de resultados da pesquisa).
title: Estrutura de FMS_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920625"
---
# <a name="fms_getfilesel-structure"></a>\_Estrutura GETFILESEL do FMS

Contém informações sobre um arquivo selecionado na janela do Gerenciador de arquivos ativo (a janela de diretório ou a janela de resultados da pesquisa).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>Membros

<dl> <dt>

**ftTime**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

A hora e a data em que o arquivo foi criado.

</dd> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, do arquivo.

</dd> <dt>

**rebatida**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Os atributos do arquivo.

</dd> <dt>

**szName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

O caminho completo finalizado com nulo e o nome de arquivo do arquivo selecionado.

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
</dt> </dl>

 

 




