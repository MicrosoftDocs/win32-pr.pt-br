---
description: .
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Hyper-V do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6997074e000b17a119a838df5b6fab961b8ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798562"
---
# <a name="server-hyper-v"></a>Hyper-V do servidor

## <a name="platforms"></a>Plataformas

 **Clientes** -Windows XP Windows \| Vista Windows \| 7  
**Servidores** -windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

A virtualização de servidor permite que vários sistemas operacionais sejam executados em um único computador físico como VMs (máquinas virtuais), permitindo consolidar cargas de trabalho de máquinas de servidor subutilizadas em um número menor de máquinas totalmente utilizadas. O Windows 7 inclui vários aprimoramentos na versão 2008 do Windows Server:

-   **Migração ao vivo:** No Windows Server 2008, tivemos migração rápida. Com Migração ao Vivo, melhoramos a velocidade de migração e a flexibilidade de armazenamento.
-   **Suporte ao processador lógico:** Aumentamos os processadores de host lógico de 16LP para 64LP.
-   **Adição automática de armazenamento:** Agora você pode adicionar discos de passagem ou VHD adicionais a uma máquina virtual em execução sem desligar a máquina virtual.
-   **Novo suporte de hardware:** Adicionamos suporte para as tecnologias incluídas em novos processadores e placas de rede chegando ao mercado, incluindo conversão de segundo nível (SLAT), descarregamento de TCP (Chimney) e VMdQ.
-   **TSv (virtualização de serviços de terminal):** Solução de área de trabalho centralizada para Hyper-V.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

-   **Migração ao vivo:** Talvez seja necessário alterar a maneira como você projetou seus sistemas de armazenamento para aproveitar totalmente essa tecnologia. Embora essas alterações possam não ser necessárias, você pode optar por implementá-las para aproveitar totalmente os benefícios. Talvez seja necessário um aplicativo de gerenciamento para orquestrar Migração ao Vivo.
-   **Suporte ao processador lógico:** Esse recurso não terá impacto sobre clientes ou ISVs ao migrar do Windows Server 2008 para o Windows Server 2008 R2.
-   **Adição automática de armazenamento:** Esse recurso não terá impacto sobre clientes ou ISVs ao migrar do Windows Server 2008 para o Windows Server 2008 R2. Os aplicativos de gerenciamento que definem as configurações de uma máquina virtual podem exigir atualização para gerenciar esse novo recurso.
-   **Novo suporte de hardware:** Esses recursos se aplicam apenas a novos hardwares que estão sendo introduzidos no mercado. Como ele não terá suporte de Build para esses recursos, não é provável que um servidor físico que esteja sendo migrado do Windows Server 2008 para o Windows Server 2008 R2 seja afetado. Se esses recursos estiverem disponíveis no servidor que está sendo migrado, nenhuma alteração direta será prevista.
-   **Virtualização de serviços de terminal:** Esse recurso não terá impacto sobre clientes ou ISVs ao migrar do Windows Server 2008 para o Windows Server 2008 R2. Os aplicativos que utilizam TS (serviços de terminal) podem ser afetados. Esse recurso integra-se diretamente ao TS e, portanto, os aplicativos que configuram o TS podem exigir atualização para gerenciar esse novo recurso.

## <a name="mitigation"></a>Atenuação

-   **Migração ao vivo:** Forneça orientação prescritiva aos usuários finais com práticas recomendadas e recomendações para o design do sistema de armazenamento. Você deve informar ao usuário final sobre as opções e as recomendações.

## <a name="leveraging-capabilitities"></a>Aproveitando o Capabilitities

-   **Migração ao vivo:** Esse recurso habilita o ambiente de ti dinâmico. Os desenvolvedores de aplicativos de gerenciamento de virtualização devem Modificar seu aplicativo para aproveitar esse novo recurso. A Microsoft tornará as interfaces WMI disponíveis publicamente para permitir que um desenvolvedor integre aplicativos a esse recurso.
-   **Virtualização de serviços de terminal:** Esse recurso habilita um novo cenário de virtualização. Os aplicativos que utilizam TS (serviços de terminal) podem ser afetados. Esse recurso integra-se diretamente ao TS e, portanto, os aplicativos que configuram o TS podem exigir atualização para gerenciar esse novo recurso.

## <a name="links-to-other-resources"></a>Links para outros recursos

[Interfaces de gerenciamento do WMI para Hyper-V v1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Embora a maior parte desse conteúdo seja aplicada à v2 do Hyper-V, uma versão atualizada com informações específicas de v2 deve estar disponível mais perto do lançamento do Windows 7.

 

 
