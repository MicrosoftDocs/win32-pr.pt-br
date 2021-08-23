---
description: Sugestões para avaliações de segurança de aplicativo para o desenvolvimento de aplicativos Windows software de segurança e desenvolvimento de software seguro, incluindo testes de segurança de aplicativo.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Práticas recomendadas para as APIs de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934bf52d99456d599f91ec23c6e5472bb4e130565cf1acb56763f29f6396c0b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622875"
---
# <a name="best-practices-for-the-security-apis"></a>Práticas recomendadas para as APIs de segurança

Para ajudar a desenvolver software seguro, recomendamos que você use as práticas recomendadas a seguir ao desenvolver aplicativos. Para obter mais informações, consulte [Central de Desenvolvedores de Segurança.](https://msdn.microsoft.com/security/default.aspx)

## <a name="security-development-life-cycle"></a>Ciclo de vida de desenvolvimento de segurança

O [SDL](/previous-versions/ms995349(v=msdn.10)) (Ciclo de Vida de Desenvolvimento de Segurança) é um processo que alinha uma série de atividades voltadas para segurança e entregas para cada fase do desenvolvimento de software. Essas atividades e entregas incluem:

-   Desenvolvendo modelos de ameaça
-   Usando ferramentas de verificação de código
-   Realização de revisões de código e testes de segurança

Para obter mais informações sobre o SDL, consulte o [Blog do SDL](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Modelos de ameaça

Realizar uma análise de modelo de ameaça pode ajudá-lo a descobrir possíveis pontos de ataque em seu código. Para obter mais informações sobre a análise do modelo de ameaça, consulte Charles, Michael e LeMond, David \[ 2003 \] , Writing Secure *Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. (Esse recurso pode não estar disponível em alguns idiomas e países.)

## <a name="service-packs-and-security-updates"></a>Service Packs e atualizações de segurança

Ambientes de build e teste devem espelhar os mesmos níveis de service packs e atualizações de segurança da base de usuários de alvo. Recomendamos que você instale os service packs e as atualizações de segurança mais recentes para qualquer plataforma ou aplicativo da Microsoft que faça parte do seu ambiente de build e teste e incentive os usuários a fazer o mesmo para o ambiente de aplicativo concluído. Para obter mais informações sobre service packs e atualizações de segurança, consulte [Microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) e Microsoft [Security](https://www.microsoft.com/security).

## <a name="authorization"></a>Autorização

Você deve criar aplicativos que exigem o menor privilégio possível. Usar o privilégio mínimo possível reduz o risco de código mal-intencionado comprometer o sistema do computador. Para obter mais informações sobre como executar código no nível de privilégio mínimo possível, consulte [Executando com privilégios especiais](running-with-special-privileges.md).

## <a name="more-information"></a>Mais informações

Para obter mais informações sobre as práticas recomendadas, consulte os tópicos a seguir.



| Tópico                                                                                                                        | Descrição                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Executando com privilégios especiais](running-with-special-privileges.md)<br/>                                            | Discute implicações de segurança de privilégios.<br/>                                                                                                                                  |
| [Evitando estouros de buffer](avoiding-buffer-overruns.md)<br/>                                                          | Fornece informações sobre como evitar estouros de buffer.<br/>                                                                                                                            |
| [CFG (Proteção de Fluxo de Controle) ](control-flow-guard.md)<br/>                                                                | Discute vulnerabilidades de corrupção de memória.<br/>                                                                                                                                    |
| [Criando uma DACL](creating-a-dacl.md)<br/>                                                                            | Mostra como criar uma DACL (lista de controle de acesso discricionário) usando a SDDL [(Linguagem](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de Definição do Descritor de Segurança).<br/> |
| [Manipulando senhas](handling-passwords.md)<br/>                                                                      | Discute as implicações de segurança do uso de senhas.<br/>                                                                                                                             |
| [Como otimizar sua pesquisa Biblioteca MSDN dados](how-to-optimize-your-msdn-library-search.md)<br/>                          | Discute opções para pesquisar o conteúdo do SDK de Segurança Biblioteca MSDN.<br/>                                                                                                           |
| [Extensibilidade do desenvolvedor do Controle de Acesso Dinâmico](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Orientação básica para alguns dos pontos de extensibilidade do desenvolvedor para as novas soluções de Controle de Acesso Dinâmico.<br/>                                                                   |



 

 

