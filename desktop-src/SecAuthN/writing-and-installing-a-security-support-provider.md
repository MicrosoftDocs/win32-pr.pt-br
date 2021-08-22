---
description: O design do SSPI permite que SSPs adicionais sejam gravados e adicionados ao sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Escrevendo e instalando um provedor de suporte de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac7125c386314ec7772a5e6079f423af0aaf5c9f7dd820a24c042d99834d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914745"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Escrevendo e instalando um provedor de suporte de segurança

O design do SSPI permite que SSPs adicionais sejam gravados e adicionados ao sistema. Um [*SSP específico*](../secgloss/s-gly.md) para um modelo de segurança pode ser desenvolvido com relativa facilidade ou grande complexidade, dependendo do nível de integração com o sistema operacional. Um SSP cliente que permite conexões com um novo tipo de servidor pode ser desenvolvido muito rapidamente, enquanto um SSP completo que fornece representação local exigiria mais esforço.

Os SSPs são instalados atualizando um **valor REG \_ SZ** no Registro, localizado da seguinte forma:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    <dl> <dt>

            Data type
</dt> <dd>            REG \_ SZ</dd> </dl>

Uma única DLL pode conter vários SSPs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições em relação ao registro e instalação de um pacote de segurança](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
