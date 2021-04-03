---
description: HKLM \\ software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646464"
---
# <a name="exec"></a>Exec

**HKLM \\ software \\ extensões do Microsoft \\ Internet Explorer \\ \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Tipo de dados | Intervalo                    | Valor padrão |
|-----------|--------------------------|---------------|
| REG \_ sz   | *Caminho para o executável* |               |



 

## <a name="browser-integration-steps"></a>Etapas de integração do navegador

1.  Use a função [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para determinar se o diagnóstico de rede está instalado. Se estiver instalado, a chave **{e2e2dd38-d088-4134-82b7-f2ba38496583}** estará presente.
2.  Use a função [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para recuperar o caminho do arquivo executável de diagnóstico de rede da entrada **exec** .
3.  Exibir a nova página de erro se o diagnóstico estiver instalado no sistema.
4.  Crie uma extensão de navegador que cria um item de barra de ferramentas padrão se o diagnóstico estiver instalado no sistema.
5.  Execute o executável de diagnóstico de rede usando o caminho recuperado na etapa 2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do recurso ferramentas de diagnóstico de rede](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
