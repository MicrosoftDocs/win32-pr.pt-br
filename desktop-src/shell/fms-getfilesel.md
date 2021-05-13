---
description: Contém informações sobre um arquivo selecionado na janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa).
title: FMS_GETFILESEL (Wfext.h)
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
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842217"
---
# <a name="fms_getfilesel-structure"></a>Estrutura \_ GETFILESEL DO FMS

Contém informações sobre um arquivo selecionado na janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa).

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

**Dwsize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, do arquivo.

</dd> <dt>

**bAttr**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Os atributos do arquivo.

</dd> <dt>

**Szname**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

O caminho completo com terminação nula e o nome do arquivo selecionado.

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
</dt> </dl>

 

 




