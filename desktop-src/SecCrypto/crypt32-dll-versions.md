---
description: Crypt32.dll é o módulo que implementa muitas das funções de CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Versões do Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647005"
---
# <a name="crypt32dll-versions"></a>Versões do Crypt32.dll

Crypt32.dll é o módulo que implementa muitas das funções de certificado e de mensagens criptográficas no CryptoAPI, como [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll é um módulo que acompanha os sistemas operacionais Windows e Windows Server, mas versões diferentes dessa DLL fornecem recursos diferentes. Não há API para determinar a versão do CryptoAPI que está em uso, mas você pode determinar a versão do Crypt32.dll que está em uso no momento usando as funções [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) e [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .

Em geral, os intervalos de versão do Crypt32.dll são mapeados para as versões do sistema operacional, conforme mostrado na tabela a seguir. No entanto, essa tabela deve ser usada como uma diretriz somente porque é possível, por meio de outros caminhos de atualização, que a versão Crypt32.dll será diferente da indicada na tabela.

| Versão do Crypt32.dll                               | Sistema operacional                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *versão* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *versão* >= 5.131.2600.1243                   | Windows XP com Service Pack 2 (SP2) Windows XP com Service Pack 1 (SP1) com hotfix [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *versão* < 5.131.2600.1243 | Windows XP com SP1Windows XP<br/>                                                                                                                                        |



 

 

 
