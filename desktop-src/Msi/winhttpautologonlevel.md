---
description: A política de logon automático (logon automático) determina quando é aceitável que o WinHTTP inclua as credenciais padrão em uma solicitação para o servidor.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828856"
---
# <a name="winhttpautologonlevel"></a>WinHttpAutoLogonLevel

A política de logon automático (logon automático) determina quando é aceitável que o *WinHTTP* inclua as credenciais padrão em uma solicitação para o servidor.

Você pode definir esse valor como **L** para **o nível de segurança do WinHTTP \_ AutoLogon \_ \_ \_ baixo**, definir como **M** para o nível de segurança do **WinHTTP \_ AutoLogon \_ \_ \_ Medium** e definir como **H** para o nível de **segurança do WinHTTP \_ logon automático \_ \_ \_ alto**. O nível padrão é o **nível de segurança do WinHTTP com \_ logon automático \_ \_ \_ médio**. Para obter mais informações sobre a política de logon automático, consulte a seção para [autenticação no WinHTTP](../winhttp/authentication-in-winhttp.md).

**Windows 8 e Windows Server 2012:** Essa política requer Windows Installer em execução no Windows 8 ou no Windows Server 2012 e não está disponível em todas as versões anteriores do Windows.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ sz**

 

 
