---
description: Políticas do sistema de usuário usadas com o Windows Installer.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Políticas de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cec4066e4d8267b2750d538e691d91382550fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826847"
---
# <a name="user-policies"></a>Políticas de usuário

As políticas de usuário a seguir podem ser configuradas em

**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**



| Nome do valor                                                            | Tipos de dados de valor          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated](alwaysinstallelevated.md)<br/>         | **REG \_ DWORD**<br/> | Se esse valor for definido como "1" e o valor do computador correspondente também for definido, o instalador sempre será instalado com privilégios elevados.<br/> Caso contrário, o instalador usa privilégios elevados para instalar aplicativos gerenciados e usa o nível de privilégio do usuário atual para aplicativos não gerenciados.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **REG \_ DWORD**<br/> | Se a política de [DisableMedia](disablemedia.md) for definida como "1", os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo de procura para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis. Procurar outros produtos é impedido, independentemente de a instalação estar com privilégios elevados. Ainda é possível que o usuário reinstale o produto da mídia se o usuário tiver uma origem de mídia rotulada corretamente.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **REG \_ DWORD**<br/> | Se esse valor for definido como "1", o instalador não armazenará arquivos de reversão durante a instalação, desabilitando a reversão da instalação. Por padrão, a reversão está habilitada. Os administradores são aconselhados a não usar essa política, a menos que seja absolutamente essencial.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **REG \_ sz**<br/>    | Ordem em que o instalador pesquisa os três tipos diferentes de fontes:<br/> "n" – rede<br/> "m" – mídia (CD-ROM ou DVD)<br/> "u" – URL (Uniform Resource Locator)<br/> Por exemplo, um valor de "NMU" instrui o instalador a Pesquisar fontes de rede primeiro, as fontes de mídia segundo e as origens de URL por último. Deixar uma letra remove o tipo de volume correspondente da pesquisa. A ordem padrão na ausência desse valor é Network First e, em seguida, a mídia seguida por URL.<br/>          |
| [Política de TransformsAtSource](transformsatsource-policy.md)<br/> | **REG \_ DWORD**<br/> | Se esse valor existir e estiver definido como "1"; o instalador pesquisa arquivos de transformação na raiz de qualquer fonte de rede na [**SourceList**](sourcelist.md) do produto. Por padrão, as transformações são armazenadas na pasta de dados do aplicativo do perfil de um usuário.<br/>                                                                                                                                                                                                                                             |



 

 

 




