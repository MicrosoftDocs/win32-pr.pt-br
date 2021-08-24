---
description: Crypt32.dll é o módulo que implementa muitas das funções CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll versões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fed9fb7e31af86673c4d24a9dd828c8d690441986725026f982c0720753c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876466"
---
# <a name="crypt32dll-versions"></a>Crypt32.dll versões

Crypt32.dll é o módulo que implementa muitas das funções certificate e Cryptographic Messaging no CryptoAPI, como [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll é um módulo que vem com os sistemas operacionais Windows e Windows Server, mas diferentes versões dessa DLL fornecem funcionalidades diferentes. Não há NENHUMA API para determinar a versão do CryptoAPI que está em uso, mas você pode determinar a versão do Crypt32.dll que está atualmente em uso usando as funções [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) e [**VerQueryValue.**](/windows/win32/api/winver/nf-winver-verqueryvaluea)

Em geral, os intervalos de versão Crypt32.dll são mapeadas para as versões do sistema operacional, conforme mostrado na tabela a seguir. No entanto, essa tabela deve ser usada como uma diretriz apenas porque é possível, por meio de outras vias de atualização, que a versão Crypt32.dll seja diferente da indicada na tabela.

| Crypt32.dll versão                               | Sistema operacional                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *versão* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *versão* >= 5.131.2600.1243                   | Windows XP com Service Pack 2 (SP2)Windows XP com Service Pack 1 (SP1) com hotfix [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <*=* versão < 5.131.2600.1243 | Windows XP com SP1Windows XP<br/>                                                                                                                                        |



 

 

 
