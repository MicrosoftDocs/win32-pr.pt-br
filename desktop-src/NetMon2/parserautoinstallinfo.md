---
description: A função de exportação ParserAutoInstallInfo identifica o analisador ou analisadores que estão localizados em uma DLL. ParserAutoInstallInfo deve ser implementado em todas as DLLs do analisador.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Função de retorno de chamada ParserAutoInstallInfo (Netmon. h)
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
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296197"
---
# <a name="parserautoinstallinfo-callback-function"></a>Função de retorno de chamada ParserAutoInstallInfo

A função de exportação **ParserAutoInstallInfo** identifica o analisador ou analisadores que estão localizados em uma dll. **ParserAutoInstallInfo** deve ser implementado em todas as DLLs do analisador.

## <a name="syntax"></a>Sintaxe


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parâmetros

Esta função de retorno de chamada não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será uma estrutura de [ \_ PARSERDLLINFO de PF](pf-parserdllinfo.md) que descreve os analisadores na dll.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Quando Monitor de Rede é carregado pela primeira vez, ele chama **ParserAutoInstallInfo** (se existir) para instalar automaticamente cada analisador e, em seguida, enumera todas as DLLs do analisador no subdiretório do analisador.

As informações retornadas na estrutura **PF \_ PARSERDLLINFO** incluem o seguinte:

-   O número de analisadores na DLL (normalmente um).
-   O nome e uma breve descrição do protocolo que cada analisador detecta.
-   Um arquivo de ajuda opcional para cada protocolo.
-   Os protocolos que precedem cada protocolo.
-   Os protocolos que seguem cada protocolo.

Cada DLL do analisador deve conter um analisador. No entanto, Monitor de Rede permite que você crie uma DLL que contenha mais de um analisador. Por exemplo, tcpip.dll é uma DLL Monitor de Rede com mais de um analisador.



| Para obter informações sobre                                               | Consulte                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede.        | [Analisadores](parsers.md)                                                       |
| Quais pontos de entrada são incluídos na DLL do analisador.               | [Arquitetura de DLL do analisador](parser-dll-architecture.md)                       |
| Como implementar **ParserAutoInstallInfo**  inclui um exemplo. | [Implementando ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PARSERDLLINFO de PF \_](pf-parserdllinfo.md)
</dt> </dl>

 

 




