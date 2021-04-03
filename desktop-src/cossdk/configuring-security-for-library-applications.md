---
description: Há considerações especiais na configuração da segurança baseada em funções e da autenticação para aplicativos de biblioteca.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Configuração da segurança para aplicativos de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102d6a0f102bfd19da0073bca14df8a8211203b1
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103930048"
---
# <a name="configuring-security-for-library-applications"></a>Configuração da segurança para aplicativos de biblioteca

Há considerações especiais na configuração da segurança baseada em funções e da autenticação para aplicativos de biblioteca.

## <a name="enabling-or-disabling-authentication"></a>Habilitando ou desabilitando a autenticação

Um dos fatores a considerar é se os chamadores do aplicativo de biblioteca devem estar sujeitos às verificações de segurança no nível de processo do processo de hospedagem, ou seja, se deseja habilitar ou desabilitar a autenticação.

Por exemplo, se o aplicativo de biblioteca for hospedado por um navegador, talvez seja necessário receber retornos de chamada não autenticados. Para atender a essa necessidade, você pode desabilitar a autenticação para que o processo de hospedagem não execute verificações de segurança para os chamadores do aplicativo de biblioteca. Quando você desabilita a autenticação, o aplicativo de biblioteca deixa de ser autenticado de forma efetiva – todas as chamadas para ele terão sucesso. Os chamadores do aplicativo de biblioteca não estão sujeitos às verificações de segurança do processo de hospedagem. Basicamente, o aplicativo de biblioteca é marcado como "não autenticado" e as verificações de segurança são omitidas para chamadas ao aplicativo de biblioteca.

Para obter informações sobre como habilitar ou desabilitar a autenticação, consulte [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).

## <a name="enforcing-role-checks"></a>Impondo verificações de função

Outra decisão a ser tomada é se o aplicativo de biblioteca deve usar a [segurança baseada em função](role-based-security-administration.md). Se a segurança baseada em funções for usada, você deverá usar a segurança em nível de componente para qualquer verificação de acesso a ser executada. As funções atribuídas ao aplicativo de biblioteca não são refletidas no descritor de segurança do processo. A única autorização que o aplicativo de biblioteca pode controlar está no nível de componente. Para obter mais informações sobre segurança em nível de componente, consulte [limites de segurança](security-boundaries.md).

Para ver como definir a segurança em nível de componente, consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).

## <a name="configuration-scenarios"></a>Cenários de configuração

Para entender melhor as implicações de decidir se o aplicativo de biblioteca deve usar a segurança baseada em função e se o aplicativo de biblioteca deve ser autenticado, considere os seguintes cenários:

-   **A autenticação está habilitada e a segurança baseada em função é usada.** Nesse cenário, as verificações de segurança são feitas pelo processo de hospedagem e alguns chamadores têm acesso negado no nível do processo. Além disso, a verificação de função é feita no nível do aplicativo de biblioteca para que alguns chamadores que o fizerem por meio da verificação de segurança em nível de processo tenham acesso negado ao aplicativo de biblioteca quando a associação de função estiver marcada. Este é o cenário comum para um aplicativo de biblioteca COM+ que usa a segurança baseada em função.

    A ilustração a seguir mostra o cenário em que a autenticação está habilitada e a verificação de função é usada.

    ![Diagrama que mostra a autenticação que ocorre em um processo de host.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **A autenticação está habilitada e a segurança baseada em função não é usada.** Nesse cenário, as verificações de segurança são feitas no nível do processo, mas a associação de função não é verificada no nível do aplicativo de biblioteca. Portanto, qualquer chamador do aplicativo de biblioteca que o fizer pela verificação de segurança em nível de processo receberá acesso ao aplicativo de biblioteca porque a associação de função não está sendo verificada. Essa situação existe quando um aplicativo COM que não usa a segurança baseada em função é migrado para um aplicativo de biblioteca COM+.

    A ilustração a seguir mostra o cenário em que a autenticação está habilitada e a verificação de função não está sendo usada.

    ![Diagrama que mostra a autenticação de nível de processo para um aplicativo de biblioteca dentro do processo de host.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **A autenticação está desabilitada e a segurança baseada em função é usada.** Nesse cenário, as verificações de segurança estão sendo feitas no nível do processo, mas os chamadores para o aplicativo de biblioteca não são autenticados. Na verdade, os chamadores do aplicativo de biblioteca são isentos da verificação de segurança em nível de processo. Como a verificação de função está habilitada, a associação de função sozinho determina quem recebe acesso ao aplicativo de biblioteca. Esse cenário pode ser apropriado quando a verificação de segurança que seria feita pelo processo de hospedagem é muito restritiva, mas você precisa ter alguma restrição de acesso no aplicativo de biblioteca ou em interfaces ou métodos específicos. Esse cenário permite que você desative efetivamente a segurança do processo e ainda tenha verificações de acesso de nível apropriadas usando a segurança baseada em funções.

    O cenário em que a autenticação está desabilitada e a verificação de função está sendo usada é mostrada na ilustração a seguir.

    ![Diagrama que mostra ' verificar associação de função ' em um aplicativo de biblioteca em um processo de host.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **A autenticação está desabilitada e a segurança baseada em função não é usada.** Nesse cenário, as verificações de segurança ainda são feitas no nível do processo, mas, como no cenário anterior, os chamadores do aplicativo de biblioteca sempre passam essa verificação de segurança. Como a verificação de função também está desabilitada, a associação de função não é verificada no nível do aplicativo de biblioteca. Essencialmente, qualquer pessoa pode chamar o aplicativo de biblioteca. Esse cenário deve ser escolhido quando o objeto COM precisa receber retornos de chamada não autenticados, como pode ser o caso com um controle ActiveX hospedado pelo Internet Explorer e com um snap-in do console de gerenciamento Microsoft. É claro que esse objeto COM deve ser confiável para se comportar adequadamente ao receber chamadas não autenticadas. Por exemplo, ele não deve acessar arquivos arbitrários em nome de seus chamadores.

    O cenário em que a autenticação está desabilitada e a verificação de função não está sendo usada é mostrada na ilustração a seguir.

    ![Diagrama que mostra chamadas para um aplicativo de biblioteca que não está autenticado no processo de host.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Depois de decidir se deseja habilitar ou desabilitar a autenticação para seu aplicativo de biblioteca COM+, consulte [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md) para um procedimento passo a passo que explica como desabilitar (ou habilitar) a autenticação usando a ferramenta administrativa serviços de componentes. Se o aplicativo de biblioteca usar a segurança baseada em função, consulte [Configurando Role-Based segurança](configuring-role-based-security.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança de aplicativos de biblioteca](library-application-security.md)
</dt> </dl>

 

 



