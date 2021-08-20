---
description: Como o protocolo Kerberos foi originalmente projetado, uma chave mestra para um usuário foi derivada de uma senha fornecida pelo usuário.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Ticket-Granting Tíquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd56ef05ce2ea9149b9bd35ef17dc684973f7125026f474e5a8dd3d1d14ff4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916378"
---
# <a name="ticket-granting-tickets"></a>Ticket-Granting Tíquetes

Como o [*protocolo Kerberos*](../secgloss/k-gly.md) foi originalmente projetado, uma chave mestra para um usuário foi derivada de uma senha fornecida pelo usuário. Quando um usuário fez logon, o cliente Kerberos na estação de trabalho do usuário aceitou a senha do usuário e a converteu em uma chave de criptografia passando o texto por meio de uma função de [*hash*](../secgloss/h-gly.md) de ida. O hash resultante era a chave [*mestra do usuário.*](../secgloss/m-gly.md) O cliente usou essa *chave mestra para* descriptografar [*chaves de sessão*](../secgloss/s-gly.md) recebidas do KDC.

O problema com o design Kerberos original é que o cliente precisa da chave mestra do usuário sempre que descriptografa uma chave de sessão do KDC. Isso significa que o cliente deve solicitar a senha ao usuário no início de cada troca de cliente/servidor ou o cliente deve armazenar a chave do usuário na estação de trabalho. As interrupções frequentes do usuário são muito invasivas. Armazenar a chave na estação de trabalho corre o risco de comprometer uma chave derivada da senha do usuário, que é uma chave de longo prazo.

A solução do protocolo Kerberos para esse problema é que o cliente receba uma chave temporária do KDC. Essa chave temporária só é boa para esta [*sessão de logon.*](../secgloss/l-gly.md) Quando um usuário faz logor, o cliente solicita um tíquete para o KDC da mesma forma que solicita um tíquete para qualquer outro serviço. O KDC responde criando uma chave de sessão de logon e um tíquete para um servidor especial, o serviço de concessão de tíquete completo do KDC. Uma cópia da chave de sessão de logon é inserida no tíquete e o tíquete é criptografado com a chave mestra do KDC. Outra cópia da chave de sessão de logon é criptografada com a chave mestra do usuário derivada da senha de logon do usuário. O tíquete e a chave de sessão criptografada são enviados ao cliente.

Quando o cliente obtém a resposta do KDC, ele descriptografa a chave de sessão de logon com a chave mestra do usuário derivada da senha do usuário. O cliente não precisa mais da chave derivada da senha do usuário porque agora o cliente usará a chave de sessão de logon para descriptografar sua cópia de qualquer chave de sessão de servidor que ele obtém do KDC. O cliente armazena a chave de sessão de logon em seu cache de tíquetes junto com seu tíquete para o serviço de concessão de tíquete completo do KDC.

O tíquete para o serviço de concessão de tíquete completo é chamado de TGT (tíquete de concessão de tíquete). Quando o cliente solicita ao KDC um tíquete para um servidor, ele apresenta credenciais na forma de uma mensagem de autenticador e um tíquete , nesse caso, um TGT, assim como ele apresentaria credenciais para qualquer outro serviço. [](../secgloss/c-gly.md) O serviço de concessão de tíquete abre o TGT com sua chave mestra, extrai a chave de sessão de logon para esse cliente e usa a chave de sessão de logon para criptografar a cópia do cliente de uma chave de sessão para o servidor.

 

 
