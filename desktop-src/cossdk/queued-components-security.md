---
description: Segurança de componentes na fila
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Segurança de componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682a9b409df2f605c259a6af6741dcc6e59d9fc23852b950a13225b24386c010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547078"
---
# <a name="queued-components-security"></a>Segurança de componentes na fila

Quando um cliente faz uma chamada de método para um objeto na fila, a chamada é realmente feita para o gravador, que o em pacotes como parte de uma mensagem para o servidor. O ouvinte lê a mensagem da fila e a passa para o player. O player invoca o componente de servidor real e faz a mesma chamada de método. O componente de servidor deve observar o contexto de chamada de segurança do cliente (não o contexto de chamada de segurança do jogador) quando o player faz a chamada de método. O gravador faz marshal do contexto de chamada de segurança do cliente para a mensagem e o player o desmarcará no servidor antes de fazer a chamada de método. No que diz respeito ao objeto de servidor, não há nenhuma diferença no contexto de segurança entre uma chamada direta do cliente e uma chamada indireta do player. Em particular, os métodos invocados são executados com os privilégios do remetente.

Um componente em fila COM+ dá suporte à semântica de segurança baseada em função, assim como outros componentes construídos para uso com aplicativos COM+. Componentes de um aplicativo na fila podem, portanto, usar interfaces programáticas para descobrir a associação de função de seu chamador ([**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) ou um usuário específico ([**ISecurityCallContext::IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)). É recomendável que qualquer componente na fila com um possível impacto de segurança use essas interfaces para verificar explicitamente as credenciais do remetente.

A identidade do chamador é a identidade associada a uma chamada de método. A identidade do chamador é usada pela segurança baseada em função e está presente no contexto de chamada de segurança. Em componentes na fila, a identidade do chamador é representada como dados na mensagem En en fila de mensagens. O En fila de mensagens autentica a identidade do remetente da mensagem. Quando a identidade do chamador e a identidade do remetente da mensagem são as mesmas, o Ensuamento de Mensagens autentica a mensagem e o chamador. Esse é o caso comum.

> [!Note]  
> Os componentes em fila COM+ não são suportados com segurança no estilo de representação, o que permite que um servidor obtenha um token de acesso correspondente à identidade do cliente e use-o para executar verificações de controle de acesso ou agir no contexto de segurança do cliente.

 

Quando o chamador de um componente na fila está interagindo com o componente por meio de um gravador fora do processo, as identidades do chamador e do remetente da mensagem (gravador) podem ser diferentes. Nesse caso, os componentes em fila COM+ verificam se o remetente da mensagem é membro da função usuário confiável do QC no servidor. Além disso, o gravador fora do processo requer um certificado de autenticação porque ele está sendo autenticado pelo Enqueamento de Mensagens.

Os membros da função usuário confiável do QC têm permissão para especificar uma identidade arbitrária, o que significa que um membro mal-intencionado pode executar uma chamada de componente na fila com privilégios elevados. Portanto, é recomendável que o número desses usuários seja mantido no mínimo absoluto.

Devido ao risco de um ataque sofisticado associado a qualquer mecanismo que propague a identidade em uma rede, bem como o risco de um ataque de negação de serviço simples inundando as filas com solicitações inexecutáveis, é recomendável implantar o serviço de componentes em fila COM+ somente em uma rede de hosts confiáveis, por exemplo,  em uma rede privada ou em uma rede virtual privada ou atrás de um firewall configurado adequadamente.

Os componentes em fila COM+ são executados no DCOM, portanto, você pode  ajudar a  proteger a integridade  e o sigilo de chamadas de método en fila selecionando Privacidade do Pacote como a configuração Nível de Autenticação de Chamadas na guia Segurança da folha Propriedades do aplicativo na fila. 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança COM+](com--security.md)
</dt> <dt>

[Limitações de segurança no modo de grupo de trabalho](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Especificando o protocolo de autenticação](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



