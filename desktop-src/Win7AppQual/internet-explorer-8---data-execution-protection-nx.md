---
description: Internet Explorer 8-proteção de execução de dados/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-proteção de execução de dados/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1f969aa2e934f36142995150b6484dad2fa5067f6cbb5ab3a947055af375ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998886"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8-proteção de execução de dados/NX

## <a name="affected-platforms"></a>Plataformas afetadas

 **clientes** -Windows XP, Windows Vista, Windows 7  
**servidores** -Windows server 2003, Windows server 2008, Windows server 2008 R2  










> [!Note]  
> O Internet Explorer 8 habilitará a proteção DEP/NX quando for executado em um sistema operacional com as service pack mais recentes. Windows o XP sp3, Windows server 2003 SP3, Windows Vista SP1 e Windows Server 2008 têm o DEP/NX habilitado por padrão no Internet Explorer 8.

 

## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -média  
**Frequência** -baixa  

> [!Note]  
> Normalmente, qualquer aplicativo executado no Internet Explorer e não é compatível com o DEP/NX falhará na inicialização e não funcionará. O Internet Explorer poderá falhar na inicialização se os complementos não compatíveis com o DEP/NX estiverem instalados.

 

## <a name="description"></a>Descrição

O DEP/NX é um recurso de segurança que ajuda a reduzir vulnerabilidades relacionadas à memória. A partir do Internet Explorer 8, todos os processos do Internet Explorer habilitam o recurso DEP/NX por padrão.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

o Kernel Windows monitora a execução de um programa. Se o kernel detectar uma tentativa de executar o código de uma página de memória que não esteja marcada como executável, o kernel interromperá a execução do programa, resultando em uma "falha". Essa é uma medida de segurança para ajudar a garantir que vulnerabilidades relacionadas à memória (por exemplo, estouros de buffer) no aplicativo não possam ser exploradas para executar código arbitrário.

## <a name="end-user-mitigation"></a>Mitigação de End-User

-   Instale uma versão mais recente do complemento ou da estrutura compatível com o DEP/NX.
-   Execute o Internet Explorer com privilégios elevados como administrador e, em seguida, desabilite o DEP/NX usando a caixa de seleção **habilitar proteção de memória para ajudar a atenuar os ataques online** na guia Avançado **Opções da Internet**  /   .

## <a name="developer-solution"></a>Solução de desenvolvedor

Compile aplicativos usando as versões mais recentes das estruturas compatíveis com o DEP.

## <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

-   Use a opção de vinculador/NXCOMPAT para indicar a compatibilidade com DEP/NX
-   Opte pelo seu código em outras defesas disponíveis, como o conjunto de defesa (/GS), o/SafeSEH (tratamento de exceção segura) e a ASLR (/DynamicBase)

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

-   teste seu código com o DEP/NX habilitado usando a versão mais recente do Internet Explorer no Windows Vista SP1 ou posterior.
-   teste com o Internet Explorer 7 no Windows Vista depois de habilitar a opção DEP/NX. Para habilitar o DEP/NX para Internet Explorer 7, execute o Internet Explorer como administrador e, em seguida, defina a caixa de seleção apropriada na guia ferramentas > opções da Internet > avançado.
-   execute a ferramenta de teste de compatibilidade do Internet Explorer (IECTT), fornecida com o ACT (Toolkit de compatibilidade de aplicativos) para localizar possíveis problemas devido às alterações de DEP/NX.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Internet Explorer 8 parte I: proteção de memória DEP/NX](/archive/blogs/ie/)
-   [Prevenção de Execução de Dados](../memory/data-execution-prevention.md)
-   [novas APIs NX adicionadas ao Windows Vista SP1, Windows XP SP3 e Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [Download de Toolkit de compatibilidade de aplicativos](/windows-hardware/get-started/adk-install)
-   [Problemas conhecidos do recurso de segurança do Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
