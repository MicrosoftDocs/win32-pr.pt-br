---
description: Remoção do Windows Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Remoção do Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2456fa5bdf9d981385f2b4832250358f7bfdab1b223aeb3658d8df4cc212237b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328930"
---
# <a name="removal-of-windows-mail"></a>Remoção do Windows Mail

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** – Alta  
**Frequência** – Alta  









## <a name="description"></a>Descrição

A Microsoft está preterindo o utilitário Windows Mail e desabilitando a API CoStartOutlookExpress. As outras APIs de email foram marcadas como preterida e são marcadas para remoção em uma versão Windows posterior. No entanto, as APIs documentadas publicamente que não estão marcadas como preterida ou obsoletas continuarão a funcionar no Windows 7. Os binários permanecerão nos sistemas dos usuários e continuarão acessíveis por meio das APIs, especificamente nos casos mencionados acima. Além disso, os arquivos de email (.eml) e notícias dos usuários (.nws) permanecerão no sistema.

## <a name="manifestation-of-impact"></a>Manifestação de impacto

A remoção Windows Mail resulta no seguinte:

-   Todos os pontos de entrada Windows Email e Contatos (por exemplo, Menu Iniciar, Atalhos criados pelo usuário, Iniciar -> Executar e assim por diante) são removidos ou desabilitados. Algumas delas são completamente removidas, outras falharão ao tentar iniciar.
-   Todas as DLLs são reenvadas na caixa
-   As APIs documentadas publicamente continuam a funcionar como no Windows Vista
-   Todas as APIs que tentam iniciar a interface do usuário principal do navegador foram modificadas para criar uma falha silenciosa. A função retornará êxito, mas não mostrará a interface do usuário para o usuário. As APIs que chamam outras caixas de diálogo (por exemplo, o Spooler ou a caixa de diálogo Contas) continuam a mostrar essa interface do usuário
-   Manipuladores de protocolo (mailto, ldap, notícias, snews, nntp) não serão associados ao Windows Mail ou Contacts. Ao tentar inocioná-los, os clientes verão uma caixa de diálogo de erro apontando-os para o local em que podem definir essas associações para outro programa
-   Associações de arquivo (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) são interrompidas ou desabilitadas. Ao tentar abrir um arquivo com essas extensões, os clientes receberão uma caixa de diálogo oferecendo outros aplicativos instalados que podem ser usados e os apontarão para uma página da Web que oferece soluções
-   Todos os arquivos de usuário (por exemplo, arquivos de contato ou mensagens) permanecem no sistema no cenário de atualização
-   A pasta Contatos fica oculta por padrão para que os clientes não a vejam
-   AS APIs são marcadas como preterida no MSDN
-   A função de visualização de arquivo foi removida
-   Ganchos de shell no menu de clique com o botão direito do mouse são removidos
-   A função de pesquisa de arquivo é removida

## <a name="mitigation"></a>Atenuação

Os usuários devem Windows Live Mail ou qualquer outro produto de email que possa ler arquivos .eml e .nws.

## <a name="solution"></a>Solução

Detectar se há um manipulador de email padrão instalado. Caso contrário, informe ao usuário para instalar Windows Live Mail ou qualquer outro produto que possa ler arquivos .eml e .nws.

Não projete o código que chama Windows API de interface do usuário do Windows Mail, pois ela não funcionará. Você deve encontrar outras maneiras de acessar os arquivos .eml e .nws. Além disso, assim que for viável, descontinue sua dependência em todas as outras APIs Windows Mail.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Teste de compatibilidade, desempenho, confiabilidade e usabilidade

-   Exerça seu aplicativo em um Windows 7 para garantir que o aplicativo não tente chamar a API de interface do usuário.
-   Como alternativa, você pode executar o ACT (Application Compatibility Toolkit) usando o Avaliador de Compatibilidade do Windows (WCE) para localizar possíveis problemas devido à preteração dessa funcionalidade.

## <a name="links-to-other-resources"></a>Links para outros recursos

<dl>

[Download de compatibilidade Toolkit aplicativo](/windows-hardware/get-started/adk-install)  
</dl>

 

 
