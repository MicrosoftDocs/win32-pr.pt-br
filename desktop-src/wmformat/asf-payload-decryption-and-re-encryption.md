---
title: Descriptografia de carga ASF e recriptografação
description: Descriptografia de carga ASF e recriptografação
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- SDK do Windows Media Format, descriptografia e recriptografia de conteúdo ASF
- Windows Media Format SDK, descriptografia de carga e nova criptografia
- SDK do Windows Media Format, descriptografia
- SDK do Windows Media Format, nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia de conteúdo ASF e nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia e descriptografia de conteúdo ASF
- DRM (gerenciamento de direitos digitais), descriptografia de carga e nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia de carga e nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia
- DRM (gerenciamento de direitos digitais), descriptografia
- DRM (gerenciamento de direitos digitais), nova criptografia
- DRM (gerenciamento de direitos digitais), nova criptografia
- APIs estendidas do cliente DRM, descriptografia e descriptografia de carga ASF
- APIs estendidas do cliente, descriptografia de carga ASF e recriptografia
- APIs estendidas do cliente DRM, descriptografia de carga e nova criptografia
- APIs estendidas do cliente, descriptografia de carga e nova criptografia
- APIs estendidas do cliente DRM, descriptografia
- APIs estendidas do cliente, descriptografia
- APIs estendidas do cliente DRM, nova criptografia
- APIs estendidas do cliente, nova criptografia
- ASF (Advanced Systems Format), nova criptografia
- ASF (formato de sistemas avançados), nova criptografia
- ASF (Advanced Systems Format), descriptografia
- ASF (formato de sistemas avançados), descriptografia
- ASF (Advanced Systems Format), descriptografia de carga e nova criptografia
- ASF (formato de sistemas avançados), descriptografia de carga e nova criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635024"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>Descriptografia de carga ASF e recriptografação

As etapas a seguir descrevem as ações que um aplicativo deve concluir para descriptografar e criptografar novamente cada carga:

1.  Incrementar o valor de Salt.
2.  Passe a carga (criptografada com o DRM do Windows Media) e o valor de Salt para a função de descriptografia, [**IWMDRMDecrypt::D ecrypt**](iwmdrmdecrypt-decrypt.md), que retornará a carga, criptografada usando a chave pública RC4.
3.  Derive uma chave RC4 transitória aplicando um hash SHA-1 do vetor de inicialização concatenado com o valor Salt.
4.  Use sua chave transitória para descriptografar a carga.
5.  Criptografar imediatamente a carga com o esquema de proteção de conteúdo autorizado de acordo com as regras de conformidade e de robustez de exportação do Windows Media DRM.
6.  Localize a carga seguinte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exportando conteúdo compactado**](exporting-compressed-content.md)
</dt> </dl>

 

 




