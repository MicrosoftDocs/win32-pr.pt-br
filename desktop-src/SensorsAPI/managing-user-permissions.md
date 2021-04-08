---
description: A API do sensor fornece um método que você pode usar para solicitar permissões ao usuário para usar um sensor ou uma coleção de sensores.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Gerenciando permissões de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb65fa5a9962be4850aa4711cafa03fb7658212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920804"
---
# <a name="managing-user-permissions"></a>Gerenciando permissões de usuário

A API do sensor fornece um método que você pode usar para solicitar permissões ao usuário para usar um sensor ou uma coleção de sensores.

Como os sensores podem revelar informações confidenciais, o Windows exige que os usuários habilitem os sensores antes que o programa possa acessar os dados.

Talvez você queira solicitar permissão quando quiser usar sensores para os quais o [**sensorstate**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) atual é \_ \_ acesso negado ao estado do sensor \_ .

Para solicitar permissões, chame o método [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) . Quando você chama esse método, o Windows abre a caixa de diálogo **habilitar sensores** para solicitar que o usuário habilite os sensores solicitados. Essa caixa de diálogo fornece ao usuário os nomes dos sensores que você solicitou. O usuário pode escolher uma das seguintes opções:

-   **Habilite esses sensores**.
-   **Não habilite esses sensores**.
-   **Abra o painel de controle para obter mais opções**.

Se um usuário optar por **não habilitar esses sensores**, o Windows não mostrará a caixa de diálogo **habilitar sensores** novamente para esses sensores específicos, mesmo que seu programa chame [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions). Se o usuário escolher qualquer outra opção, o Windows permitirá que a caixa de diálogo seja exibida quando solicitado. Se sua chamada para **RequestPermissions** contiver alguns sensores que o usuário escolheu anteriormente para manter desabilitado, a API do sensor removerá esses sensores da lista de sensores que o usuário vê.

### <a name="modal-or-modeless-behavior"></a>Comportamento modal ou sem janela restrita

O método [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) usa um argumento **booliano** que determina se a caixa de diálogo **habilitar sensores** é exibida como uma janela modal ou sem-modo. Essa configuração também afeta se o comportamento do código de retorno da caixa de diálogo é síncrono ou assíncrono.

Quando modal, a caixa de diálogo tem foco exclusivo entre janelas de aplicativo até que o usuário escolha uma opção e o código de retorno **HRESULT** de sua chamada para [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indica a opção do usuário. Quando sem janela restrita, a caixa de diálogo não tem foco exclusivo e sua chamada para **RequestPermissions** retorna imediatamente. Nesse caso, o código de retorno indica se o método foi bem-sucedido, mas não pode ser usado para determinar a escolha do usuário. Em seguida, você pode determinar quais sensores foram habilitados manipulando o evento [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) e verificando cada sensor para o estado do sensor \_ \_ pronto.

Para obter mais informações sobre códigos de retorno, consulte a página de referência do [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) .

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Prática recomendada: Evite várias chamadas sem janela restrita para RequestPermissions

As chamadas modeladas repetidamente para [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) exibirão várias instâncias da caixa de diálogo **habilitar esses sensores** e poderão inundar a tela com caixas de diálogo, resultando em uma experiência de usuário ruim. Se você pensa que, após sua primeira chamada para **RequestPermissions**, outros sensores de localização podem ser instalados, exigindo outra chamada para **RequestPermissions**, você deve chamar **RequestPermissions** modalmente ou aguardar até que todos os sensores de localização sejam instalados para fazer uma chamada sem janela restrita.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Privacidade e segurança na plataforma de sensor e local](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Solicitando permissões de usuário](requesting-user-permissions.md)
</dt> </dl>

 

 
