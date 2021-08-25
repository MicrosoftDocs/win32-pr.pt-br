---
description: A estrutura de PARSERINFO de PF \_ define um analisador por vez. Na estrutura PF \_ PARSERINFO, um analisador é definido pelas informações sobre o protocolo que o analisador detecta.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Estrutura de PF_PARSERINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533e8dae6a009488998acd3232b062b423553b9df10f14ec97ef9ae2f8c55bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889936"
---
# <a name="pf_parserinfo-structure"></a>Estrutura de PARSERINFO de PF \_

A estrutura de **\_ PARSERINFO de PF** define um analisador por vez. Na estrutura **PF \_ PARSERINFO** , um analisador é definido pelas informações sobre o protocolo que o analisador detecta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**szProtocolName**
</dt> <dd>

Nome do protocolo que o analisador detecta.

</dd> <dt>

**szComment**
</dt> <dd>

Breve descrição do protocolo.

</dd> <dt>

**szHelpFile**
</dt> <dd>

Nome do arquivo de ajuda de protocolo, se houver.

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

Ponteiro para uma estrutura de [ \_ acompanhamento de PF](pf-followset.md) que lista os protocolos que podem preceder o protocolo que a estrutura **PF \_ PARSERINFO** descreve. Monitor de Rede adiciona o protocolo analisador ao [*seguinte conjunto*](f.md) de todos os protocolos no conjunto.

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

Ponteiro para uma estrutura de [ \_ acompanhamento de PF](pf-followset.md) que lista o protocolo que pode seguir o protocolo que a estrutura **PF \_ PARSERINFO** descreve. Monitor de Rede adiciona os protocolos do conjunto ao conjunto de [*acompanhamento*](f.md) do protocolo analisador.

</dd> <dt>

**pWhoHandsOffToMe**
</dt> <dd>

Ponteiro para uma estrutura de [ \_ entrega de PF](pf-handoffset.md) que é descrita no protocolo que a estrutura **de \_ PARSERINFO do PF** descreve. Monitor de Rede adiciona o protocolo analisador aos [*conjuntos de entrega*](h.md) de todos os protocolos no conjunto.

</dd> <dt>

**pWhoDoIHandOffTo**
</dt> <dd>

Ponteiro para uma estrutura de [ \_ entrega do PF](pf-handoffset.md) que lista os protocolos para os quais o protocolo analisador é immãos. Monitor de Rede adiciona os protocolos desse conjunto ao conjunto de [*entrega*](h.md) do protocolo analisador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **\_ PARSERINFO de PF** é usada na estrutura de **\_ PARSERDLLINFO de PF** para fornecer uma descrição de um analisador. Monitor de Rede usa a descrição do analisador para atualizar o arquivo de [*Parser.ini*](p.md) e os arquivos ini dos analisadores que precedem e seguem o protocolo descrito na estrutura **PF \_ PARSERINFO** .

Um conjunto de acompanhamento especifica os protocolos que seguem um protocolo. Monitor de Rede usa um conjunto de acompanhamento quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo. Um conjunto de acompanhamento é armazenado no arquivo de [*Parser.ini*](p.md) . Quando o analisador é instalado pela primeira vez, Monitor de Rede atualiza o conjunto de protocolos do analisador que estão listados em **pWhoCanPrecedeMe** e **pWhoCanFollowMe**.

Um conjunto de entregas especifica os protocolos que seguem um protocolo. O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo. Um conjunto de entregas é armazenado nos arquivos INI de cada analisador. Quando o analisador é instalado pela primeira vez, Monitor de Rede atualiza o conjunto de entrega dos protocolos analisadores listados em **pWhoHandsOffToMe** e **pWhoDoIHandOffTo**.



| Para obter informações sobre                                               | Consulte                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede.        | [Analisadores](parsers.md)                                                       |
| O que os conjuntos de acompanhamento contêm.                                        | [Especificando um conjunto de acompanhamento](specifying-a-follow-set.md)                       |
| O que os conjuntos de entrega contêm.                                       | [Especificando um conjunto de entrega](specifying-a-handoff-set.md)                     |
| Quais pontos de entrada são incluídos na DLL do analisador.                | [Arquitetura de DLL do analisador](parser-dll-architecture.md)                       |
| Como implementar **ParserAutoInstallInfo**  inclui um exemplo. | [Implementando ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> <dt>

[seguir do PF \_](pf-followset.md)
</dt> <dt>

[teleentregador de PF \_](pf-handoffset.md)
</dt> <dt>

[PARSERDLLINFO de PF \_](pf-parserdllinfo.md)
</dt> </dl>

 

 




