---
description: A estrutura PROPERTYINST define uma instância de uma propriedade em uma parte dos dados reconhecidos. Monitor de Rede aloca e preenche uma estrutura PROPERTYINST quando uma propriedade é anexada à captura.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Estrutura PROPERTYINST (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0d1c338fb8b4e63f03bff422e25578132476f70d932e8f17d5b0c39a0f6416e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778496"
---
# <a name="propertyinst-structure"></a>Estrutura PROPERTYINST

A **estrutura PROPERTYINST** define uma instância de uma propriedade em uma parte dos dados reconhecidos. Monitor de Rede aloca e preenche uma estrutura **PROPERTYINST** quando uma propriedade é anexada à captura.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a>Membros

<dl> <dt>

**lpPropertyInfo**
</dt> <dd>

Ponteiro para a [estrutura PROPERTYINFO](propertyinfo.md) que define a propriedade .

</dd> <dt>

**szPropertyText**
</dt> <dd>

Ponteiro para uma cadeia de caracteres que é exibida no painel de detalhes da Monitor de Rede interface do usuário.

</dd> <dt>

**Lpdata**
</dt> <dd>

Ponteiro para o início dos dados da propriedade. O analisador determina onde os dados da propriedade são iniciados.

</dd> <dt>

**lpByte**
</dt> <dd>

Ponteiro para os **dados BYTE.**

</dd> <dt>

**lpWord**
</dt> <dd>

Ponteiro para os **dados do WORD.**

</dd> <dt>

**lpDword**
</dt> <dd>

Ponteiro para os **dados DWORD.**

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Ponteiro para os [**dados LARGEINT.**](largeint.md)

</dd> <dt>

**lpSysTime**
</dt> <dd>

Ponteiro para os [**dados SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

**lpPropertyInstEx**
</dt> <dd>

Ponteiro para uma [estrutura PROPERTYINSTEX.](propertyinstex.md) O **membro lpPropertyInstEx** é usado somente quando você chama [AttachPropertyInstanceEx](attachpropertyinstanceex.md).

Se **lpPropertyInstEx** for usado, você deverá definir o membro **DataLength** como 0xFFFF.

</dd> <dt>

**Datalength**
</dt> <dd>

Comprimento dos dados para esta instância da propriedade . Se o **membro lpPropertyInstEx** aponta para uma estrutura [**PROPERTYINSTEX,**](propertyinstex.md) você deve definir **DataLength** como 0xFFFF.

</dd> <dt>

**Level**
</dt> <dd>

Informações de nível.

</dd> <dt>

**HelpID**
</dt> <dd>

Identificador de contexto do arquivo de ajuda.

</dd> <dt>

**IFlags**
</dt> <dd>

Sinalizador de condição de erro.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura PROPERTYINST** define uma instância de uma propriedade anexada. O analisador acessa a estrutura **PROPERTYINST** por meio de várias funções auxiliares. Por exemplo, quando a [**função FormatPropertyInstance**](formatpropertyinstance.md) é chamada para formatar os dados de uma propriedade, ela modifica o membro **szPropertyText** da estrutura **PROPERTYINST.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> </dl>

 

