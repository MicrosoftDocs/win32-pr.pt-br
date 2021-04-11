---
description: Como o protocolo Kerberos foi originalmente projetado, uma chave mestra para um usuário foi derivada de uma senha fornecida pelo usuário.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Tíquetes de Ticket-Granting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dff161ba2d905f676fe6b6b5e7e7d5289ee550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090453"
---
# <a name="ticket-granting-tickets"></a>Tíquetes de Ticket-Granting

Como o [*protocolo Kerberos*](../secgloss/k-gly.md) foi originalmente projetado, uma chave mestra para um usuário foi derivada de uma senha fornecida pelo usuário. Quando um usuário fez logon, o cliente Kerberos na estação de trabalho do usuário aceitou a senha do usuário e a converteu em uma chave de criptografia passando o texto por meio de uma função de [*hash*](../secgloss/h-gly.md) unidirecional. O hash resultante era a [*chave mestra*](../secgloss/m-gly.md)do usuário. O cliente usou essa *chave mestra* para descriptografar [*as chaves de sessão*](../secgloss/s-gly.md) recebidas do KDC.

O problema com o design do Kerberos original é que o cliente precisa da chave mestra do usuário sempre que descriptografa uma chave de sessão do KDC. Isso significa que o cliente deve solicitar a senha ao usuário no início de cada troca de cliente/servidor ou o cliente deve armazenar a chave do usuário na estação de trabalho. Interrupções frequentes do usuário são muito invasivas. Armazenar a chave nos riscos da estação de trabalho compromete uma chave derivada da senha do usuário, que é uma chave de longo prazo.

A solução do protocolo Kerberos para esse problema é que o cliente obtenha uma chave temporária do KDC. Essa chave temporária é boa somente para esta [*sessão de logon*](../secgloss/l-gly.md). Quando um usuário faz logon, o cliente solicita um tíquete para o KDC da mesma forma que solicitaria um tíquete para qualquer outro serviço. O KDC responde criando uma chave de sessão de logon e um tíquete para um servidor especial, o serviço de concessão de tíquete completo do KDC. Uma cópia da chave de sessão de logon é inserida no tíquete e o tíquete é criptografado com a chave mestra do KDC. Outra cópia da chave de sessão de logon é criptografada com a chave mestra do usuário derivada da senha de logon do usuário. O tíquete e a chave de sessão criptografada são enviados ao cliente.

Quando o cliente obtém a resposta do KDC, ele descriptografa a chave de sessão de logon com a chave mestra do usuário derivada da senha do usuário. O cliente não precisa mais da chave derivada da senha do usuário, pois agora o cliente usará a chave de sessão de logon para descriptografar sua cópia de qualquer chave de sessão de servidor obtida do KDC. O cliente armazena a chave de sessão de logon em seu cache de tíquete junto com seu tíquete para o serviço de concessão de tíquete completo do KDC.

O tíquete para o serviço de concessão de tíquete completo é chamado de tíquete de concessão de tíquete (TGT). Quando o cliente solicita ao KDC um tíquete para um servidor, ele apresenta [*credenciais*](../secgloss/c-gly.md) na forma de uma mensagem de autenticador e um tíquete — nesse caso, um TGT — da mesma forma que apresentaria credenciais para qualquer outro serviço. O serviço de concessão de tíquete abre o TGT com sua chave mestra, extrai a chave de sessão de logon para esse cliente e usa a chave de sessão de logon para criptografar a cópia de uma chave de sessão do cliente para o servidor.

 

 
