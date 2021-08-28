---
title: Usando comandos de script com suporte Windows Media Player
description: Usando comandos de script com suporte Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows SDK de Formato de Mídia, comandos de script
- Windows SDK de formato de mídia, Windows Media Player
- FORMATO DE SISTEMAS Avançados (ASF), comandos de script
- ASF (Formato de Sistemas Avançados), comandos de script
- ASF (Advanced Systems Format), Windows Media Player
- ASF (formato de sistemas avançados), Windows Media Player
- scripts, comandos
- scripts, Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58709af99cb4ebcb4eaba64fa6bb167b0ca80acb3fcb21b34efe4a55e2bacf12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110066"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Usando comandos de script com suporte Windows Media Player

O Windows SDK de Formato de Mídia não fornece suporte nativo para análise e resposta a comandos de script. Você deve incluir qualquer lógica relacionada aos comandos de script em seu aplicativo. Os tipos de script que você usa também devem ser definidos em seu aplicativo.

Você pode incluir código para lidar com os mesmos comandos de script com suporte do Windows Media Player. Manter a compatibilidade com Windows Media Player torna seus arquivos mais universais do que se você inserir comandos de script personalizado.

A tabela a seguir lista os tipos de script com suporte pelo Windows Media Player.



| Tipo de script | Descrição                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | O player envia a URL especificada para o navegador para exibição ao usuário. Se um controle de player inserido estiver sendo usado, você poderá adicionar uma referência de quadro específica à URL usando a sintaxe &&*framename.*                                                                             |
| Filename    | Uma URL para outro arquivo de mídia a ser tocada.                                                                                                                                                                                                                                                |
| CAPTION     | Uma cadeia de caracteres de texto que é exibida na área de legendas Windows Media Player. Esse tipo dá suporte à formatação HTML padrão, para que o texto possa ser formatado como desejar. Um exemplo de uso é a legenda fechada.                                                                             |
| Evento       | O nome de um evento que deve ocorrer. O tipo EVENT dá suporte à personalização para seus próprios usos. O código para o evento especificado deve ser definido no metadado Windows Media do fluxo para que o player execute o evento especificado. Um exemplo de uso é a inserção de ad. |
| Openevent   | Esse script precede o EVENT real. O OPENEVENT permite que o player pré-buffer do conteúdo para que, quando o EVENTO ocorra, a alternância entre fluxos pareça ser perfeita.                                                                                                       |
| TEXT        | Uma cadeia de caracteres TEXT que é exibida na área de legendas Windows Media Player. Pode ser texto sem formatação, SAMI ou texto formatado em HTML.                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




