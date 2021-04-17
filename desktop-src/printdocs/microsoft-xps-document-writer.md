---
description: O Microsoft XPS Document Writer (MXDW) é um driver de impressão para arquivo que permite que um aplicativo do Windows Crie arquivos de documento XPS (XML Paper Specification) em versões do Windows a partir do Windows XP com Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Gravador de documento XPS da Microsoft (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760989"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Gravador de documento XPS da Microsoft (MXDW)

O Microsoft XPS Document Writer (MXDW) é um driver de impressão para arquivo que permite que um aplicativo do Windows Crie arquivos de documento XPS (XML Paper Specification) em versões do Windows a partir do Windows XP com Service Pack 2 (SP2). Usar o MXDW possibilita que um aplicativo do Windows salve seu conteúdo como um documento XPS sem alterar qualquer código do programa do aplicativo.

## <a name="when-to-use"></a>Quando usar

Como usuário, você deve selecionar o MXDW quando quiser criar um documento XPS a partir de um aplicativo do Windows que não tem a opção de salvar seu conteúdo como um documento XPS.

Como desenvolvedor de aplicativos, você recomendaria o MXDW a usuários que desejam criar documentos XPS quando seu aplicativo não oferecer a opção de salvar como um documento XPS. Para obter mais informações sobre a especificação de papel XML e documentos XPS, consulte [especificação de documento XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) e a [especificação XPS e downloads de licenças](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

O MXDW é instalado automaticamente no Windows Vista e em versões posteriores do Windows e pode ser baixado e instalado no Windows XP com SP2 e Windows Server 2003.

## <a name="installation"></a>Instalação

No Windows Vista e versões posteriores do Windows, o MXDW é instalado automaticamente quando o sistema operacional é instalado.

**Windows XP com SP2 e Windows Server 2003**: Baixe e instale o .net Framework 3,0 ou o pacote XPS Essential do [centro de download da Microsoft](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Como usar

Quando instalado, o MXDW aparece como uma fila de impressão disponível na caixa de diálogo Imprimir apresentada por um aplicativo. Quando o MXDW é selecionado como a impressora, é solicitado que o nome do arquivo seja criado como o documento XPS que captura a saída de impressão do aplicativo.

A imagem a seguir mostra o MXDW que está sendo selecionado como a impressora na caixa de diálogo impressão comum do Windows Vista.

![uma imagem da caixa de diálogo de impressão que mostra a seleção do Microsoft XPS Document Writer (MXDW)](images/choosingmxdwinvista.gif)

Os desenvolvedores de aplicativos podem personalizar a saída de MXDW usando as [definições de configuração do MXDW](mxdw-configuration-settings.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Downloads de licença e de especificação XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Ferramenta de conformidade do isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[Definições de configuração do MXDW](mxdw-configuration-settings.md)
</dt> </dl>

 

 
