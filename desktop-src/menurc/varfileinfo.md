---
title: Estrutura VarFileInfo
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão que não dependem de uma combinação específica de idioma e página de código.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menus de estrutura VarFileInfo e outros recursos
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddae8f913e199e0a1219e5ec36012ba3a3eaf24708ca6771ec075b497107418e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733387"
---
# <a name="varfileinfo-structure"></a>Estrutura VarFileInfo

Representa a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão que não dependem de uma combinação específica de idioma e página de código.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a>Membros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O comprimento, em bytes, de todo o **bloco VarFileInfo,** incluindo todas as estruturas indicadas pelo **membro** Children.

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Esse membro é sempre igual a zero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O tipo de dados no recurso de versão. Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

A cadeia de caracteres Unicode L"VarFileInfo".

</dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Quantas palavras zero necessárias para alinhar o **membro Children** em um limite de 32 bits.

</dd> <dt>

**Filhos**
</dt> <dd>

Tipo: **[ **Var**](var-str.md)**

</dd> <dd>

Normalmente, contém uma lista de idiomas compatíveis com o aplicativo ou com a DLL.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura de linguagem C verdadeira porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de header fornecidos com o SDK (Software Development Kit) do Windows.

O **membro Children** da estrutura VS [**\_ VERSIONINFO**](vs-versioninfo.md) pode conter zero ou uma estrutura **VarFileInfo.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





