---
title: Informações de autenticação do usuário
description: O serviço de Gerenciador de Conexões remoto no computador cliente envia um nome de usuário e uma senha para o servidor RAS no computador remoto.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f347cd9f42106619f2558bdcbc677c961b4fae749912c92dd32ac2c8096f6fd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127806"
---
# <a name="user-authentication-information"></a>Informações de autenticação do usuário

O serviço de Gerenciador de Conexões remoto no computador cliente envia um nome de usuário e uma senha para o servidor RAS no computador remoto. Antes de estabelecer uma conexão, o servidor remoto usa essas informações para autenticar o usuário. Por padrão, o Gerenciador de Conexões remoto envia o nome de usuário e a senha do usuário conectado no momento. O cliente RAS pode usar a [**estrutura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) especificada na [**chamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar um nome de usuário e senha diferentes.

Se o servidor remoto não puder autenticar o usuário com as informações especificadas, ele poderá permitir que [a](paused-states.md) operação de conexão entre em um estado em pausa para permitir que o cliente RAS colete dados de autenticação diferentes do usuário.

 

 