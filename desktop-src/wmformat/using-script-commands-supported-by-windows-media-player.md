---
title: Usando comandos de script com suporte no Windows Media Player
description: Usando comandos de script com suporte no Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- SDK do Windows Media Format, comandos de script
- SDK do Windows Media Format, Windows Media Player
- ASF (Advanced Systems Format), comandos de script
- ASF (formato de sistemas avançados), comandos de script
- ASF (Advanced Systems Format), Windows Media Player
- ASF (formato de sistemas avançados), Windows Media Player
- scripts, comandos
- scripts, Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005602"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Usando comandos de script com suporte no Windows Media Player

O Windows Media Format SDK não fornece suporte nativo para análise e resposta a comandos de script. Você deve incluir qualquer lógica relacionada aos comandos de script em seu aplicativo. Os tipos de script que você usa também devem ser definidos em seu aplicativo.

Você pode incluir código para lidar com os mesmos comandos de script suportados pelo Windows Media Player. Manter a compatibilidade com o Windows Media Player torna seus arquivos mais universais do que se você inserir comandos de script personalizados.

A tabela a seguir lista os tipos de script que têm suporte do Windows Media Player.



| Tipo de script | Descrição                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | O Player envia a URL especificada para o navegador para exibição para o usuário. Se um controle de Player inserido estiver sendo usado, você poderá adicionar uma referência de quadro específica à URL usando a sintaxe &&*FrameName* .                                                                             |
| NOME do arquivo    | Uma URL para outro arquivo de mídia a ser reproduzido.                                                                                                                                                                                                                                                |
| CAPTION     | Uma cadeia de texto que é exibida na área de legendas do Windows Media Player. Esse tipo dá suporte à formatação HTML padrão, portanto, o texto pode ser formatado como desejar. Um exemplo de uso é a legendagem oculta.                                                                             |
| CIRCUNSTÂNCIA       | O nome de um evento que deve ocorrer. O tipo de evento dá suporte à personalização para seus próprios usos. O código para o evento especificado deve ser definido no metarquivo do Windows Media para o fluxo para que o Player execute o evento especificado. Um exemplo de uso é a inserção de anúncios. |
| OPENEVENT   | Esse script precede o evento real. O OPENEVENT permite que o Player bufferu previamente o conteúdo para que, quando o evento ocorrer, a mudança entre os fluxos pareça ser direta.                                                                                                       |
| TEXT        | Uma cadeia de texto que é exibida na área de legendas do Windows Media Player. Pode ser texto sem formatação, SAMI ou HTML formatado.                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




