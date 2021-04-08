---
description: O modelo de segurança usado no protocolo SMB da Microsoft é idêntico ao usado por outras variantes de SMB e consiste em dois níveis de segurança&\# 8212; usuário e compartilhamento.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticação do protocolo SMB da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827065"
---
# <a name="microsoft-smb-protocol-authentication"></a>Autenticação do protocolo SMB da Microsoft

O modelo de segurança usado no protocolo SMB da Microsoft é idêntico ao usado por outras variantes de SMB e consiste em dois níveis de segurança: usuário e compartilhamento. Um compartilhamento é um arquivo, diretório ou impressora que pode ser acessado pelos clientes do protocolo Microsoft SMB.

A autenticação no nível do usuário indica que o cliente que está tentando acessar um compartilhamento em um servidor deve fornecer um nome de usuário e senha. Quando autenticado, o usuário pode acessar todos os compartilhamentos em um servidor também não protegido pela segurança em nível de compartilhamento. Esse nível de segurança permite que os administradores do sistema determinem especificamente quais usuários e grupos podem acessar um compartilhamento.

A autenticação de nível de compartilhamento indica que o acesso a um compartilhamento é controlado por uma senha atribuída somente a esse compartilhamento. Diferentemente da segurança em nível de usuário, esse nível de segurança não exige um nome de usuário para autenticação e nenhuma identidade de usuário é estabelecida.

Em ambos os níveis de segurança, a senha é criptografada antes de ser enviada ao servidor. [NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) e a criptografia do LM (LAN Manager) mais antiga têm suporte pelo protocolo SMB da Microsoft. Os dois métodos de criptografia usam a autenticação de desafio/resposta, em que o servidor envia ao cliente uma cadeia de caracteres aleatória e o cliente retorna uma cadeia de caracteres de resposta computada que comprova que o cliente tem credenciais suficientes para acesso.

 

 
