---
description: Fornece uma linha no painel superior do Visualizador de Eventos que serve como um contêiner para todos os dados possíveis inseridos em uma coluna.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Estrutura NMCOLUMNVARIANT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748425"
---
# <a name="nmcolumnvariant-structure"></a>Estrutura NMCOLUMNVARIANT

A estrutura **NMCOLUMNVARIANT** fornece uma linha no painel superior do Visualizador de eventos que serve como um contêiner para todos os dados possíveis inseridos em uma coluna.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Um valor do tipo de enumeração [**NMCOLUMNTYPE**](nmcolumntype.md) .

</dd> <dt>

**Valor**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

valor inteiro sem sinal de 8 bits.

</dd> <dt>

**Sint8Val**
</dt> <dd>

valor inteiro com sinal de 8 bits.

</dd> <dt>

**Uint16Val**
</dt> <dd>

valor inteiro sem sinal de 16 bits.

</dd> <dt>

**Sint16Val**
</dt> <dd>

valor inteiro com sinal de 16 bits.

</dd> <dt>

**Uint32Val**
</dt> <dd>

valor inteiro sem sinal de 32 bits.

</dd> <dt>

**Sint32Val**
</dt> <dd>

valor inteiro de 32 bits assinado.

</dd> <dt>

**Float64Val**
</dt> <dd>

valor float de 64 bits.

</dd> <dt>

**FrameVal**
</dt> <dd>

Número do quadro.

</dd> <dt>

**YesNoVal**
</dt> <dd>

Exibe Sim ou não.

</dd> <dt>

**OnOffVal**
</dt> <dd>

Exibe ativado ou desativado.

</dd> <dt>

**TrueFalseVal**
</dt> <dd>

Exibe verdadeiro ou falso.

</dd> <dt>

**MACAddrVal**
</dt> <dd>

Endereço MAC.

</dd> <dt>

**IPXAddrVal**
</dt> <dd>

Endereço IPX.

</dd> <dt>

**IPAddrVal**
</dt> <dd>

Endereço IP.

</dd> <dt>

**VarTimeVal**
</dt> <dd>

Hora da variante. Use **VariantTimetoSystemTime** para converter em hora do sistema.

</dd> <dt>

**pStringVal**
</dt> <dd>

Ponteiro para uma cadeia de caracteres.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NMCOLUMNTYPE**](nmcolumntype.md)
</dt> </dl>

 

 




