---
description: Um conjunto de entrega especifica os protocolos que seguem um protocolo. O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Especificando um conjunto de entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f3f7d559c83e3c56bc6ea202b3a0e339dbc1b76d93fc2af1b73f5a2c60c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778346"
---
# <a name="specifying-a-handoff-set"></a>Especificando um conjunto de entrega

Um conjunto de entrega especifica os protocolos que seguem um protocolo. O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo.

Por exemplo, o protocolo TCP tem uma propriedade de porta que identifica o protocolo que segue o protocolo TCP. Um valor da propriedade 20 indica que o próximo protocolo é FTP. Um valor da propriedade 53 indica que o próximo protocolo é DNS. Como a propriedade de porta identifica o protocolo a seguir, o analisador TCP pode usar o conjunto de entrega a seguir para obter um identificador para o protocolo especificado pela propriedade de porta.

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

Os conjuntos de entrega são armazenados no arquivo INI do analisador. Por exemplo, o conjunto de entrega TCP anterior está localizado tcpip.ini arquivo. Observe que, se uma DLL do analisador for compatível com vários protocolos, cada analisador que usa um conjunto de entrega terá seu próprio local no arquivo INI.

As informações do conjunto de entrega são especificadas durante a implementação da [**função ParserAutoInstallInfo.**](parserautoinstallinfo.md) O analisador pode especificar os protocolos que precedem o protocolo do analisador e os protocolos que seguem o protocolo do analisador. Monitor de Rede aceita todos os protocolos que precedem e adiciona o protocolo de analisador às seções do conjunto a seguir do arquivo INI do analisador – para cada protocolo anterior. Monitor de Rede armazena a lista de protocolos a seguir na seção conjunto de entrega do arquivo INI do analisador.

Monitor de Rede armazena as informações do conjunto de entrega no arquivo INI do analisador, mas o analisador não acessa os arquivos INI diretamente. Para usar as informações no conjunto de entrega, o analisador chama a [**função CreateHandoffTable**](createhandofftable.md) para criar uma tabela de entrega. Normalmente, a tabela de entrega é criada quando o analisador registra o protocolo. Depois que o protocolo é registrado, Monitor de Rede cria uma tabela de conjunto de entrega que o analisador pode usar.

O analisador usa seu conjunto de entrega ao reconhecer dados. Primeiro, o analisador lê o valor da propriedade que identifica o próximo protocolo. Em seguida, o analisador chama [**GetProtocolFromTable**](getprotocolfromtable.md) para obter um handle para o próximo protocolo. Por fim, o analisador retorna um ponteiro para o ponteiro no *parâmetro phNextProtocol* de [**RecognizeFrame.**](recognizeframe.md)

 

 



