---
title: Configurações de registro de esquema personalizado
description: Configurações de registro de esquema personalizado
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, configurações de registro de esquema personalizado
- Windows Media Player, esquemas
- Windows Media Player, registro
- registro, configurações de esquema personalizado
- registro, esquemas
- registro, configurações para Windows Media Player
- esquemas
- configurações do registro de esquema personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1f20b69570a18d256049bb0e785099e43b091d080e4f9f65e62655c3103d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750389"
---
# <a name="custom-scheme-registry-settings"></a>Configurações de registro de esquema personalizado

Os esquemas são protocolos personalizados. Windows Media Player mantém uma lista de esquemas no registro no computador do usuário. quando o usuário tenta reproduzir um arquivo de mídia digital, o Player verifica primeiro se o SDK do formato de mídia Windows dá suporte ao esquema. Caso contrário, o Player verificará o esquema em relação à lista no registro. se uma correspondência for encontrada, o Player verificará um valor que indica qual tecnologia subjacente ou *tempo de execução* (como o Microsoft DirectShow ou o Windows Media Format SDK) pode ser usado para reproduzir o arquivo. Se nenhuma correspondência for encontrada, o Player apresentará ao usuário uma caixa de diálogo de aviso que solicita ao usuário a permissão para tentar reproduzir o arquivo. Se você transmitir arquivos de mídia digital usando um esquema de protocolo personalizado, poderá evitar que esse aviso apareça no computador do usuário registrando o esquema e fornecendo um valor para o tempo de execução.

A lista de esquemas é mantida como um conjunto de chaves do registro que correspondem aos esquemas registrados, sem os dois-pontos e as duas barras (://). Por exemplo, a chave para o esquema wmhtml://, que é usada para transmitir mídia avançada, é denominada "wmhtml". Uma lista separada é mantida para o computador local e para cada usuário. Para o computador local, as chaves de esquema são subchaves da seguinte chave do registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Schemes\\**

Por exemplo, a chave do esquema wmhtml://para o computador local é:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Schemes \\ wmhtml**

Para alterar os valores nessa chave ou criar uma nova subchave, o usuário atual deve ser um administrador do computador.

Para usuários individuais, as chaves de esquema são subchaves da seguinte chave do registro:

**HKEY \_ atual \_ \\ software \\ do usuário \\ esquema do Microsoft MediaPlayer \\ Player \\\\**

Por exemplo, a chave para o esquema wmhtml://para o usuário atual é:

**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ Schemes \\ wmhtml**

Ao procurar esquemas registrados, o Player primeiro verifica os valores localizados em **HKEY \_ local \_ Machine**. Se nenhum for encontrado para o esquema atual, o Player em seguida verificará os valores em **HKEY \_ Current \_ User**. Se nenhum for encontrado para o esquema atual, o Player exibirá o aviso para o usuário.

Cada subchave de esquema pode conter um dos seguintes valores possíveis para *tempo de execução*.



| Valor | Descrição                                |
|-------|--------------------------------------------|
| 6     | renderizar usando o SDK do formato de mídia Windows. |
| 7     | Renderizar usando o Microsoft DirectShow.         |



 

alterar o valor de *tempo de execução* para um esquema ao qual o SDK do formato de mídia Windows dá suporte não terá nenhum efeito. o Player sempre usará o sdk do formato de mídia Windows como o tempo de execução para esquemas aos quais o sdk do formato de mídia do Windows dá suporte. Esse valor de registro foi projetado para permitir a configuração de tempo de execução para esquemas personalizados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do Registro**](registry-settings.md)
</dt> </dl>

 

 




