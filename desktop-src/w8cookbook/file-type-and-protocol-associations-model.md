---
title: Tipo de arquivo e modelo de associações de URI
description: Tipo de arquivo e modelo de associações de URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008502"
---
# <a name="file-type-and-uri-associations-model"></a>Tipo de arquivo e modelo de associações de URI

## <a name="platforms"></a>Plataformas

 **Clientes** -Windows 8  
**Servidores** -Windows Server 2012  



## <a name="description"></a>Descrição

O tipo de arquivo e o modelo de associação de URI foram alterados no Windows 8. Os aplicativos não são mais capazes de se definir por meio de programação como o manipulador padrão para um tipo de arquivo ou URI. Em vez disso, agora o usuário controla o que é o manipulador padrão para um tipo de arquivo ou esquema de URI.

## <a name="manifestation"></a>Manifestação

A maneira como essa alteração apresenta ao usuário depende de como o aplicativo foi projetado, por exemplo:

-   Muitos aplicativos verificam se são o padrão sempre que são executados e, se não forem, eles solicitam que o usuário os defina como padrão. No entanto, como os aplicativos não podem mais ser consultados com precisão para determinar qual aplicativo é o manipulador padrão para um tipo de arquivo ou esquema de URI, nenhuma dessas operações funciona.
-   Muitos aplicativos têm uma caixa de diálogo ou menu interno ou em seu instalador que especifica os tipos de arquivo para os quais o aplicativo deve servir como padrão. No entanto, como os aplicativos não podem mais ser definidos por meio de programação como o manipulador padrão para um tipo de arquivo ou esquema de URI, isso não funciona mais.

## <a name="mitigation"></a>Atenuação

Há várias coisas que os usuários podem fazer para acomodar essas alterações:

-   Os usuários são solicitados a escolher um aplicativo padrão para manipular tipos de arquivo, esquemas de URI ou ambos quando um não tiver sido especificado
-   Os usuários recebem a opção de alterar seu manipulador padrão depois de instalar novos aplicativos que podem manipular um tipo de arquivo ou esquema de URI
-   O painel de controle programas padrão permite que os usuários definam padrões para um aplicativo ou para um tipo de arquivo, esquema de URI ou ambos; os aplicativos podem vincular ao painel de controle
-   Os padrões podem ser alterados no Windows Explorer

## <a name="solution"></a>Solução

Como resultado dessas alterações, estas diretrizes de API são fornecidas:

-   A funcionalidade de algumas chamadas de método na API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) foi alterada e não deve mais ser usada.

    -   **Não chame** [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) para determinar se um aplicativo é o padrão
    -   **Não chame** [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) para determinar qual aplicativo (se houver) é o padrão atual
    -   **Não chame** [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) para definir o aplicativo padrão

-   A orientação que avança é:

    -   **Não consultar para** ver qual aplicativo é o manipulador padrão para tipos de arquivo ou esquemas de URI

    -   **Não** tente monitorar as alterações no manipulador padrão para tipos de arquivo ou esquemas de URI

    -   **Não** tente definir um aplicativo como o manipulador padrão para os tipos de arquivo ou esquemas de URI

    -   **Não** tentar gerenciar padrões para tipos de arquivo ou esquemas de URI de dentro de um aplicativo

    -   **Integre com** o painel de controle [definir programas padrão](../shell/default-programs.md) se desejar permitir que os usuários do seu aplicativo acessem a interface do usuário de gerenciamento padrão (a interface do usuário de gerenciamento no aplicativo não tem mais suporte)

        -   Chamar [IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) permite que o usuário acesse a página '[definir programas padrão](../shell/default-programs.md)' do painel de controle para o aplicativo especificado

## <a name="tests"></a>Testes

-   Teste para verificar se os aplicativos são registrados corretamente no painel de controle definir programas padrão
-   Teste para verificar se os aplicativos são registrados corretamente para aparecer na lista de OpenWith para os tipos de arquivo, esquemas de URI ou ambos, que eles registram para manipular
-   Teste para verificar se as novas notificações de aplicativo aparecem depois que seu aplicativo está instalado e o usuário invoca um tipo de arquivo, esquema de URI ou ambos, que seu aplicativo registrou para manipular

## <a name="resources"></a>Recursos

-   [Práticas recomendadas para tipos de arquivo e associações de URI em aplicativos de área de trabalho do Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Associação de tipo de arquivo e apresentação de conferência de Build de reprodução automática](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 