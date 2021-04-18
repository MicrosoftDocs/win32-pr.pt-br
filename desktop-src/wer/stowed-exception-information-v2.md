---
title: Estrutura de STOWED_EXCEPTION_INFORMATION_V2
description: Contém informações de exceção dedevidas.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- Estrutura de STOWED_EXCEPTION_INFORMATION_V2 Relatório de Erros do Windows
- Ponteiro de estrutura de PSTOWED_EXCEPTION_INFORMATION_V2 Relatório de Erros do Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782622"
---
# <a name="stowed_exception_information_v2-structure"></a>\_ \_ Estrutura v2 de informações de exceção dedevida \_

Contém informações de exceção dedevidas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a>Membros

<dl> <dt>

**Cabeçalho**
</dt> <dd>

Tipo: **[ **\_ \_ \_ cabeçalho de informações de exceção dedevida**](stowed-exception-information-header.md)**

</dd> <dd>

A estrutura de [**cabeçalho de \_ informações de exceção \_ \_ dedevida**](stowed-exception-information-header.md) que contém informações para esta estrutura pai.

</dd> <dt>

**ResultCode**
</dt> <dd>

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O código [**HRESULT**](/windows/desktop/WinProg/windows-data-types) para a exceção de dedevida.

</dd> <dt>

**ExceptionForm**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um valor de 2 bits que identifica a forma da exceção.



| Valor                                                                                                                                                                                                                                                                  | Significado                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> Em <dt>**DEdevido \_ Formato de exceção \_ \_ Binary**</dt> <dt>0x01</dt> </dl> | Esse valor indica que a forma da exceção é binária.<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> Em <dt>**DEdevido \_ \_ \_ Texto de formulário de exceção**</dt> <dt>0x02</dt> </dl>       | Esse valor indica que a forma da exceção é texto.<br/>   |



 

</dd> <dt>

**ThreadId**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um valor de 30 bits que identifica o thread que gerou a exceção. O valor é deslocado para a direita em 2 bits quando ele é armazenado. Para convertê-lo de volta em uma ID de thread válida, mude o valor para a esquerda por 2. Por exemplo:

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

(*struct sem nome*)
</dt> <dd>

Os membros dessa estrutura aninhada serão válidos somente se o membro **ExceptionForm** estiver definido como **binário de \_ \_ formulário de \_ exceção dedevida**.

<dl> <dt>

**ExceptionAddress**
</dt> <dd>

Tipo: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um ponteiro que contém o endereço de exceção.

</dd> <dt>

**StackTraceWordSize**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamanho, em bytes, de cada palavra no rastreamento de pilha para o qual o membro de **StackTrace** aponta. Esse valor é definido como 4 para plataformas de 32 bits e 8 para plataformas de 64 bits.

</dd> <dt>

**StackTraceWords**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O número de palavras no rastreamento de pilha para o qual o membro de **StackTrace** aponta. O número de palavras é igual ao número de elementos na matriz.

</dd> <dt>

**Pilha**
</dt> <dd>

Tipo: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um ponteiro para um bloco de memória que contém o rastreamento de pilha.

</dd> </dl> </dd> <dt>

(*struct sem nome*)
</dt> <dd>

O membro dessa estrutura aninhada será válido somente se o membro **ExceptionForm** estiver definido como **texto de \_ \_ formulário de \_ exceção dedevido**.

<dl> <dt>

**ErrorText**
</dt> <dd>

Tipo: **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o texto de erro da exceção.

</dd> </dl> </dd> <dt>

**NestedExceptionType**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um valor de 32 bits que especifica o tipo de objeto ao qual o membro **aninhaexception** aponta. Defina o valor com esta macro de definição de tipo de permuta de bytes que assume little-endian:

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

Aqui estão algumas definições de tipo comuns:



| Valor                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> Em <dt>**DEdevido \_ EXCEÇÃO \_ de \_ tipo \_ aninhado None**</dt> <dt>(0x00000000)</dt> </dl>                                  | Esse valor especifica que não há nenhum objeto de exceção aninhado.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> Em <dt>**DEdevido \_ EXCEÇÃO tipo \_ aninhado \_ \_**</dt> exceção <dt> \_ \_ \_ de tipo aninhado do Win32 (' W32E ')</dt> </dl>    | Esse valor especifica que o membro **aninhaexception** aponta para um objeto de [**\_ registro de exceção**](/windows/desktop/api/winnt/ns-winnt-exception_record) .<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> Em <dt>**DEdevido \_ \_ \_ \_ tipo ANINHAdo de exceção**</dt> o <dt> \_ \_ tipo aninhado de exceção dedevida \_ (' Coloque ')</dt> </dl> | Esse valor especifica que o membro **aninhaexception** aponta para outro objeto de exceção dedevida. O outro objeto de exceção envidado pode ser um objeto **v2 de \_ \_ informações \_ de exceção** devidada ou uma versão diferente com um membro de **cabeçalho** válido, ou seja, um membro de **cabeçalho** que contém um cabeçalho de [**\_ \_ informações \_ de exceção dedevida**](stowed-exception-information-header.md)válido.<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> Em <dt>**DEdevido \_ EXCEÇÃO tipo aninhado \_ \_ \_ CLR**</dt> <dt> \_ \_ \_ (' CLR1 ')</dt> </dl>          | Esse valor especifica que o membro **aninhaexception** aponta para um objeto de exceção ' CLR1 '.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> Em <dt>**DEdevido \_ EXCEÇÃO tipo aninhado \_ \_ \_ Leo**</dt> <dt> \_ de exceptioned \_ \_ Type (' LEO1 ')</dt> </dl>          | Esse valor especifica que o membro **aninhaexception** aponta para um objeto de exceção de idioma.<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**Aninhaexception**
</dt> <dd>

Tipo: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um ponteiro para um tipo de exceção aninhada. O tipo de objeto é indicado pelo membro **NestedExceptionType** .

</dd> </dl>

## <a name="remarks"></a>Comentários

Em **DEdevido \_ \_As informações \_ de exceção v2** e o [**cabeçalho de \_ \_ informações \_ de exceção dedevida**](stowed-exception-information-header.md) não são definidas atualmente em um cabeçalho disponível publicamente, portanto, você precisa defini-las no código-fonte antes de usá-las.

A estrutura de informações de exceção devidada **\_ \_ \_ v1** é idêntica a essa estrutura, exceto que ela não contém os membros **NestedExceptionType** e **aninhaexception** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                         |
| parâmetro<br/>                   | <dl> <dt>Nenhuma</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**registro de exceção \_**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**cabeçalho de \_ informações de exceção DEdevida \_ \_**](stowed-exception-information-header.md)
</dt> </dl>

 

