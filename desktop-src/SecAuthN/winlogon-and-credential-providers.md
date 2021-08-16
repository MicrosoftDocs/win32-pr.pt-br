---
description: é o módulo Windows que executa logon interativo para uma sessão de logon. O comportamento do Winlogon pode ser personalizado pela implementação e registro de um provedor de credenciais.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon e provedores de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a110c741289de9fdd08f1f5d5c820e9695f057b1d74db2e56f014f5da28eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785766"
---
# <a name="winlogon-and-credential-providers"></a>Winlogon e provedores de credenciais

o [*Winlogon*](../secgloss/w-gly.md) é o módulo Windows que executa logon interativo para uma [*sessão de logon*](../secgloss/l-gly.md). O comportamento do Winlogon pode ser personalizado pela implementação e registro de um provedor de credenciais.

Para obter informações sobre como implementar um provedor de credenciais, consulte os tópicos a seguir.



| Tópico                                                                                                           | Descrição                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [experiência de Logon Windows controlada pelo provedor de credenciais](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Visão geral do Winlogon e da arquitetura do provedor de credenciais e um provedor de credenciais de exemplo.<br/> |
| [Interfaces do Shell](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Referência da interface do provedor de credenciais.<br/>                                                    |
| [Provedores de credenciais no Windows 10](credential-providers-in-windows.md)<br/>                            | Provedores de credenciais de terceiros e provedores de credenciais do sistema no Windows 10.<br/>             |



 

para obter uma implementação de provedor de credenciais de exemplo, consulte o exemplo localizado no diretório de instalação SDK do Windows em \\ samples \\ Security \\ credentialprovider.

**Windows Server 2003 e Windows XP:** Não há suporte para provedores de credenciais. Para obter informações sobre como personalizar o Winlogon, consulte [Winlogon e Gina](winlogon-and-gina.md).

 

 
