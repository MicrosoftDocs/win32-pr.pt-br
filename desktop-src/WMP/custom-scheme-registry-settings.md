---
title: Configurações do registro de esquema personalizado
description: Configurações do registro de esquema personalizado
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, configurações de registro de esquema personalizado
- Windows Media Player, esquemas
- Windows Media Player, registro
- registro, configurações de esquema personalizado
- registro, esquemas
- registro, configurações do Windows Media Player
- esquemas
- configurações do registro de esquema personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005108"
---
# <a name="custom-scheme-registry-settings"></a>Configurações do registro de esquema personalizado

Os esquemas são protocolos personalizados. O Windows Media Player mantém uma lista de esquemas no registro no computador do usuário. Quando o usuário tenta reproduzir um arquivo de mídia digital, o Player verifica primeiro se o SDK do Windows Media Format dá suporte ao esquema. Caso contrário, o Player verificará o esquema em relação à lista no registro. Se uma correspondência for encontrada, o Player verificará um valor que indica qual tecnologia subjacente ou *tempo de execução* (como o Microsoft DirectShow ou o Windows Media Format SDK) pode ser usado para reproduzir o arquivo. Se nenhuma correspondência for encontrada, o Player apresentará ao usuário uma caixa de diálogo de aviso que solicita ao usuário a permissão para tentar reproduzir o arquivo. Se você transmitir arquivos de mídia digital usando um esquema de protocolo personalizado, poderá evitar que esse aviso apareça no computador do usuário registrando o esquema e fornecendo um valor para o tempo de execução.

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
| 6     | Renderizar usando o Windows Media Format SDK. |
| 7     | Renderizar usando o Microsoft DirectShow.         |



 

Alterar o valor de *tempo de execução* de um esquema que o Windows Media Format SDK suporta não terá nenhum efeito. O Player sempre usará o SDK do Windows Media Format como o tempo de execução para esquemas que o Windows Media Format SDK suporta. Esse valor de registro foi projetado para permitir a configuração de tempo de execução para esquemas personalizados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro**](registry-settings.md)
</dt> </dl>

 

 




