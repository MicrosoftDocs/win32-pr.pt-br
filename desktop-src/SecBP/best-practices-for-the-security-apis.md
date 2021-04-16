---
description: Sugestões para avaliações de segurança de aplicativos para o desenvolvimento de aplicativos do software de segurança do Windows e o desenvolvimento de software seguro, incluindo teste de segurança do aplicativo.
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: Práticas recomendadas para as APIs de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa821cfbaa9874d17559ad0e81f636fbaddd14f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757485"
---
# <a name="best-practices-for-the-security-apis"></a>Práticas recomendadas para as APIs de segurança

Para ajudar a desenvolver softwares seguros, recomendamos que você use as práticas recomendadas a seguir ao desenvolver aplicativos. Para obter mais informações, consulte [Security Developer Center](https://msdn.microsoft.com/security/default.aspx).

## <a name="security-development-life-cycle"></a>Ciclo de vida de desenvolvimento de segurança

O SDL ( [ciclo de vida de desenvolvimento de segurança](/previous-versions/ms995349(v=msdn.10)) ) é um processo que alinha uma série de atividades voltadas à segurança e resultados finais em cada fase do desenvolvimento de software. Essas atividades e os resultados finais incluem:

-   Desenvolvendo modelos de ameaças
-   Usando ferramentas de verificação de código
-   Conduzindo revisões de código e testes de segurança

Para obter mais informações sobre o SDL, consulte o [blog do SDL](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx).

## <a name="threat-models"></a>Modelos de ameaça

A condução de uma análise do modelo de ameaça pode ajudá-lo a descobrir possíveis pontos de ataque em seu código. Para obter mais informações sobre a análise do modelo de risco, consulte Howard, Michael e LeBlanc, David \[ 2003 \] , *escrevendo código seguro*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington. (Esse recurso pode não estar disponível em alguns idiomas e países.)

## <a name="service-packs-and-security-updates"></a>Service Packs e atualizações de segurança

Ambientes de compilação e teste devem espelhar os mesmos níveis de Service Packs e atualizações de segurança da base de usuários de destino. Recomendamos que você instale os service packs e atualizações de segurança mais recentes para qualquer plataforma ou aplicativo da Microsoft que faça parte de seu ambiente de compilação e teste e incentive os usuários a fazer o mesmo para o ambiente de aplicativo concluído. Para obter mais informações sobre Service Packs e atualizações de segurança, consulte [microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us) e [Microsoft Security](https://www.microsoft.com/security).

## <a name="authorization"></a>Autorização

Você deve criar aplicativos que exigem o privilégio mínimo possível. Usar o privilégio mínimo possível reduz o risco de um código mal-intencionado comprometer seu sistema de computador. Para obter mais informações sobre como executar código no menor nível de privilégio possível, consulte [executando com privilégios especiais](running-with-special-privileges.md).

## <a name="more-information"></a>Mais informações

Para obter mais informações sobre as práticas recomendadas, consulte os tópicos a seguir.



| Tópico                                                                                                                        | Descrição                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Executando com privilégios especiais](running-with-special-privileges.md)<br/>                                            | Discute as implicações de segurança dos privilégios.<br/>                                                                                                                                  |
| [Evitando estouros de buffer](avoiding-buffer-overruns.md)<br/>                                                          | Fornece informações sobre como evitar estouros de buffer.<br/>                                                                                                                            |
| [CFG (Proteção de Fluxo de Controle) ](control-flow-guard.md)<br/>                                                                | Discute vulnerabilidades de corrupção de memória.<br/>                                                                                                                                    |
| [Criando uma DACL](creating-a-dacl.md)<br/>                                                                            | Mostra como criar uma DACL (lista de controle de acesso discricionário) usando o SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ).<br/> |
| [Manipulando senhas](handling-passwords.md)<br/>                                                                      | Discute as implicações de segurança do uso de senhas.<br/>                                                                                                                             |
| [Como otimizar a pesquisa da biblioteca MSDN](how-to-optimize-your-msdn-library-search.md)<br/>                          | Discute opções de pesquisa de conteúdo do SDK de segurança na biblioteca MSDN.<br/>                                                                                                           |
| [Extensibilidade do desenvolvedor de controle de acesso dinâmico](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | Orientação básica para alguns dos pontos de extensibilidade do desenvolvedor para as novas soluções de controle de acesso dinâmico.<br/>                                                                   |



 

 

