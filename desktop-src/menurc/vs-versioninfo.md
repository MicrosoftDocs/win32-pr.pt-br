---
title: Estrutura de VS_VERSIONINFO
description: Representa a organização de dados em um recurso de versão de arquivo. É a estrutura raiz que contém todas as outras estruturas de informações de versão de arquivo.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO de menus de estrutura e outros recursos
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086383"
---
# <a name="vs_versioninfo-structure"></a>Estrutura do VS \_ VERSIONINFO

Representa a organização de dados em um recurso de versão de arquivo. É a estrutura raiz que contém todas as outras estruturas de informações de versão de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, da estrutura do **vs \_ VERSIONINFO** . Esse comprimento não inclui nenhum preenchimento que alinhe quaisquer dados de recursos de versão subsequentes em um limite de 32 bits.

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, do membro de **valor** . Esse valor será zero se não houver nenhum membro de **valor** associado à estrutura de versão atual.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tipo de dados no recurso de versão. Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

A cadeia de caracteres Unicode L " \_ informações de versão vs \_ ".

</dd> <dt>

**Padding1**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Contém tantas palavras zero quantas forem necessárias para alinhar o membro de **valor** em um limite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**

</dd> <dd>

Dados arbitrários associados a esta estrutura do **vs \_ VERSIONINFO** . O membro **wValueLength** especifica o comprimento deste membro; Se **wValueLength** for zero, esse membro não existirá.

</dd> <dt>

**Padding2**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palavras zero quantas forem necessárias para alinhar o membro **filho** em um limite de 32 bits. Esses bytes não estão incluídos no **wValueLength**. Esse membro é opcional.

</dd> <dt>

**Filhos**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Uma matriz de zero ou uma estrutura [**StringFileInfo**](stringfileinfo.md) e nenhuma ou uma estrutura [**VarFileInfo**](varfileinfo.md) que são filhos da estrutura atual do **vs \_ VERSIONINFO** .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





