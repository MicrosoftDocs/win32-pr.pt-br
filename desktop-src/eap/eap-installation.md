---
title: Instalação do EAP
description: Os fornecedores implementam EAPs, também conhecidos como protocolos de autenticação, em DLLs (bibliotecas de vínculo dinâmico).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a790f4282ef2658bacdd7f25be647234c3cf32d62ca80e8ce2745da3f4f738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984446"
---
# <a name="eap-installation"></a>Instalação do EAP

Os fornecedores implementam EAPs, também conhecidos como protocolos de autenticação, em DLLs (bibliotecas de vínculo dinâmico). Uma DLL para o protocolo de autenticação deve residir nos computadores cliente e servidor. Para simplificar, as DLLs do cliente e do servidor podem ser idênticas; no entanto, isso não é um requisito. Além disso, lembre-se de que a mesma DLL pode dar suporte a mais de um protocolo de autenticação.

O fornecedor deve fornecer software de instalação para instalar e remover a DLL. O software de instalação também deve criar as chaves e os valores apropriados para o protocolo de autenticação no registro do sistema e removê-los após a desinstalação.

A instalação de cada DLL de EAP deve criar a seguinte chave do registro.

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Services** \\ **RASMAN** \\  \\  \\ **&lt; eaptypeid &gt;** PPP EAP

No caminho anterior, **&lt; eaptypeid &gt;** é a ID do protocolo de autenticação. O fornecedor deve obter essa ID da IANA (Internet Assigned Numbers Authority).

Para obter mais informações e uma descrição dos valores com suporte para essa chave, consulte [valores do registro do protocolo de autenticação](authentication-protocol-registry-values.md).

 

 




