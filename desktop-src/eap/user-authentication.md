---
title: Autenticação de Usuário
description: O próprio protocolo de autenticação pode autenticar o usuário por meio do PEAP (EAP Protegido).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3f5d377163f2519d97de847d8d14b5bd96925577a8133988adf8fbf950b283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978366"
---
# <a name="user-authentication"></a>Autenticação de Usuário

O próprio protocolo de autenticação pode autenticar o usuário por meio do PEAP (EAP Protegido). Também há dois provedores de autenticação integrados ao sistema operacional: Windows autenticação de domínio (acessada por meio dos Serviços de Diretório) e RADIUS (Serviço de Usuário Discado de Acesso Remoto).

No caso em que RADIUS é o provedor de autenticação, o Plug-in EAP é instalado no servidor RADIUS em vez de no servidor ap (ponto de acesso) sem fio, como um servidor RAS. O servidor AP passa pacotes EAP diretamente do cliente para o serviço de autenticação no servidor RADIUS. O servidor AP não processa nenhuma das informações nos pacotes EAP, mas deve aceitar as chaves de criptografia geradas por PEAP de força total (256 bits) do lado do servidor para criar a conexão segura.

 

 




