---
description: É o Windows que executa o logon interativo para uma sessão de logon. O comportamento do Winlogon pode ser personalizado implementando e registrando um Provedor de Credenciais.
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

[*O Winlogon*](../secgloss/w-gly.md) é o Windows que executa o logon interativo para uma sessão [*de logon*](../secgloss/l-gly.md). O comportamento do Winlogon pode ser personalizado implementando e registrando um Provedor de Credenciais.

Para obter informações sobre como implementar um Provedor de Credenciais, consulte os tópicos a seguir.



| Tópico                                                                                                           | Descrição                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Provedor de Credenciais experiência de Windows logon controlada](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Visão geral do Winlogon e Provedor de Credenciais arquitetura e um exemplo Provedor de Credenciais.<br/> |
| [Shell Interfaces](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Provedor de Credenciais de interface.<br/>                                                    |
| [Provedores de credenciais no Windows 10](credential-providers-in-windows.md)<br/>                            | Provedores de credenciais de terceiros e provedores de credenciais do sistema Windows 10.<br/>             |



 

Para uma implementação Provedor de Credenciais exemplo, consulte o exemplo localizado no diretório de instalação Windows SDK em \\ Samples \\ Security \\ CredentialProvider.

**Windows Server 2003 e Windows XP:** Não há suporte para provedores de credenciais. Para obter informações sobre como personalizar o Winlogon, [consulte Winlogon e LTD.](winlogon-and-gina.md)

 

 
