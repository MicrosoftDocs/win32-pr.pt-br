---
description: Depois de criar o provedor de rede ou o Gerenciador de credenciais, você deve registrá-lo no sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registrando provedores de rede e gerenciadores de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169825"
---
# <a name="registering-network-providers-and-credential-managers"></a>Registrando provedores de rede e gerenciadores de credenciais

Depois de criar o provedor de rede ou o Gerenciador de credenciais, você deve registrá-lo no sistema. Isso é necessário para que o MPR saiba quais provedores de rede estão instalados. Quando o MPR é iniciado, ele verifica o registro e carrega os provedores de rede ou os gerenciadores de credenciais encontrados.

Como os provedores de rede e os gerenciadores de credenciais estão relacionados, eles são registrados nas mesmas subchaves do registro. Na verdade, as DLLs do provedor de rede também podem ser gerenciadores de credenciais.

Para obter informações detalhadas sobre as chaves do registro que você deve criar para o provedor de rede ou o Gerenciador de credenciais, consulte [chaves do registro de autenticação](authentication-registry-keys.md).

 

 



