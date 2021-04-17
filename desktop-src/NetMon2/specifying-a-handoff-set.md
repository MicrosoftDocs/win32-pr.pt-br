---
description: Um conjunto de entregas especifica os protocolos que seguem um protocolo. O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Especificando um conjunto de entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780199"
---
# <a name="specifying-a-handoff-set"></a>Especificando um conjunto de entrega

Um conjunto de entregas especifica os protocolos que seguem um protocolo. O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo.

Por exemplo, o protocolo TCP tem uma propriedade Port que identifica o protocolo que segue o protocolo TCP. Um valor de propriedade de 20 indica que o próximo protocolo é FTP. Um valor de propriedade de 53 indica que o próximo protocolo é DNS. Como a propriedade Port identifica o protocolo a seguir, o analisador TCP pode usar o seguinte conjunto de entrega para obter um identificador para o protocolo que a propriedade Port especifica.

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

Os conjuntos de entrega são armazenados no arquivo INI do analisador. Por exemplo, o conjunto de entrega TCP anterior está localizado no arquivo tcpip.ini. Observe que, se uma DLL do analisador der suporte a vários protocolos, cada analisador que usa um conjunto de entrega terá seu próprio local no arquivo INI.

As informações do conjunto de entrega são especificadas durante a implementação da função [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . O analisador pode especificar os protocolos que precedem o protocolo do analisador e os protocolos que seguem o protocolo do analisador. Monitor de Rede usa todos os protocolos precedidos e adiciona o protocolo analisador às seções do conjunto de acompanhamento a seguir do arquivo INI do analisador — para cada protocolo anterior. Monitor de Rede armazena a lista de protocolos que seguem na seção conjunto de entrega do arquivo INI do analisador.

O Monitor de Rede armazena as informações de conjunto de entrega no arquivo INI do analisador, mas o analisador não acessa os arquivos INI diretamente. Para usar as informações no conjunto de entrega, o analisador chama a função [**Createentregatable**](createhandofftable.md) para criar uma tabela de entrega. Normalmente, a tabela de entrega é criada quando o analisador registra o protocolo. Depois que o protocolo é registrado, o Monitor de Rede cria uma tabela de conjunto de entrega que o analisador pode usar.

O analisador usa seu conjunto de entregas ao reconhecer dados. Primeiro, o analisador lê o valor da propriedade que identifica o próximo protocolo. Em seguida, o analisador chama o [**GetProtocolFromTable**](getprotocolfromtable.md) para obter um identificador para o próximo protocolo. Por fim, o analisador retorna um ponteiro para o identificador no parâmetro *phNextProtocol* de [**RecognizeFrame**](recognizeframe.md).

 

 



