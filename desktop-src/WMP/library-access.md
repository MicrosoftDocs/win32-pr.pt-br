---
title: Acesso à biblioteca
description: Acesso à biblioteca
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, acesso
- biblioteca, acessando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292158"
---
# <a name="library-access"></a>Acesso à biblioteca

As propriedades e métodos do modelo de objeto do Windows Media Player que acessam a biblioteca exigem acesso somente leitura ou de leitura/gravação ao banco de dados. A biblioteca contém informações que alguns usuários desejam manter particulares e que devem ser acessados ou alterados somente com seu consentimento.

Para o Windows Media Player 9 Series ou posterior, você pode determinar programaticamente o nível de acesso. Para determinar o nível atual de acesso concedido ao seu código, recupere as *configurações*. Propriedade **mediaAccessRights** . Essa propriedade retorna "None", "Read" ou "Full" (leitura/gravação). Para solicitar direitos de acesso específicos, chame as *configurações*. método **requestMediaAccessRights** , passando um parâmetro que especifica o nível que você está solicitando. O método exibe uma mensagem para o usuário explicando o nível de acesso solicitado e retorna um valor **booliano** que indica se o acesso foi concedido.

Determinados direitos de acesso são concedidos automaticamente dependendo de onde seu código está sendo executado em relação ao computador do usuário.

-   Se a página da Web ou o programa estiver localizado no computador do usuário, os direitos de acesso completo serão concedidos por padrão.
-   Páginas da Web têm acesso de leitura ao *Player*. **currentMedia**, *Player*. **currentPlaylist** e *mídia*. **sourceURL** quando a página da Web está localizada em uma zona de segurança do Internet Explorer que é igual ou menos restrita do que a zona de segurança do item de mídia ou da lista de reprodução.

    Variando do menos restrito ao mais restrito, as zonas de segurança são a zona **confiável** (incluindo o computador local do usuário), a zona **da intranet local** , a zona da **Internet** e a zona **restrita** .

    Por exemplo, uma página da Web na zona **da intranet local** tem direitos de acesso completo ao *Player*. **currentMedia** quando o item de mídia correspondente está na intranet local ou na Internet, mas os direitos de acesso devem ser solicitados para itens de mídia localizados no computador local de um usuário ou em um site na zona **confiável** .

Você deve testar seu aplicativo baseado na Web ou no Windows em todas as zonas de segurança que ele pode encontrar. O aplicativo deve ser criado para lidar com a negação de uma solicitação de acesso corretamente.

As versões do modelo de objeto do Windows Media Player anteriores ao Windows Media Player 9 Series não incluem **mediaAccessRights** ou **requestMediaAccessRights**. Essas versões anteriores do Windows Media Player permitem que o usuário defina níveis de acesso usando a caixa de diálogo **Opções** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> <dt>

[**Trabalhando com a biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




