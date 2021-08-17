---
title: Diretrizes de hardware periférico
description: Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo força a desabilitação do redirecionamento do dispositivo usando uma política de sistema ou política de grupo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0cbe39010eaa59d4207ad28722521793fe33a04f9d06591f21f8ac381940235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756265"
---
# <a name="peripheral-hardware-guidelines"></a>Diretrizes de hardware periférico

Para um Conexão de Área de Trabalho Remota (RDC), o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) é o computador local. Consequentemente, dispositivos como unidades de disco e impressoras anexadas ao servidor aparecem como dispositivos locais para um cliente. Por outro lado, as unidades e impressoras anexadas a um terminal do cliente podem parecer dispositivos remotos, dependendo das opções selecionadas para a conexão, do servidor usado e da versão do software cliente usado.

Embora a versão inicial do Serviços de Área de Trabalho Remota não desse suporte a aplicativos que enviam a saída diretamente para portas seriais, paralelas e de som anexadas ao terminal do cliente, as versões atuais permitem que esses dispositivos apareçam como dispositivos locais para aplicativos em execução na sessão Serviços de Área de Trabalho Remota.

Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo força a desabilitação do redirecionamento do dispositivo usando uma política de sistema ou política de grupo.

 

 




