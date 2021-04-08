---
description: Explica as diferenças entre o SSP/APs e os SSPs.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs versus SSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922366"
---
# <a name="sspaps-vs-ssps"></a>SSP/APs versus SSPs

Os [*pacotes de segurança*](../secgloss/s-gly.md) são implantados em um dos seguintes tipos de DLLs (bibliotecas de vínculo dinâmico):

-   [SSP/APs](#sspaps-vs-ssps)
-   [SSPs](#sspaps-vs-ssps)

Se um pacote de segurança está em um provedor de suporte de segurança/um [*pacote de autenticação*](../secgloss/a-gly.md) (SSP/AP) ou uma DLL do SSP (provedor de [*suporte de segurança*](../secgloss/s-gly.md) ) é determinada pelos tipos de serviços de segurança que ele fornece e da extensão para a qual ele requer integração com a [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA). Essas diferenças também determinam a API implementada em um pacote de segurança personalizado.

## <a name="sspaps"></a>SSP/APs

Um SSP/AP é uma DLL que contém um ou mais [*pacotes de segurança*](../secgloss/s-gly.md) e pode funcionar como um SSP para aplicativos cliente/servidor e como um [pacote de autenticação](authentication-packages.md) para aplicativos de logon. Para funcionar em ambas as funções, os SSP/APs são carregados no espaço de processo do LSA na inicialização do sistema e podem ser carregados em processos de aplicativos cliente/servidor também.

Os pacotes de segurança do SSP/AP personalizados devem implementar as [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md)e [funções implementadas pelo SSP/APS](authentication-functions.md). Essas implementações de função podem fazer uso de funções de suporte de LSA para oferecer recursos avançados de segurança, como a criação de tokens, suporte a [*credenciais complementares*](../secgloss/s-gly.md) e autenticação de passagem.

Se um pacote de segurança do SSP/AP personalizado fornecer uma gama completa de funções de [*integridade*](../secgloss/i-gly.md) e privacidade de mensagens, ele também implementará as [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md).

## <a name="ssps"></a>SSPs

Um SSP é uma DLL que contém um ou mais pacotes de segurança que fornecem conexão autenticada, integridade de mensagem e serviços de criptografia de mensagens a aplicativos cliente/servidor. Os SSPs implementam as funções de SSPI ( [interface do provedor de suporte de segurança](sspi.md) ). Os aplicativos podem acessar os pacotes de segurança em um SSP chamando as funções SSPI diretamente. Os SSPs são carregados nos processos de cliente e servidor; Eles não são integrados à LSA.

 

 
