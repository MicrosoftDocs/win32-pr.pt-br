---
title: Persistência de configuração
description: Persistência de configuração
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows SDK do formato de mídia, persistência
- Windows SDK de formato de mídia, persistência de configuração
- ASF (Advanced Systems Format), persistência
- ASF (formato de sistemas avançados), persistência
- ASF (Advanced Systems Format), persistência de configuração
- ASF (formato de sistemas avançados), persistência de configuração
- persistência de configuração
- persistência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b5b2442779fb709299f42e0194317aadaf54a51cd4946e61adf7a90a50957d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434353"
---
# <a name="configuration-persistence"></a>Persistência de configuração

nenhuma das propriedades habilitadas para gravação descritas nesta documentação é salva pelo SDK do Windows Media. Cada aplicativo que usa o SDK deve fornecer seus próprios procedimentos de persistência, conforme necessário, e invocar o método Set apropriado em cada instância do SDK. Dessa forma, as alterações de configuração feitas por um aplicativo não afetam outro aplicativo. Por exemplo, alterar o tempo de buffer em um player não afeta outro jogador.

A única exceção a essa regra é para as informações de credenciais. Se o aplicativo indicar, em seu retorno, da chamada **AcquireCredentials** , que as informações de ID de usuário e senha devem ser mantidas, o SDK salvará essas informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando a funcionalidade de rede**](implementing-network-functionality.md)
</dt> <dt>

[**Interface IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




