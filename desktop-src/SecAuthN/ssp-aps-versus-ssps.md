---
description: Explica as diferenças entre SSP/APs e SSPs.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs versus SSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c471e529a478cadbfcc385a1b0d699a4539e7bc80beeb2d40e01e2f7e9f428d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917262"
---
# <a name="sspaps-vs-ssps"></a>SSP/APs versus SSPs

[*Os pacotes*](../secgloss/s-gly.md) de segurança são implantados em um dos seguintes tipos de DLLs (bibliotecas de vínculo dinâmico):

-   [SSP/APs](#sspaps-vs-ssps)
-   [Ssps](#sspaps-vs-ssps)

Se um pacote de segurança está em um SSP/AP [*(provedor*](../secgloss/a-gly.md) de suporte de segurança/pacote de autenticação) ou uma DLL do SSP [*(provedor*](../secgloss/s-gly.md) de suporte de segurança) é determinado pelos tipos de serviços de segurança que ele fornece e a extensão à qual ele requer integração com a LSA (Autoridade de Segurança [*Local).*](../secgloss/l-gly.md) Essas diferenças também determinam a API implementada em um pacote de segurança personalizado.

## <a name="sspaps"></a>SSP/APs

Um SSP/AP é uma DLL [](../secgloss/s-gly.md) que contém um ou mais pacotes de segurança e [](authentication-packages.md) pode funcionar como um SSP para aplicativos cliente/servidor e como um pacote de autenticação para aplicativos de logon. Para funcionar em ambas as funções, os SSP/APs são carregados no espaço de processo LSA na inicialização do sistema e também podem ser carregados em processos de aplicativo cliente/servidor.

Os pacotes de segurança SSP/AP personalizados devem implementar as funções Implementadas por [SSP/APs](authentication-functions.md)no modo de usuário e as funções [implementadas pelo SSP/APs.](authentication-functions.md) Essas implementações de função podem usar funções de suporte LSA para oferecer recursos avançados de segurança, como criação de tokens, suporte a credenciais [*complementares*](../secgloss/s-gly.md) e autenticação de passagem.

Se um pacote de segurança SSP/AP [](../secgloss/i-gly.md) personalizado fornece a gama completa de funções de integridade e privacidade de mensagens, ele também implementará as Funções Implementadas por [SSP/APs](authentication-functions.md)do modo de usuário.

## <a name="ssps"></a>Ssps

Um SSP é uma DLL que contém um ou mais pacotes de segurança que fornecem conexão autenticada, integridade de mensagens e serviços de criptografia de mensagens para aplicativos cliente/servidor. Os SSPs [implementam funções](sspi.md) SSPI (Interface do Provedor de Suporte de Segurança). Os aplicativos podem acessar os pacotes de segurança em um SSP chamando as funções SSPI diretamente. Os SSPs são carregados nos processos do cliente e do servidor; eles não são integrados ao LSA.

 

 
