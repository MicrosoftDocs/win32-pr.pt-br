---
description: Políticas do sistema de usuário usadas com o Windows Instalador.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Políticas de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ce52f4a691729c71ed57ddba8dd80811681844e1ba6c02664ee50c11f8d0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623085"
---
# <a name="user-policies"></a>Políticas de usuário

As políticas de usuário a seguir podem ser configuradas em

**HKEY \_ Atual \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**



| Nome do valor                                                            | Tipos de dados de valor          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated](alwaysinstallelevated.md)<br/>         | **REG \_ DWORD**<br/> | Se esse valor for definido como "1" e o valor do computador correspondente também estiver definido, o instalador sempre será instalado com privilégios elevados.<br/> Caso contrário, o instalador usa privilégios elevados para instalar aplicativos gerenciados e usa o nível de privilégio do usuário atual para aplicativos não gerenciados.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **REG \_ DWORD**<br/> | Se a política [DisableMedia](disablemedia.md) estiver definida como "1", os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo Procurar para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis. A navegação por outros produtos é impedida, independentemente de a instalação estar com privilégios elevados. Ainda é possível que o usuário reinstale o produto da mídia se o usuário tiver uma fonte de mídia rotulada corretamente.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **REG \_ DWORD**<br/> | Se esse valor for definido como "1", o instalador não armazenará arquivos de reação durante a instalação, desabilitando a reação da instalação. Por padrão, a reação está habilitada. Os administradores são aconselhados a não usar essa política, a menos que seja absolutamente essencial.<br/>                                                                                                                                                                                                                                                             |
| [Searchorder](searchorder.md)<br/>                             | **REG \_ SZ**<br/>    | Ordem na qual o instalador pesquisa os três tipos diferentes de fontes:<br/> "n"– rede<br/> "m"– mídia (CD-ROM ou DVD)<br/> "u"– URL (Uniform Resource Locator)<br/> Por exemplo, um valor de "nmu" instrui o instalador a pesquisar as fontes de rede primeiro, as fontes de mídia segundo e as fontes de URL por último. Deixar de fora uma letra remove o tipo de volume correspondente da pesquisa. A ordem padrão na ausência desse valor é rede primeiro, depois mídia seguida por URL.<br/>          |
| [Política TransformsAtSource](transformsatsource-policy.md)<br/> | **REG \_ DWORD**<br/> | Se esse valor existir e for definido como "1"; o instalador procura arquivos de transformação na raiz de quaisquer fontes de rede na [**lista de origem**](sourcelist.md) do produto. Por padrão, as transformação são armazenadas na pasta Dados do Aplicativo do perfil de um usuário.<br/>                                                                                                                                                                                                                                             |



 

 

 




