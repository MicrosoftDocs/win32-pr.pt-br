---
description: O mecanismo de protocolo do SSL (Schannel) usa um CSP (provedor de serviços de criptografia) ao executar operações criptográficas. Os aplicativos criptográficos podem chamar o CryptAcquireContext usando os \_ provedores de RSA \_ Schannel e Prov DH do Prov \_ \_ .
ms.assetid: ad1eabf1-23bc-4d23-8f8b-13f0bda95120
title: Usando CSPs Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289ed57d9f312ee1ef57aecf7534a8d585859126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796367"
---
# <a name="using-schannel-csps"></a>Usando CSPs Schannel

O mecanismo de protocolo do SSL ([*Schannel*](../secgloss/s-gly.md)) usa um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) ao executar operações criptográficas. Os aplicativos criptográficos podem chamar o [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) usando os \_ provedores de RSA \_ Schannel e Prov DH do Prov \_ \_ .

Esta seção define os [*tipos de CSP*](../secgloss/c-gly.md) RSA e Diffie-Hellman Schannel e descreve a funcionalidade que um CSP deve oferecer para ser compatível com Schannel.dll, o mecanismo de protocolo criptográfico. Um mecanismo de protocolo é um programa que estabelece um canal de comunicações seguro entre um aplicativo cliente e servidor.

Os aplicativos não devem tentar usar as informações nesta documentação para usar o PROV \_ RSA \_ Schannel ou o Prov \_ DH \_ Schannel diretamente. Em vez disso, esta documentação explica como os desenvolvedores e fornecedores do CSP devem gravar CSPs Schannel compatíveis com os provedores do Microsoft Schannel.

Esta documentação destina-se a ajudar os desenvolvedores de CSP a implementar CSPs de Schannel compatíveis com RSA ou Diffie-Hellman. Presume-se que os desenvolvedores estejam familiarizados [*com o protocolo*](../secgloss/s-gly.md) SSL versão 3,0, criptografia de [*chave pública*](../secgloss/p-gly.md) , [*certificados digitais*](../secgloss/d-gly.md)e o conjunto de funções CryptoAPI. Os desenvolvedores novos para esses tópicos são aconselhados a ler a especificação do protocolo SSL 3,0 e a documentação do [Cryptography Essentials](cryptography-essentials.md) neste SDK. Além disso, os desenvolvedores de CSP RSA e Diffie-Hellman [*devem conhecer as especificações de protocolo*](../secgloss/t-gly.md) TLS, juntamente com os algoritmos de RSA e [*Diffie-Hellman*](../secgloss/d-gly.md)relevantes.

Para obter um exemplo usado por um mecanismo de protocolo da Microsoft, consulte [criando a chave mestra](creating-the-master-key.md). As chamadas para funções de criptografia neste exemplo resultam em chamadas para funções de CP que um CSP deve implementar. Para escrever um CSP compatível, um desenvolvedor deve entender a especificação do SSL 3,0 e combinar esse conhecimento com uma compreensão do código do mecanismo de protocolo semelhante ao usado neste exemplo.

Como o uso do protocolo de tecnologia de comunicação privada deve ser mínimo no futuro, os desenvolvedores de novos CSPs não precisam dar suporte a esse protocolo. O mecanismo de protocolo Schannel oferece suporte estritamente para compatibilidade com versões anteriores.

 

 
