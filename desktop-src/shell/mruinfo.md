---
description: Contém informações que definem uma nova lista MRU (usada mais recentemente). Usado por CreateMRUListW.
title: Estrutura MRUINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 91c0b1a2c10f4ac77afa5f8af2380b3d14ced8f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988760"
---
# <a name="mruinfo-structure"></a>Estrutura MRUINFO

Contém informações que definem uma nova lista MRU (usada mais recentemente). Usado por [**CreateMRUListW**](createmrulist.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho da estrutura.

</dd> <dt>

**Scanner**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

O número máximo de entradas na lista MRU.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Um ou mais dos sinalizadores a seguir.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARY** (0x0001)


</dt> <dd>

Os dados são armazenados no registro como dados binários em vez de dados de cadeia de caracteres.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)


</dt> <dd>

Grave alterações na versão do MRU armazenada no registro somente quando um novo item for adicionado ou os recursos da lista MRU forem liberados da memória. Observe que a versão ativa do MRU na memória é atualizada imediatamente em resposta a qualquer alteração no conteúdo ou na ordenação.

</dd> </dl> </dd> <dt>

**hKey**
</dt> <dd>

Tipo: **HKEY**

</dd> <dd>

Um identificador para a chave aberta no momento ou um dos seguintes valores predefinidos sob os quais armazenar os dados MRU.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**HKEY \_ Current \_ User**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**\_máquina local \_ HKEY**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

Tipo: **LPCTSTR**

</dd> <dd>

A subchave sob a qual armazenar os dados MRU.

</dd> <dt>

**lpfnCompare**
</dt> <dd>

Tipo: **[ **MRUCMPPROC**](mrucmpproc.md)**

</dd> <dd>

Um ponteiro para uma função de comparação de dados opcional que pode ser usada para determinar se um item está presente na lista de MRU. Isso é útil quando a lista MRU foi criada com o **sinalizador \_ binário MRU** . Se esse membro for **nulo**, as funções de comparação de cadeia de caracteres padrão serão usadas; para dados binários, é usada uma comparação de memória direta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não está definida em um arquivo de cabeçalho. Você mesmo deve defini-lo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |
| Nomes Unicode e ANSI<br/>   | **MRUINFOW** (Unicode) e **MRUINFOA** (ANSI)<br/>  |



 

 




