---
title: Diretrizes de hardware periférico
description: Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo force a desabilitação do redirecionamento do dispositivo usando uma política do sistema ou uma política de grupo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364240"
---
# <a name="peripheral-hardware-guidelines"></a>Diretrizes de hardware periférico

Para um cliente Conexão de Área de Trabalho Remota (RDC), o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) é o computador local. Consequentemente, dispositivos como unidades de disco e impressoras conectadas ao servidor aparecem como dispositivos locais para um cliente. Por outro lado, as unidades e impressoras anexadas a um terminal de cliente podem parecer dispositivos remotos, dependendo das opções selecionadas para a conexão, do servidor usado e da versão do software cliente usado.

Embora a versão inicial do Serviços de Área de Trabalho Remota não tivesse suporte a aplicativos que enviam a saída diretamente para portas seriais, paralelas e de som anexadas ao terminal do cliente, as versões atuais permitem que esses dispositivos apareçam como dispositivos locais em aplicativos em execução na sessão de Serviços de Área de Trabalho Remota.

Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo force a desabilitação do redirecionamento do dispositivo usando uma política do sistema ou uma política de grupo.

 

 




