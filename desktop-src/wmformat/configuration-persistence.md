---
title: Persistência de configuração
description: Persistência de configuração
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- SDK do Windows Media Format, persistência
- SDK do Windows Media Format, persistência de configuração
- ASF (Advanced Systems Format), persistência
- ASF (formato de sistemas avançados), persistência
- ASF (Advanced Systems Format), persistência de configuração
- ASF (formato de sistemas avançados), persistência de configuração
- persistência de configuração
- persistência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365619"
---
# <a name="configuration-persistence"></a>Persistência de configuração

Nenhuma das propriedades habilitadas para gravação descritas nesta documentação é salva pelo SDK do Windows Media. Cada aplicativo que usa o SDK deve fornecer seus próprios procedimentos de persistência, conforme necessário, e invocar o método Set apropriado em cada instância do SDK. Dessa forma, as alterações de configuração feitas por um aplicativo não afetam outro aplicativo. Por exemplo, alterar o tempo de buffer em um player não afeta outro jogador.

A única exceção a essa regra é para as informações de credenciais. Se o aplicativo indicar, em seu retorno, da chamada **AcquireCredentials** , que as informações de ID de usuário e senha devem ser mantidas, o SDK salvará essas informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando a funcionalidade de rede**](implementing-network-functionality.md)
</dt> <dt>

[**Interface IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




