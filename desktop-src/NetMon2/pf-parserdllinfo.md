---
description: A estrutura de PARSERDLLINFO de PF \_ define os analisadores localizados na DLL do analisador.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Estrutura de PF_PARSERDLLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: caaafeb9883ad514366f91f3834354fbd5ac0850400e61594a5307c4533e0960
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962846"
---
# <a name="pf_parserdllinfo-structure"></a>Estrutura de PARSERDLLINFO de PF \_

A estrutura de **\_ PARSERDLLINFO de PF** define os analisadores localizados na DLL do analisador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**nParsers**
</dt> <dd>

Número de analisadores na DLL do analisador.

</dd> <dt>

**ParserInfo**
</dt> <dd>

Matriz de [estruturas \_ PARSERINFO de PF](pf-parserinfo.md) que descrevem cada analisador na DLL do analisador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **\_ PARSERDLLINFO de PF** é retornada pela função de exportação [ParserAutoInstallInfo](parserautoinstallinfo.md) que é implementada na DLL do analisador. A função **ParserAutoInstallInfo** identifica o número de analisadores na dll e usa uma matriz de estruturas [ \_ PARSERINFO de PF](pf-parserinfo.md) para descrever cada analisador.

A estrutura de PARSERDLLINFO de PF \_ deve ser alocada usando **HeapAlloc**.



| Para obter informações sobre                                               | Consulte                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede.        | [Analisadores](parsers.md)                                                      |
| Quais pontos de entrada são incluídos na DLL do analisador.               | [Arquitetura de DLL do analisador](parser-dll-architecture.md)                      |
| Como implementar **ParserAutoInstallInfo**  inclui um exemplo. | [Implementando ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PARSERINFO de PF \_](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




