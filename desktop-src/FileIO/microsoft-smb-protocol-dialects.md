---
description: Para estabelecer uma conexão entre um cliente e um servidor usando o protocolo SMB da Microsoft, primeiro você deve determinar o dialeto com o nível mais alto de funcionalidade que o cliente e o servidor dão suporte.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialetos do protocolo SMB da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461062"
---
# <a name="microsoft-smb-protocol-dialects"></a>Dialetos do protocolo SMB da Microsoft

A lista de pacotes de mensagens do protocolo SMB da Microsoft cresceu ao longo dos anos para acomodar a funcionalidade crescente do protocolo SMB da Microsoft e, agora, os números nos centenas. Cada estágio de seu crescimento é marcado por um conjunto de pacotes padrão, ou dialeto. Cada dialeto é identificado por uma cadeia de caracteres padrão, como "PC NETWORK PROGRAM 1,0", "MICROSOFT NETWORKs 3,0", "DOS LANMAN 2,1" ou "NT LM 0,12". A primeira cadeia de caracteres identifica o primeiro dialeto de SMB e a última cadeia de caracteres identifica CIFS, o primeiro dialeto do protocolo SMB da Microsoft.

A maioria dos clientes Windows dá suporte a pelo menos seis dialetos diferentes do protocolo SMB da Microsoft, portanto, uma das primeiras etapas para estabelecer uma conexão entre um cliente e um servidor usando o protocolo SMB da Microsoft é determinar o dialeto com o nível mais alto de funcionalidade que o cliente e o servidor têm suporte. Esse processo é conhecido como "negociar o dialeto". As cadeias de caracteres de dialeto mencionadas acima estão incluídas nos pacotes de solicitação de negociação de dialeto e resposta para essa finalidade.

 

 



