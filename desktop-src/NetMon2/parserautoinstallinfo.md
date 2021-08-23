---
description: A função de exportação ParserAutoInstallInfo identifica o analisador ou os analisadores localizados em uma DLL. ParserAutoInstallInfo deve ser implementado em todas as DLLs do analisador.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Função de retorno de chamada ParserAutoInstallInfo (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3c6c69b66f3ff92905333a28c5dadfd79290033f0abb68cb2a790f07c6e34412
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063746"
---
# <a name="parserautoinstallinfo-callback-function"></a>Função de retorno de chamada ParserAutoInstallInfo

A **função de exportação ParserAutoInstallInfo** identifica o analisador ou os analisadores localizados em uma DLL. **ParserAutoInstallInfo** deve ser implementado em todas as DLLs do analisador.

## <a name="syntax"></a>Sintaxe


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parâmetros

Essa função de retorno de chamada não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será uma estrutura [ \_ PARSERDLLINFO](pf-parserdllinfo.md) de PF que descreve os analisadores na DLL.

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

Quando Monitor de Rede é carregado pela primeira vez, ele chama **ParserAutoInstallInfo** (se existir) para instalar automaticamente cada analisador e, em seguida, enumerar todas as DLLs do analisador no subdiretório do analisador.

As informações retornadas na estrutura **\_ PARSERDLLINFO** do PF incluem o seguinte:

-   O número de analisadores na DLL (normalmente um).
-   O nome e uma breve descrição do protocolo detectado por cada analisador.
-   Um arquivo de Ajuda opcional para cada protocolo.
-   Os protocolos que precedem cada protocolo.
-   Os protocolos que seguem cada protocolo.

Cada DLL do analisador deve conter um analisador. No entanto, Monitor de Rede permite que você crie uma DLL que contenha mais de um analisador. Por exemplo, tcpip.dll é uma Monitor de Rede DLL com mais de um analisador.



| Para obter informações sobre                                               | Consulte                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| O que são analisadores e como eles funcionam com Monitor de Rede.        | [Analisadores](parsers.md)                                                       |
| Quais pontos de entrada estão incluídos na DLL do analisador.               | [Arquitetura de DLL do analisador](parser-dll-architecture.md)                       |
| Como implementar **o ParserAutoInstallInfo**  inclui um exemplo. | [Implementando ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




