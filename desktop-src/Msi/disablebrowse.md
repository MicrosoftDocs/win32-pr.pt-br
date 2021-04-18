---
description: Definir o valor dessa política do sistema por máquina para &\# 0034; 1&\# 0034; impede que usuários não administrativos usem uma caixa de diálogo de procura para localizar fontes de aplicativos gerenciados armazenados em mídia, como CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752047"
---
# <a name="disablebrowse"></a>DisableBrowse

Definir o valor dessa [política de sistema](system-policy.md) por máquina como "1" impede que usuários não administrativos usem uma caixa de [diálogo de procura](browse-dialog.md) para localizar fontes de [*aplicativos gerenciados*](m-gly.md) armazenados em mídia, como CD-ROM. A caixa de combinação "usar recurso de:" para entrada direta está bloqueada e o "procurar..." o botão está desabilitado. Para obter mais detalhes sobre a navegação de origem, consulte [resiliência de origem](source-resiliency.md).

DisableBrowse substitui AllowLockdownBrowse e impede a navegação mesmo se AllowLockdownBrowse estiver definido.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Em alguns casos com DisableBrowse definido, um usuário não administrativo ainda pode ser capaz de instalar aplicativos gerenciados de fontes na mídia rotulada corretamente. Definir a política DisableBrowse apenas desabilita a capacidade de navegar para fontes. Ele pode ser usado para impedir que um usuário não-administrativo navegue para uma nova fonte durante uma instalação, reinstalação ou reparo de instalações por demanda. Se [AllowLockdownMedia](allowlockdownmedia.md) for definido, o usuário não administrativo ainda poderá instalar um aplicativo gerenciado a partir de uma mídia rotulada corretamente.

DisableBrowse impede que o usuário não administrativo navegue para um novo local de mídia ou qualquer outro local de origem. Para obter detalhes de como proteger as fontes de mídia de aplicativos gerenciados, consulte [resiliência de origem](source-resiliency.md).

Para obter informações sobre a interação dessa política com as fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).

 

 



