---
description: O design de SSPI permite que os SSPs adicionais sejam gravados e adicionados ao sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Gravando e instalando um provedor de suporte de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771824"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Gravando e instalando um provedor de suporte de segurança

O design de SSPI permite que os SSPs adicionais sejam gravados e adicionados ao sistema. Um [*SSP*](../secgloss/s-gly.md) específico de um modelo de segurança pode ser desenvolvido com a facilidade relativa ou uma grande complexidade, dependendo do nível de integração com o sistema operacional. Um SSP de cliente que permite conexões com um novo tipo de servidor poderia ser desenvolvido muito rapidamente, enquanto que um SSP completo que fornece representação local exigiria mais esforço.

Os SSPs são instalados atualizando um valor de **\_ sz de reg** no registro, localizado da seguinte maneira:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    <dl> <dt>

            Data type
</dt> <dd>            REG \_ sz</dd> </dl>

Uma única DLL pode conter vários SSPs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições sobre o registro e a instalação de um pacote de segurança](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
