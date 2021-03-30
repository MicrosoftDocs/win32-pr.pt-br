---
title: Autenticação de Usuário
description: O próprio protocolo de autenticação pode autenticar o usuário por meio de EAP protegido (PEAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103638925"
---
# <a name="user-authentication"></a>Autenticação de Usuário

O próprio protocolo de autenticação pode autenticar o usuário por meio de EAP protegido (PEAP). Também há dois provedores de autenticação internos no sistema operacional: autenticação de domínio do Windows (acessada por meio de serviços de diretório) e RADIUS (Remote Access dial-in User Service).

No caso em que o RADIUS é o provedor de autenticação, o plug-in EAP é instalado no servidor RADIUS, e não no servidor AP (ponto de acesso sem fio), como um servidor RAS. O servidor AP passa pacotes EAP diretamente do cliente para o serviço de autenticação no servidor RADIUS. O servidor AP não processa nenhuma das informações nos pacotes EAP, mas deve aceitar as chaves de criptografia geradas pelo PEAP do lado do servidor (256 bits) para criar a conexão segura.

 

 




