---
description: Memória Dinâmica
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memória Dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088464"
---
# <a name="dynamic-memory"></a>Memória Dinâmica

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes (em execução como máquinas virtuais)** – Windows Vista \| Windows 7  
**Servidores** -Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -alta  






## <a name="description"></a>Descrição

Em um alto nível, o Hyper-V Memória Dinâmica é um aprimoramento de gerenciamento de memória para a função do Hyper-V incluída no Windows Server 2008 R2 SP1. Ele foi projetado para uso em produção e permite que os clientes alcancem taxas de maior capacidade de consolidação/VM (máquina virtual), otimizando a utilização de memória no computador físico. A alocação de memória estática é reduzida e a memória adicional é alocada de acordo com a necessidade. Memória Dinâmica afeta os desenvolvedores de software que desejam garantir que o software funcione corretamente em um ambiente de máquina virtual.

## <a name="usage-scenario"></a>Cenário de uso

Há dois cenários de uso principal em que Memória Dinâmica entram em cena, aplicativos do lado do host e aplicativos do lado do convidado.

**Aplicativos do lado do host (ferramentas de gerenciamento)**

As ferramentas antigas que gerenciam um novo servidor Windows Server 2008 R2 SP1 não poderão acessar as novas configurações de Memória Dinâmica. Novas APIs e contadores de desempenho do WMI foram desenvolvidos para gerenciar as novas configurações de Memória Dinâmica para máquinas virtuais do Hyper-V. Os desenvolvedores de software que trabalham em ferramentas de gerenciamento devem aproveitar essas APIs e contadores para uso com o Windows Server 2008 R2 SP1 com a função Hyper-V instalada. Os detalhes sobre essas novas APIs estarão disponíveis por meio [da documentação do provedor WMI do Hyper-V no MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).

**Aplicativos do lado do convidado**

Os desenvolvedores que escrevem software para uso dentro de uma máquina virtual configurada para usar Memória Dinâmica precisam ter em mente que a memória do sistema de VM não é mais constante. Consequentemente, o aplicativo deve liberar memória quando não for mais necessário para permitir que outros aplicativos tirem proveito do recurso.

Alocações de memória e desalocações continuam funcionando normalmente para aplicativos de usuário. Memória Dinâmica é completamente transparente para a maioria dos aplicativos do usuário final. No entanto, se o software que está sendo desenvolvido fizer uso de contadores de desempenho de memória na máquina virtual, o teste cuidadoso deverá ser executado em um ambiente Memória Dinâmica habilitado para garantir que o software faça as alterações feitas na conta da alocação de memória do sistema operacional convidado. A memória disponível não é mais "estática" da perspectiva da máquina virtual? s.

## <a name="solutions"></a>Soluções

As máquinas virtuais devem ter o SP1 (Integration Services) atualizado instalado a fim de aproveitar o Memória Dinâmica. Verifique se todos os computadores usados no gerenciamento de máquinas virtuais do Hyper-V estão usando os bits mais recentes do Windows Server 2008 R2 SP1.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Memória Dinâmica entrando no blog do Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Usando o provedor WMI do Hyper-V](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Isenção de responsabilidade

As informações contidas neste documento estão relacionadas ao produto de pré-lançamento software que pode ser substancialmente modificado antes de sua primeira versão comercial. De acordo, as informações podem não descrever ou refletir com precisão o produto de software quando o primeiro é lançado comercialmente. Este documento serve apenas para fins informativos. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
