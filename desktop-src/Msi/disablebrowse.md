---
description: Definir o valor dessa política de sistema por computador como &\# 0034;1&0034; impede que usuários não administrativas usem uma caixa de diálogo Procurar para localizar fontes de \# aplicativos gerenciados armazenados na mídia, como CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e565cca833d8d771b5bc28dea4483049868995a06acc9a42116611a1df6ce098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745566"
---
# <a name="disablebrowse"></a>DisableBrowse

Definir o valor dessa política de sistema por computador como "1" impede [](browse-dialog.md) que usuários não [](m-gly.md) administrativas usem uma caixa de diálogo Procurar para localizar fontes de aplicativos gerenciados armazenados na mídia, como CD-ROM. [](system-policy.md) A caixa de combinação "Usar recurso de:" para entrada direta está bloqueada e a caixa de combinação "Procurar..." O botão está desabilitado. Para obter mais detalhes sobre a navegação de origem, consulte [resiliência de origem.](source-resiliency.md)

DisableBrowse substitui AllowLockdownBrowse e impede a navegação mesmo se AllowLockdownBrowse estiver definido.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Em alguns casos com DisableBrowse definido, um usuário não administrativa ainda pode ser capaz de instalar aplicativos gerenciados de fontes na mídia rotulada corretamente. Definir a política DisableBrowse apenas desabilita a capacidade de navegar até fontes. Ele pode ser usado para impedir que um usuário nãoadministrativo navega para uma nova fonte durante uma instalação, reinstalação ou reparo sob demanda. Se [AllowLockdownMedia](allowlockdownmedia.md) estiver definido, o usuário nãoadministrativo ainda poderá instalar um aplicativo gerenciado da mídia rotulada corretamente.

DisableBrowse impede que o usuário nãoadministrativo navega para um novo local de mídia ou qualquer outro local de origem. Para obter detalhes sobre como proteger fontes de mídia de [aplicativos gerenciados, consulte Resiliência de origem](source-resiliency.md).

Para obter informações sobre a interação dessa política com fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).

 

 



