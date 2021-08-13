---
description: Há considerações especiais sobre como configurar a segurança baseada em função e a autenticação para aplicativos de biblioteca.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Configuração da segurança para aplicativos de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0d8b3993a00512c20409f1f029b7402d5f9ace97984cbe9757453b5672125f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548867"
---
# <a name="configuring-security-for-library-applications"></a>Configuração da segurança para aplicativos de biblioteca

Há considerações especiais sobre como configurar a segurança baseada em função e a autenticação para aplicativos de biblioteca.

## <a name="enabling-or-disabling-authentication"></a>Habilitando ou desabilitando a autenticação

Um dos fatores a serem considerados é se os chamadores do aplicativo de biblioteca devem estar sujeitos às verificações de segurança no nível do processo do processo de hospedagem, ou seja, se a autenticação deve ser habilitada ou desabilitada.

Por exemplo, se o aplicativo de biblioteca for hospedado por um navegador, talvez seja necessário receber retornos de chamada não autenticados. Para atender a essa necessidade, você pode desabilitar a autenticação para que o processo de hospedagem não execute verificações de segurança para chamadores do aplicativo de biblioteca. Quando você desabilita a autenticação, o aplicativo de biblioteca efetivamente fica não autenticado– todas as chamadas para ele terão êxito. Os chamadores do aplicativo de biblioteca não estão sujeitos às verificações de segurança do processo de hospedagem. Basicamente, o aplicativo de biblioteca é marcado como "não autenticado", e as verificações de segurança são omitidas para chamadas ao aplicativo de biblioteca.

Para obter informações sobre como habilitar ou desabilitar a autenticação, consulte [Habilitando a autenticação para um aplicativo de biblioteca.](enabling-authentication-for-a-library-application.md)

## <a name="enforcing-role-checks"></a>Impondo verificações de função

Outra decisão a ser tomada é se o aplicativo de biblioteca deve usar [a segurança baseada em função](role-based-security-administration.md). Se a segurança baseada em função for usada, você deverá usar a segurança no nível do componente para que as verificações de acesso sejam executadas. As funções atribuídas ao aplicativo de biblioteca não são refletidas no descritor de segurança do processo. A única autorização que o aplicativo de biblioteca pode controlar é no nível do componente. Para obter mais informações sobre a segurança no nível do componente, consulte [Limites de segurança](security-boundaries.md).

Para ver como definir a segurança no nível do componente, consulte [Definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).

## <a name="configuration-scenarios"></a>Cenários de configuração

Para entender melhor as implicações de decidir se o aplicativo de biblioteca deve usar a segurança baseada em função e se o aplicativo de biblioteca deve ser não autenticado, considere os seguintes cenários:

-   **A autenticação está habilitada e a segurança baseada em função é usada.** Nesse cenário, as verificações de segurança são feitas pelo processo de hospedagem e alguns chamadores têm acesso negado no nível do processo. Além disso, a verificação de função é feita no nível do aplicativo de biblioteca para que alguns chamadores que fazem isso por meio da verificação de segurança no nível do processo tenham o acesso negado ao aplicativo de biblioteca quando a associação de função for verificada. Esse é o cenário comum para um aplicativo de biblioteca COM+ que usa segurança baseada em função.

    A ilustração a seguir mostra o cenário em que a autenticação está habilitada e a verificação de função é usada.

    ![Diagrama que mostra a autenticação que ocorre em um processo de host.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **A autenticação está habilitada e a segurança baseada em função não é usada.** Nesse cenário, as verificações de segurança são feitas no nível do processo, mas a associação de função não é verificada no nível do aplicativo de biblioteca. Portanto, qualquer chamador do aplicativo de biblioteca que o fizer por meio da verificação de segurança no nível do processo receberá acesso ao aplicativo de biblioteca porque a associação de função não está sendo verificada. Essa situação existiria quando um aplicativo COM que não usa a segurança baseada em função fosse migrado para um aplicativo de biblioteca COM+.

    A ilustração a seguir mostra o cenário em que a autenticação está habilitada e a verificação de função não está sendo usada.

    ![Diagrama que mostra a autenticação em nível de processo para um aplicativo de biblioteca dentro do processo de host.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **A autenticação está desabilitada e a segurança baseada em função é usada.** Nesse cenário, as verificações de segurança estão sendo feitas no nível do processo, mas os chamadores para o aplicativo de biblioteca não são autenticados. Na verdade, os chamadores do aplicativo de biblioteca são isentos da verificação de segurança no nível do processo. Como a verificação de função está habilitada, somente a associação de função determina quem recebe acesso ao aplicativo de biblioteca. Esse cenário pode ser apropriado quando a verificação de segurança que seria feita pelo processo de hospedagem é muito restritiva, mas você precisa ter alguma restrição de acesso no aplicativo de biblioteca ou em interfaces ou métodos específicos. Esse cenário permite que você desligue efetivamente a segurança do processo e ainda tenha verificações de acesso de nível apropriadas usando a segurança baseada em função.

    O cenário em que a autenticação está desabilitada e a verificação de função está sendo usada é mostrada na ilustração a seguir.

    ![Diagrama que mostra 'verificar a associação de função' em um aplicativo de biblioteca dentro de um processo de host.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **A autenticação está desabilitada e a segurança baseada em função não é usada.** Nesse cenário, as verificações de segurança ainda são feitas no nível do processo, mas, assim como no cenário anterior, os chamadores do aplicativo de biblioteca sempre passam por essa verificação de segurança. Como a verificação de função também está desabilitada, a associação de função não é verificada no nível do aplicativo de biblioteca. Essencialmente, qualquer pessoa pode chamar o aplicativo de biblioteca. Esse cenário deve ser escolhido quando o objeto COM precisa receber retornos de chamada não autenticados, como pode ser o caso com um controle ActiveX hospedado pelo Internet Explorer e com um snap-in Console de Gerenciamento Microsoft. É claro que esse objeto COM deve ser confiável para se comportar adequadamente ao receber chamadas não autenticadas. Por exemplo, ele não deve acessar arquivos arbitrários em nome de seus chamadores.

    O cenário em que a autenticação está desabilitada e a verificação de função não está sendo usada é mostrada na ilustração a seguir.

    ![Diagrama que mostra chamadas a um aplicativo de biblioteca que não são autenticados no processo de host.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Depois de decidir se deve habilitar ou desabilitar a autenticação para seu aplicativo de biblioteca COM+, consulte Habilitando a autenticação para um aplicativo de biblioteca para um procedimento passo a passo que explica como desabilitar (ou habilitar) a autenticação usando [a](enabling-authentication-for-a-library-application.md) ferramenta administrativa serviços de componentes. Se o aplicativo de biblioteca usar a segurança baseada em função, consulte [Configurando Role-Based Segurança](configuring-role-based-security.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança do aplicativo de biblioteca](library-application-security.md)
</dt> </dl>

 

 



