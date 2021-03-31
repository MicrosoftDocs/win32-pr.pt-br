---
title: Sinalização fora de banda
description: Os aplicativos de cooperação que compartilham dados comuns usando o diretório podem usar a sinalização fora de banda para evitar a distorção de versão e atualizações parciais.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004907"
---
# <a name="out-of-band-signaling"></a>Sinalização fora de banda

Os aplicativos de cooperação que compartilham dados comuns usando o diretório podem usar a sinalização fora de banda para evitar a distorção de versão e atualizações parciais. Em suma, os aplicativos de cooperação usam um mecanismo separado da replicação de diretório para informar um ao outro sobre as alterações nos dados comuns compartilhados. A sinalização fora de banda é mais eficiente quando usada em combinação com um mecanismo de controle de versão — isso permite que o parceiro detecte a alteração para notificar os parceiros remotos de qual versão dos dados compartilhados aguardar.

Retornando ao exemplo de RPC fornecido na seção "distorção de versão" do [comportamento de replicação no Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), o servidor RPC poderia chamar de volta os clientes conectados para informá-los da mudança para um novo servidor: "vou mover. Aguarde, a replicação levará o novo endereço em breve "para que o cliente possa lidar com o período de transição.

Os aplicativos que exigem políticas idênticas em vigor para se comunicar entre si podem usar a sinalização fora de banda para garantir que uma nova política não seja empregada até que todas as partes envolvidas tenham recebido isso. Por exemplo, se a política de IPsec entre dois computadores for alterada, um agente no computador de origem poderá contatar um agente no computador de destino para negociar o aplicativo da política alterada, com o aplicativo de atraso da máquina de origem até que a máquina de destino tenha recebido a nova política também.

 

 




