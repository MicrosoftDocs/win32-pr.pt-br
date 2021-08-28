---
description: O usuário começa a fazer logon na rede digitando um nome de logon e senha. O cliente Kerberos na estação de trabalho do usuário converte a senha em uma chave de criptografia e salva o resultado em uma variável de programa.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Troca de serviços de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480370dd9fe5d7c5fc10e7979de9d4e7f67f99db3e517e1ec6520a3274ef23c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073286"
---
# <a name="authentication-service-exchange"></a>Troca de serviços de autenticação

O usuário começa a fazer logon na rede digitando um nome de logon e senha. O cliente [*Kerberos*](/windows/desktop/SecGloss/k-gly) na estação de trabalho do usuário converte a senha em uma chave de criptografia e salva o resultado em uma variável de programa.

Em seguida, o cliente solicita [*credenciais*](/windows/desktop/SecGloss/c-gly) para o serviço de concessão de TÍQUETE (TGS) do [*centro de distribuição de chaves*](/windows/desktop/SecGloss/k-gly) (KDC) enviando ao serviço de autenticação do KDC uma mensagem do tipo KRB \_ como \_ req (solicitação de serviço de autenticação Kerberos). A primeira parte dessa mensagem identifica o usuário e o serviço TGS que está sendo solicitado. A segunda parte desta mensagem contém dados de pré-autenticação destinados a provar que o usuário conhece a senha. Essa é simplesmente uma mensagem de autenticador que é criptografada com a [*chave mestra*](/windows/desktop/SecGloss/m-gly) derivada da senha de logon do usuário.

Quando o KDC recebe KRB \_ como \_ req, ele pesquisa o usuário em seu banco de dados, obtém a chave mestra do usuário associado, descriptografa os dados de pré-autenticação e avalia o carimbo de data/hora dentro do. Se o carimbo de data/hora for válido, o KDC poderá ter certeza de que os dados de pré-autenticação foram criptografados com a chave mestra do usuário e, portanto, que o cliente é original.

Depois que o KDC verificar a identidade do usuário, ele cria credenciais que o cliente pode apresentar ao TGS, da seguinte maneira:

1.  O KDC inventa uma chave de [*sessão*](/windows/desktop/SecGloss/s-gly) de logon e criptografa uma cópia com a chave mestra do usuário.
2.  O KDC insere outra cópia da chave de sessão de logon e os dados de autorização do usuário em um tíquete de concessão de tíquete (TGT) e criptografa o TGT com a própria chave mestra do KDC.
3.  O KDC envia essas credenciais de volta ao cliente respondendo com uma mensagem do tipo KRB \_ como \_ Rep (resposta do serviço de autenticação Kerberos).
4.  Quando o cliente recebe a resposta, ele usa a chave derivada da senha do usuário para descriptografar a nova chave de sessão de logon.
5.  O cliente armazena a nova chave em seu cache de tíquetes.
6.  O cliente extrai o TGT da mensagem e o armazena em seu cache de tíquete também.

 

 
