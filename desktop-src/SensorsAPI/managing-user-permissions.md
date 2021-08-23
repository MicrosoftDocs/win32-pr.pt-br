---
description: A API do Sensor fornece um método que você pode usar para solicitar ao usuário permissões para usar um sensor ou coleção de sensores.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Gerenciando permissões de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02fac57959b493683d0fe0a007602e5a7af3f78dc959d0e7eca2811595c23dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576246"
---
# <a name="managing-user-permissions"></a>Gerenciando permissões de usuário

A API do Sensor fornece um método que você pode usar para solicitar ao usuário permissões para usar um sensor ou coleção de sensores.

Como os sensores podem revelar informações confidenciais, Windows requer que os usuários habilitam sensores antes que seu programa possa acessar qualquer dado.

Talvez você queira solicitar permissão quando quiser usar sensores para os quais o [**SensorState**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) atual é SENSOR \_ STATE ACCESS \_ \_ NEGADO.

Para solicitar permissões, chame o [**método ISensorManager::RequestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Quando você chama esse método, Windows  a caixa de diálogo Habilitar sensores para solicitar que o usuário habilita os sensores solicitados. Essa caixa de diálogo fornece ao usuário os nomes dos sensores solicitados. O usuário pode escolher uma das seguintes opções:

-   **Habilita esses sensores**.
-   **Não habilita esses sensores.**
-   **Abra Painel de Controle para obter mais opções.**

Se um usuário escolher Não habilitar esses **sensores,** o  Windows mostrará a caixa de diálogo Habilitar sensores novamente para esses sensores específicos, mesmo se o programa chamar [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions). Se o usuário escolher qualquer outra opção, Windows permitirá que a caixa de diálogo seja exibida quando solicitado. Se sua chamada para **RequestPermissions** contiver alguns sensores que o usuário optou anteriormente por manter desabilitado, a API do Sensor removerá esses sensores da lista de sensores que o usuário vê.

### <a name="modal-or-modeless-behavior"></a>Comportamento modal ou sem modo

O [**método RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) usa um argumento **booliana** que determina se a caixa de diálogo Habilitar sensores é exibida como uma janela modal ou sem modo.  Essa configuração também afeta se o comportamento do código de retorno da caixa de diálogo é síncrono ou assíncrono.

Quando modal, a caixa de diálogo tem foco exclusivo entre as janelas do aplicativo até que o usuário escolha uma opção e o código de retorno **HRESULT** de sua chamada para [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indica a escolha do usuário. Quando sem modo, a caixa de diálogo não tem foco exclusivo e sua chamada para **RequestPermissions** retorna imediatamente. Nesse caso, o código de retorno indica se o método foi bem-sucedido, mas não pode ser usado para determinar a escolha do usuário. Em seguida, você pode determinar quais sensores foram habilitados manipulando o [**evento OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) e verificando cada sensor para SENSOR \_ STATE \_ READY.

Para obter mais informações sobre códigos de retorno, consulte a página de [**referência RequestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Melhor prática: evitar várias chamadas sem modo para RequestPermissions

Chamadas sem modo repetidas para [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)  exibirão várias instâncias da caixa de diálogo Habilitar esses sensores e poderão inundar a tela com caixas de diálogo, resultando em uma experiência ruim do usuário. Se você achar que, após sua primeira chamada para **RequestPermissions**, outros sensores de localização poderão ser instalados, exigindo outra chamada para **RequestPermissions**, você deverá chamar **RequestPermissions** de forma modicamente ou aguardar até que todos os sensores de localização sejam instalados para fazer uma chamada sem modo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Privacidade e segurança na plataforma sensor e localização](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Solicitando permissões de usuário](requesting-user-permissions.md)
</dt> </dl>

 

 
