---
description: Contém informações sobre botões personalizados a serem adicionados à barra de ferramentas do Gerenciador de Arquivos. Os botões são fornecidos por uma DLL de extensão do Gerenciador de Arquivos.
title: FMS_TOOLBARLOAD (Wfext.h)
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
ms.openlocfilehash: 719e13e824778ec133ad761d09ccd3bd8f5846ae8cdb36c83ba4f85eca1c2408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224105"
---
# <a name="fms_toolbarload-structure"></a>Estrutura FMS \_ TOOLBARLOAD

Contém informações sobre botões personalizados a serem adicionados à barra de ferramentas do Gerenciador de Arquivos. Os botões são fornecidos por uma DLL de extensão do Gerenciador de Arquivos.

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

**Dwsize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, da estrutura. O Gerenciador de Arquivos define o tamanho antes de chamar a extensão e verifica o tamanho após o retorno do procedimento de extensão.

</dd> <dt>

**lpButtons**
</dt> <dd>

Tipo: **LPEXT \_ BUTTON**

</dd> <dd>

O endereço de uma matriz de [**estruturas EXT \_ BUTTON.**](ext-button.md)

</dd> <dt>

**cButtons**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O número de [**estruturas EXT \_ BUTTON**](ext-button.md) na matriz apontada pelo **membro lpButtons.** Esse número é igual ao número de botões e separadores a adicionar à barra de ferramentas.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O número de botões representados pelo bitmap determinado.

</dd> <dt>

**idBitmap**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O identificador de um recurso de bitmap no arquivo executável para a DLL de extensão. O recurso bitmap contém imagens para o número de botões especificados por **cBitmaps**. O Gerenciador de Arquivos carrega o recurso de bitmap e o usa para exibir os botões.

</dd> <dt>

**Hbitmap**
</dt> <dd>

Tipo: **HBITMAP**

</dd> <dd>

Um handle para um bitmap que o Gerenciador de Arquivos usará para obter e exibir imagens de botão se **idBitmap** for 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BARRA DE FERRAMENTAS \_ FMEVENTLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




