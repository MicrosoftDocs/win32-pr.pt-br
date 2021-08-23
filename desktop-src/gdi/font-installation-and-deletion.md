---
description: Um aplicativo pode usar uma fonte para desenhar texto somente se essa fonte estiver residente em um dispositivo especificado ou instalado na tabela de fontes do sistema.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Instalação e exclusão de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112cfbff6bebdfc2fa4d46993f1fa60dcc19285bc3e16ebc2fd929e3a43ba679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037924"
---
# <a name="font-installation-and-deletion"></a>Instalação e exclusão de fontes

Um aplicativo pode usar uma fonte para desenhar texto somente se essa fonte estiver residente em um dispositivo especificado ou instalado na tabela de fontes do sistema. A tabela de fontes é uma matriz interna que identifica todas as fontes que não são do dispositivo que estão disponíveis para um aplicativo. Um aplicativo pode recuperar os nomes das fontes atualmente instaladas em um dispositivo ou armazenadas na tabela de fontes internas chamando as funções [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) ou [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) .

Para instalar uma fonte temporariamente, chame [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa). Essas funções carregam uma fonte que é armazenada em um arquivo de recurso de fonte. No entanto, essa é uma instalação temporária porque, após uma reinicialização, a fonte não estará presente.

Para instalar uma fonte que permanecerá após a reinicialização do sistema, use um dos seguintes métodos:

-   Vá para o painel de controle, clique no ícone **fontes** e selecione **instalar novas fontes** no menu **arquivo** . A fonte está disponível para um aplicativo mesmo antes da reinicialização. No entanto, em uma situação de servidor de terminal, a fonte está disponível para a sessão atual, mas não está disponível para outras sessões até após uma reinicialização.
-   Copie a fonte na pasta% windir% \\ fonts. Em seguida, vá para o painel de controle e clique no ícone **fontes** ou chame [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa). A fonte está disponível para um aplicativo mesmo antes da reinicialização. No entanto, em uma situação de servidor de terminal, a fonte está disponível para a sessão atual, mas não está disponível para outras sessões até após uma reinicialização. Se você copiar apenas a fonte na pasta% windir% \\ fonts, a fonte estará disponível somente depois que o sistema for reinicializado.

Quando um aplicativo termina de usar uma fonte instalada, ele deve remover essa fonte chamando a função [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) .

Uma fonte instalada a partir de um local diferente da pasta% windir% \\ fonts não pode ser modificada quando carregada em qualquer sessão ativa, incluindo a sessão 0. Qualquer tentativa de alterar, substituir ou excluir, portanto, será bloqueada. Se a modificação para uma fonte for necessária:

-   *Fontes temporárias* são carregadas apenas na sessão atual. Antes de tentar qualquer modificação de fonte, chame [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) para forçar a sessão atual a descarregar a fonte.
-   As *fontes permanentes* permanecem instaladas após a reinicialização e são carregadas por todas as sessões criadas. Chame [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) para forçar a sessão atual a descarregar a fonte. em seguida, na chave do registro da fonte (**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ fonts**), localize e remova o valor do registro associado à fonte. Por fim, reinicialize o computador para garantir que a fonte não seja carregada em nenhuma sessão. Após a reinicialização, continue com sua modificação/exclusão de fonte.

Sempre que um aplicativo chama as funções que adicionam e excluem recursos de fonte, ele também deve chamar a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) e enviar uma mensagem do [**WM \_ FONTCHANGE**](wm-fontchange.md) para todas as janelas de nível superior no sistema. Essa mensagem notifica outros aplicativos de que a tabela de fontes interna foi alterada por um aplicativo que adicionou ou removeu uma fonte.

 

 
