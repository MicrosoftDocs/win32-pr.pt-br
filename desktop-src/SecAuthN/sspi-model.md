---
description: A interface de provedor de suporte de segurança (SSPI) permite que um aplicativo use vários modelos de segurança disponíveis em um computador ou rede sem alterar a interface para o sistema de segurança.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modelo SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370567"
---
# <a name="sspi-model"></a>Modelo SSPI

A [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) permite que um aplicativo use vários modelos de segurança disponíveis em um computador ou rede sem alterar a interface para o sistema de segurança. O SSPI não estabelece [*credenciais*](../secgloss/c-gly.md) de logon porque isso geralmente é uma operação privilegiada tratada pelo sistema operacional.

Um SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) está contido em uma dll ( [*biblioteca de vínculo dinâmico*](../secgloss/d-gly.md) ) que implementa o SSPI, tornando um ou mais [*pacotes de segurança*](../secgloss/s-gly.md) disponíveis para os aplicativos. Cada pacote de segurança fornece mapeamentos entre as chamadas de função SSPI de um aplicativo e as funções de um modelo de segurança real. Os pacotes de segurança dão suporte a [*protocolos de segurança*](../secgloss/s-gly.md) como a autenticação [*Kerberos*](../secgloss/k-gly.md) e o Gerenciador de LAN.

A interface SSPI está disponível no modo kernel, bem como no modo de usuário. Para usar a funcionalidade SSPI no modo kernel, você deve instalar o DDK do sistema de arquivos instalável do Windows. O modelo de chamada permanece o mesmo, mas as considerações do modo kernel são observadas nas páginas de referência de função. Para obter mais informações, consulte [funções SSPI](authentication-functions.md).

 

 
