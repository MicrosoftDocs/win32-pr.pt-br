---
title: Seleção do mecanismo de fala
description: Seleção do mecanismo de fala
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822549"
---
# <a name="speech-engine-selection"></a>Seleção do mecanismo de fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A configuração de ID de idioma de um caractere determina seu idioma de entrada de fala padrão; O Microsoft Agent solicita SAPI para um mecanismo instalado que corresponda a esse idioma. Se um aplicativo cliente não especificar uma preferência de idioma, o Microsoft Agent tentará localizar um mecanismo de reconhecimento de fala que corresponda à ID de idioma padrão do usuário (usando a ID de idioma principal e, em seguida, a ID de idioma secundária). Se nenhum mecanismo estiver disponível correspondendo a esse idioma, a fala será desabilitada para esse caractere.

Você também pode solicitar um mecanismo de reconhecimento de fala específico especificando sua ID de modo (usando a propriedade [**SRModeID**](srmodeid-property.md) de caracteres). No entanto, se a ID de idioma para essa ID de modo não corresponder à configuração de idioma do cliente, a chamada falhará (gerará um erro no controle). O mecanismo de reconhecimento de fala permanecerá o último mecanismo definido com êxito pelo cliente, ou se nenhum, o mecanismo que corresponde à ID de idioma atual do sistema. Se ainda não houver correspondência, a entrada de fala não estará disponível para esse cliente.

O Microsoft Agent carrega automaticamente um mecanismo de reconhecimento de fala quando a entrada de fala é iniciada por um usuário pressionando a tecla de atalho de escuta ou o cliente de entrada-ativo chama o método [**Listen**](listen-method.md) . No entanto, um mecanismo também pode ser carregado ao definir ou consultar sua ID de modo, configurar ou consultar as propriedades da janela de comandos de voz, consultar [**SRStatus**](srstatus-property.md)ou quando a fala estiver habilitada e o usuário exibir a página de entrada de fala das opções de caractere avançado. No entanto, o Microsoft Agent só mantém carregado os mecanismos de fala que os clientes estão usando.

 

 




