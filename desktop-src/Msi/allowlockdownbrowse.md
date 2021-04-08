---
description: Definir o valor dessa política do sistema por máquina para &\# 0034; 1&\# 0034; permite que usuários não administrativos usem uma caixa de diálogo de navegação para localizar fontes de aplicativos gerenciados.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828079"
---
# <a name="allowlockdownbrowse"></a>AllowLockdownBrowse

Definir o valor dessa [política do sistema](system-policy.md) por máquina como "1" permite que usuários não administrativos usem uma caixa de [diálogo de procura](browse-dialog.md) para localizar fontes de [*aplicativos gerenciados*](m-gly.md). As fontes podem incluir mídia, como CD-ROM, URLs e locais de rede. Para obter mais informações, consulte [resiliência de origem](source-resiliency.md). O padrão em Windows Installer é que usuários não administrativos não podem procurar novas fontes de aplicativos gerenciados. As únicas fontes disponíveis são aquelas que já estão registradas na lista de origem do produto. Se essa política estiver definida, um usuário não administrativo poderá procurar novas fontes de aplicativos atribuídos ou publicados ou aplicativos que estão sendo instalados para todos os usuários. A definição de AllowLockdownBrowse também permite que usuários não administrativos executem programas em privilégios LocalSystem durante uma instalação elevada.

A configuração padrão é recomendada para garantir um ambiente seguro.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios LocalSystem se tiverem um pacote Windows Installer que instala ou inicia esses programas.

[DisableBrowse](disablebrowse.md) substitui AllowLockdownBrowse e impede a navegação mesmo se AllowLockdownBrowse estiver definido.

Para obter informações sobre a interação dessa política com as fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> <dt>

[AllowLockdownMedia](allowlockdownmedia.md)
</dt> </dl>

 

 



