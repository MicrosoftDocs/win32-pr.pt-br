---
description: A autenticação inicial ocorre quando o servidor recebe uma resposta de desafio de um cliente.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Autenticação inicial usando Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6e9582161eb43e5109af4dc223ae150e94cbddf9b3514dabcb30339a3acc36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482616"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Autenticação inicial usando Microsoft Digest

A autenticação inicial ocorre quando o servidor recebe uma resposta de desafio de um cliente. A autenticação de uma resposta de desafio normalmente envolve um mínimo de dois servidores:

-   O servidor de origem — recebe a solicitação do cliente e emite um desafio e, em seguida, recebe a resposta de desafio do cliente que deve ser autenticado.
-   O servidor de autenticação — recebe informações de autorização do servidor de origem e executa a autenticação. Normalmente, esse servidor é um controlador de domínio que dá suporte a vários servidores de origem.

Quando o servidor de origem recebe uma solicitação com um cabeçalho de autorização que contém uma resposta de desafio de resumo, a autenticação continua da seguinte maneira:

-   A identidade do servidor de origem é verificada em relação ao servidor codificado no nonce do desafio.
-   O carimbo de data/hora codificado no nonce é verificado. Se o nonce tiver expirado e as informações de nome de usuário/senha forem válidas, o servidor de origem encerrará a autenticação emitindo um novo desafio de resumo com a diretiva obsoleta definida como "true". Isso indica que apenas o nonce era "obsoleto" e o cliente pode responder ao novo desafio usando a senha usada na resposta anterior. Se o cliente receber um novo desafio depois de enviar a resposta de desafio para o desafio obsoleto, o cliente deverá gerar uma nova resposta de desafio.
-   Se a detecção de reprodução for imposta, a diretiva NC (contagem de nonce) será verificada em relação ao banco de dados de sessão nonce mantido pelo servidor.
-   O servidor de autenticação é identificado e enviou as informações de autorização do cliente.
-   O servidor de autenticação verifica a identidade do servidor codificado no nonce em relação à identidade do servidor de origem.
-   O servidor de autenticação, que é um controlador de domínio, recupera a senha do usuário.
-   Usando as informações de autorização, a senha e a identificação do servidor de origem, o servidor de autenticação computa o valor que o cliente deve ter fornecido na diretiva de resposta da resposta de desafio. O servidor de autenticação compara o valor calculado à resposta do cliente para determinar o êxito ou a falha da autenticação.

Se a autenticação for bem-sucedida, o [*contexto de segurança*](../secgloss/s-gly.md) do usuário e uma [*chave de sessão*](../secgloss/s-gly.md) de resumo serão retornados para o servidor de origem. Se a autenticação falhar, o servidor de origem deverá gerar uma resposta de erro. Após uma autenticação bem-sucedida, o servidor de origem retorna o recurso solicitado ao cliente.

A chave de sessão de resumo retornada pelo servidor de autenticação é armazenada em cache pelo servidor de origem para uso na autenticação de solicitações futuras. Para obter mais informações, consulte [Autenticando solicitações subsequentes usando Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
