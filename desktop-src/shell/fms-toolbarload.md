---
description: Contém informações sobre os botões personalizados a serem adicionados à barra de ferramentas do Gerenciador de arquivos. Os botões são fornecidos por uma DLL de extensão do Gerenciador de arquivos.
title: Estrutura de FMS_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967936"
---
# <a name="fms_toolbarload-structure"></a>\_Estrutura TOOLBARLOAD do FMS

Contém informações sobre os botões personalizados a serem adicionados à barra de ferramentas do Gerenciador de arquivos. Os botões são fornecidos por uma DLL de extensão do Gerenciador de arquivos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, da estrutura. O Gerenciador de arquivos define o tamanho antes de chamar a extensão e verifica o tamanho após o retorno do procedimento de extensão.

</dd> <dt>

**lpButtons**
</dt> <dd>

Tipo: **\_ botão LPEXT**

</dd> <dd>

O endereço de uma matriz de estruturas de [**\_ botão de ext**](ext-button.md) .

</dd> <dt>

**cButtons**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de estruturas de [**\_ botão de ext**](ext-button.md) na matriz apontadas pelo membro **lpButtons** . Esse número é igual ao número de botões e separadores a serem adicionados à barra de ferramentas.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de botões representados pelo bitmap fornecido.

</dd> <dt>

**idBitmap**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O identificador de um recurso de bitmap no arquivo executável para a extensão DLL. O recurso de bitmap contém imagens para o número de botões especificados por **cBitmaps**. O Gerenciador de arquivos carrega o recurso de bitmap e, em seguida, o usa para exibir os botões.

</dd> <dt>

**hBitmap**
</dt> <dd>

Tipo: **HBITMAP**

</dd> <dd>

Um identificador para um bitmap que o Gerenciador de arquivos usará para obter e exibir imagens de botão se **idBitmap** for 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




