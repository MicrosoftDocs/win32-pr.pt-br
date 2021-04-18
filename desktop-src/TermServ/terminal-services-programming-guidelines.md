---
title: Diretrizes de programação de Serviços de Área de Trabalho Remota
description: Tópicos que fornecem diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, diretrizes de programação
- Diretrizes de programação Serviços de Área de Trabalho Remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105778805"
---
# <a name="remote-desktop-services-programming-guidelines"></a>Diretrizes de programação de Serviços de Área de Trabalho Remota

A maioria dos aplicativos baseados no Windows de 32 bits ou 64 bits executam "no estado em que se encontram" em um ambiente Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal). No entanto, alguns aplicativos funcionam corretamente e funcionam bem em um ambiente de Serviços de Área de Trabalho Remota, enquanto outros não. Os tópicos a seguir fornecem diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Diretrizes de vários usuários](multiple-user-guidelines.md)
</dt> <dd>

Diretrizes para o desenvolvimento de aplicativos para vários usuários em um ambiente de Serviços de Área de Trabalho Remota.

</dd> <dt>

[Diretrizes de desempenho](performance-guidelines.md)
</dt> <dd>

Diretrizes para o desenvolvimento de aplicativos que têm bom desempenho em um ambiente de Serviços de Área de Trabalho Remota.

</dd> <dt>

[Diretrizes gerais de programação](general-programming-guidelines.md)
</dt> <dd>

Diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.

</dd> </dl>

Muitas dessas diretrizes são boas práticas de programação que irão beneficiar os aplicativos em execução em qualquer ambiente do Windows. No entanto, algumas otimizações recomendadas, como a limitação de efeitos gráficos, são otimizações que você desejará apenas quando o aplicativo estiver sendo executado em Serviços de Área de Trabalho Remota. Para obter um exemplo de código que mostra como detectar um ambiente de Serviços de Área de Trabalho Remota, consulte [detectando o ambiente de serviços de área de trabalho remota](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[Os serviços de terminal agora estão Serviços de Área de Trabalho Remota](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Formato de arquivo de modelo administrativo](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[Segurança da chave do registro e direitos de acesso](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[Hives do registro](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[Descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[Direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 