---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Remoção do Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171469"
---
# <a name="removal-of-windows-mail"></a>Remoção do Windows Mail

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -alta  
**Frequência** -alta  









## <a name="description"></a>Descrição

A Microsoft está preterindo o utilitário Windows Mail e desabilitando a API CoStartOutlookExpress. As outras APIs de email foram marcadas como preteridas e são removidas para remoção em uma versão posterior do Windows. No entanto, as APIs documentadas publicamente que não estão marcadas como preteridas ou obsoletas continuarão a funcionar no Windows 7. Os binários permanecerão nos sistemas dos usuários e continuarão acessíveis por meio das APIs, especificamente nos casos mencionados acima. Além disso, os arquivos de email (. eml) e de notícias (. NWS) dos usuários permanecerão no sistema.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

A remoção do Windows Mail resulta no seguinte:

-   Todos os pontos de entrada para o Windows Mail e contatos (por exemplo, menu Iniciar, atalhos criados pelo usuário, execução de > de início e assim por diante) são removidos ou desabilitados. Algumas delas são completamente removidas, outras falharão ao tentar iniciar.
-   Todas as DLLs são fornecidas na caixa
-   APIs documentadas publicamente continuam funcionando como faziam no Windows Vista
-   Todas as APIs que tentarem iniciar a interface do usuário do navegador principal foram modificadas para criar uma falha silenciosa. A função retornará êxito, mas não mostrará a IU ao usuário. As APIs que chamam outras caixas de diálogo (por exemplo, o spooler ou a caixa de diálogo contas) continuam a mostrar essa interface do usuário
-   Os manipuladores de protocolo (mailto, LDAP, News, snews, NNTP) não serão associados ao Windows mail ou aos contatos. Ao tentar iniciá-los, os clientes verão uma caixa de diálogo de erro apontando para o local onde podem definir essas associações para outro programa
-   As associações de arquivo (. eml,. nws,. Contact,. Group,. wab,. p7c,. VFC) estão desfeitas ou desabilitadas. Ao tentar abrir um arquivo com essas extensões, os clientes receberão uma caixa de diálogo oferecendo a eles outros aplicativos instalados que podem usá-los e apontar para uma página da Web que oferece soluções
-   Todos os arquivos de usuário (por exemplo, arquivos de contato ou mensagens) permanecem no sistema no cenário de atualização
-   A pasta contatos fica oculta por padrão, de modo que os clientes não as verão
-   As APIs são marcadas como preteridas no MSDN
-   A função de visualização de arquivo foi removida
-   Os ganchos do Shell no menu de atalho são removidos
-   A função de pesquisa de arquivo foi removida

## <a name="mitigation"></a>Atenuação

Os usuários devem instalar o Windows Live mail ou qualquer outro produto de email capaz de ler arquivos. eml e. nws.

## <a name="solution"></a>Solução

Detectar se há um manipulador de email padrão instalado. Caso contrário, avise o usuário para instalar o Windows Live mail ou qualquer outro produto capaz de ler arquivos. eml e. nws.

Não crie um código que chame a API da interface do usuário do Windows Mail, pois ele não funcionará. Você deve encontrar outras maneiras de acessar os arquivos. eml e. nws. Além disso, assim que for viável, descontinue sua dependência em todas as outras APIs do Windows Mail.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

-   Exerça seu aplicativo em um ambiente do Windows 7 para garantir que o aplicativo não tente chamar a API da interface do usuário.
-   Como alternativa, você pode executar o kit de ferramentas de compatibilidade de aplicativos (ACT) usando o Stone (avaliador de compatibilidade do Windows) para localizar possíveis problemas devido à reprovação dessa funcionalidade.

## <a name="links-to-other-resources"></a>Links para outros recursos

<dl>

[Download do kit de ferramentas de compatibilidade de aplicativos](/windows-hardware/get-started/adk-install)  
</dl>

 

 
