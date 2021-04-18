---
description: Os tópicos nesta seção abordam a funcionalidade básica de fontes internacionais.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Gerenciamento de fontes internacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759664"
---
# <a name="international-font-management"></a>Gerenciamento de fontes internacionais

Os tópicos nesta seção abordam a funcionalidade básica de fontes internacionais. Para obter instruções sobre como usar a tecnologia de fonte internacional em seus aplicativos, consulte [enumeração e seleção de fontes internacionais](using-international-fonts-and-text.md) e [usando MS Shell Dlg e MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).

## <a name="font-management-infrastructure"></a>Infraestrutura de gerenciamento de fontes

A partir do Windows 7, a infraestrutura de gerenciamento de fontes dá suporte à ocultação de fontes que não são apropriadas para listas de seleção de fontes de um usuário. As configurações padrão do sistema optarão por ocultar automaticamente as fontes que não foram projetadas para os idiomas de entrada (teclados) habilitados no sistema do sistema operacional. Além disso, os usuários podem optar por ocultar manualmente as fontes no painel de controle fontes. Esse recurso significa que os usuários não precisam mais enfrentar listas longas de fontes inadequadas e são especialmente valiosos para usuários internacionais que trabalham em scripts não latinos.

No Windows 7, não há APIs para consultar diretamente quais fontes estão ocultas ou para definir fontes como ocultas. No entanto, isso não significa que você não possa aproveitar esse recurso em seu aplicativo. Se você usar a API [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) do Windows (caixa de diálogo de fonte comum) para habilitar a seleção de fontes hoje, você obterá o novo comportamento gratuitamente. A nova faixa de Cenários do Windows (controles de fonte) introduzida no Windows 7 também dá suporte a esse comportamento e fornece outro motivo para "Ribbonar" seus aplicativos. Para obter detalhes sobre como usar os controles de fonte na faixa de opção e **ChooseFont** para exibir fontes ao filtrar as fontes ocultas, consulte a [enumeração e a seleção de fontes internacionais](using-international-fonts-and-text.md).

Observe que ocultar fontes afeta apenas a interface do usuário de seleção de fontes. Ele não afeta as APIs de desenho. Quando uma fonte é selecionada em um contexto de dispositivo, não há nenhum efeito no desenho devido à fonte que está sendo ocultada. A função [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) continua enumerando fontes definidas como ocultas.

## <a name="gdi-font-embedding-and-subsetting"></a>Incorporação e subconfiguração de fonte GDI

A tecnologia de fontes internacionais usa a biblioteca de serviços de inserção de fontes para permitir que você agrupe fontes TrueType e OpenType em um documento ou arquivo. A inserção de uma fonte em um arquivo garante que a fonte estará presente no computador que está recebendo o arquivo. Para obter mais informações, consulte [referência de inserção de fonte](../gdi/font-embedding-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Seleção e enumeração de fontes internacionais](using-international-fonts-and-text.md)
</dt> <dt>

[Usando MS Shell Dlg e MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Referência de incorporação de fonte](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
