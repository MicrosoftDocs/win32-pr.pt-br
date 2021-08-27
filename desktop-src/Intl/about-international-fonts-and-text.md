---
description: Os tópicos nesta seção abordam a funcionalidade básica de Fontes Internacionais.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Gerenciamento internacional de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4c44661b234a95abb4d40f2204382b3d074bf1d7c0bb1c68a241345211695f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083046"
---
# <a name="international-font-management"></a>Gerenciamento internacional de fontes

Os tópicos nesta seção abordam a funcionalidade básica de Fontes Internacionais. Para obter instruções sobre como usar a tecnologia de fonte internacional em seus aplicativos, consulte [Enumeração](using-international-fonts-and-text.md) e seleção de fontes internacionais e Usando Dlg do MS Shell e [MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).

## <a name="font-management-infrastructure"></a>Infraestrutura de Gerenciamento de Fontes

A partir Windows 7, a infraestrutura de gerenciamento de fontes dá suporte à ocultação de fontes que não são apropriadas para listas de seleção de fontes de um usuário. As configurações padrão do sistema optarão por ocultar automaticamente as fontes que não foram projetadas para as linguagens de entrada (teclados) habilitadas no sistema operacional. Além disso, os usuários podem optar por ocultar manualmente as fontes no Painel de Controle. Esse recurso significa que os usuários não precisam mais se deparar com longas listas de fontes inadequadas e é particularmente valioso para usuários internacionais que trabalham em scripts não latinos.

No Windows 7, não há APIs para consultar diretamente quais fontes estão ocultas ou para definir fontes a serem ocultas. No entanto, isso não significa que você não pode aproveitar esse recurso em seu aplicativo. Se você usar a API Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) (caixa de diálogo Comum da fonte) para habilitar a seleção de fonte hoje, você obterá o novo comportamento gratuitamente. A nova faixa Windows faixa de opções (Controles de Fonte) introduzida no Windows 7 também dá suporte a esse comportamento e fornece outro motivo para "Faixa de opções" para seus aplicativos. Para obter detalhes sobre como usar controles de fonte na Faixa de Opções e **EscolherFont** para exibir fontes ao filtrar as fontes ocultas, consulte Enumeração e seleção de fontes [internacionais.](using-international-fonts-and-text.md)

Observe que ocultar fontes afeta apenas a interface do usuário de seleção de fonte. Ele não afeta as APIs de desenho. Quando uma fonte é selecionada em um contexto de dispositivo, não há nenhum efeito no desenho devido à fonte estar oculta. A [**função EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) continua enumerando fontes definidas como ocultas.

## <a name="gdi-font-embedding-and-subsetting"></a>Incorporação e subconjunto de fonte GDI

A tecnologia International Fonts usa a Biblioteca de Serviços de Incorporação de Fonte para permitir que você adote fontes TrueType e OpenType em um documento ou arquivo. A incorporação de uma fonte em um arquivo garante que a fonte estará presente no computador que está recebendo o arquivo. Para obter mais informações, consulte [Referência de incorporação de fonte.](../gdi/font-embedding-reference.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumeração e seleção de fontes internacionais](using-international-fonts-and-text.md)
</dt> <dt>

[Usando o MS Shell Dlg e o MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Referência de incorporação de fonte](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
