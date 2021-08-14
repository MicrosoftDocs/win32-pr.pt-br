---
title: Sinalização fora de banda
description: Os aplicativos que compartilham dados comuns usando o diretório podem usar a sinalização fora de banda para evitar distorção de versão e atualizações parciais.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06aab6482c9ad7af8e7c9b505b528b3559adb81f990b4d83681e44f418fadc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185413"
---
# <a name="out-of-band-signaling"></a>Sinalização fora de banda

Os aplicativos que compartilham dados comuns usando o diretório podem usar a sinalização fora de banda para evitar distorção de versão e atualizações parciais. Em termos simples, os aplicativos de distribuição usam um mecanismo separado da replicação de diretório para informar uns aos outros sobre as alterações nos dados comuns compartilhados. A sinalização fora de banda é mais eficaz quando usada em combinação com um mecanismo de controle de versão— isso permite que o parceiro detecte a alteração para notificar os parceiros remotos sobre qual versão dos dados compartilhados aguardar.

Retornando ao exemplo RPC dado na seção "Distorção de Versão" do Comportamento de Replicação no [Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), o servidor RPC pode chamar novamente em clientes conectados para informá-los sobre a mudança para um novo servidor: "Vou me mover. Aguarde, a replicação levará o novo endereço em breve" para que o cliente possa lidar com o período de transição.

Os aplicativos que exigem políticas idênticas para se comunicarem entre si podem usar a sinalização fora de banda para garantir que uma nova política não seja empregada até que todas as partes envolvidas a tenham recebido. Por exemplo, se a política de segurança do protocolo IPsec entre dois máquinas for alterada, um agente no computador de origem poderá contatar um agente no computador de destino para negociar a aplicação da política alterada, com o computador de origem atrasando o aplicativo até que o computador de destino também tenha recebido a nova política.

 

 




