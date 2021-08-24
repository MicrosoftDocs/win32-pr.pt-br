---
description: Memória Dinâmica
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memória Dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 408e54aa1a1d238a98bb0eff8af2dd76862b32b77c26b3d3812d8707bc0099f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329848"
---
# <a name="dynamic-memory"></a>Memória Dinâmica

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes (em execução como máquinas virtuais)** – Windows Vista \| Windows 7  
**Servidores** – Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Impacto do recurso

 **Gravidade –** Baixa  
**Frequência** – Alta  






## <a name="description"></a>Descrição

Em um alto nível, o Hyper-V Memória Dinâmica é um aprimoramento de gerenciamento de memória para a função Hyper-V incluída no Windows Server 2008 R2 SP1. Ele foi projetado para uso em produção e permite que os clientes alcancem taxas de densidade de VM (consolidação/máquina virtual) mais altas, otimizando a utilização de memória no computador físico. A alocação de memória estática é reduzida e a memória adicional é alocada conforme necessário. Memória Dinâmica afeta os desenvolvedores de software que querem garantir que seu software funcione corretamente em um ambiente de máquina virtual.

## <a name="usage-scenario"></a>Cenário de uso

Há dois cenários de uso principais em que Memória Dinâmica entra em cena, aplicativos do lado do host e aplicativos do lado do convidado.

**Aplicativos do lado do host (ferramentas de gerenciamento)**

Ferramentas antigas que gerenciam um novo servidor Windows Server 2008 R2 SP1 não poderão acessar as novas Memória Dinâmica configurações. Novas APIs WMI e contadores de desempenho foram desenvolvidos para gerenciar as novas Memória Dinâmica configurações para máquinas virtuais hyper-V. Os desenvolvedores de software que trabalham em ferramentas de gerenciamento devem aproveitar essas APIs e contadores para uso com o Windows Server 2008 R2 SP1 com a função Hyper-V instalada. Detalhes sobre essas novas APIs estarão disponíveis por meio da documentação do Provedor WMI do [Hyper-V no MSDN.](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

**Aplicativos do lado do convidado**

Os desenvolvedores que escrevem software para uso dentro de uma máquina virtual configurada para usar Memória Dinâmica precisam ter em mente que a memória do sistema de VM não é mais constante. Consequentemente, o aplicativo deve liberar memória quando não for mais necessário permitir que outros aplicativos aproveitem o recurso.

As alocações de memória e desa alocações continuam a funcionar normalmente para aplicativos de usuário. Memória Dinâmica é completamente transparente para a maioria dos aplicativos de usuário final. No entanto, se o software que está sendo desenvolvido usa contadores de desempenho de memória na máquina virtual, testes cuidadosos devem ser executados em um ambiente habilitado para Memória Dinâmica para garantir que o software use as alterações feitas na alocação de memória do sistema operacional convidado em conta. A memória disponível não é mais "estática" da perspectiva da máquina virtual.

## <a name="solutions"></a>Soluções

As máquinas virtuais devem ter o SP1 (Integration Services) atualizado instalado para aproveitar os Memória Dinâmica. Verifique se todas as máquinas usadas no gerenciamento de máquinas virtuais Hyper-V estão usando os bits Windows Server 2008 R2 SP1 mais recentes.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Memória Dinâmica blog do Coming To Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Usando o provedor WMI do Hyper-V](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Isenção de responsabilidade

As informações contidas neste documento estão relacionadas ao produto de software de pré-lançamento que pode ser substancialmente modificado antes de sua primeira versão comercial. Da mesma forma, as informações podem não descrever ou refletir com precisão o produto de software quando lançados comercialmente pela primeira vez. Este documento serve apenas para fins informativos. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
