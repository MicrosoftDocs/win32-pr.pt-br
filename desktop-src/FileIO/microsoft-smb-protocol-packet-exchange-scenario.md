---
description: Exemplo de um intercâmbio de pacotes do protocolo SMB da Microsoft entre um cliente e um servidor.
ms.assetid: f831d0de-0e38-4141-811c-892a1b5c4037
title: cenário de Exchange de pacote do protocolo SMB da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47415c6d49f6c1f7b924719d4d012277c03956c1af0d948b3ef66049c1203641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048046"
---
# <a name="microsoft-smb-protocol-packet-exchange-scenario"></a>cenário de Exchange de pacote do protocolo SMB da Microsoft

Este tópico fornece um exemplo de um intercâmbio de pacotes do protocolo SMB da Microsoft entre um cliente e um servidor. As etapas a seguir são uma visão geral do processo:

1.  O cliente e o servidor estabelecem uma sessão NetBIOS.
2.  O cliente e o servidor negociam o dialeto do protocolo SMB da Microsoft.
3.  O cliente faz logon no servidor.
4.  O cliente se conecta a um compartilhamento no servidor.
5.  O cliente abre um arquivo no compartilhamento.
6.  O cliente lê a partir do arquivo.

Primeiro, uma conexão TCP Full duplex é estabelecida pelo cliente com o servidor. Em seguida, o cliente cria e envia um pacote de solicitação de sessão NetBIOS pela conexão TCP. Se o pacote foi formatado corretamente, o servidor retorna um pacote que contém uma mensagem confirmando que a sessão foi estabelecida. Depois disso, o cliente envia os primeiros pacotes do protocolo SMB da Microsoft para o servidor.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pacote 1: \_ negociação de com SMB \_**<br/> **Direção:** Cliente para servidor<br/> **Descrição:** O cliente solicita que o servidor negocie o dialeto do protocolo SMB da Microsoft. Uma lista de cadeias de caracteres que identificam os dialetos com os quais o cliente pode trabalhar está incluída no pacote.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Pacote 2: \_ negociação de com SMB \_**<br/> **Direção:** Servidor para cliente<br/> **Descrição:** O servidor responde à solicitação do cliente para identificar o dialeto do protocolo SMB da Microsoft que será usado na sessão. O pacote retornado também inclui uma cadeia de caracteres aleatória de 8 bytes que será usada na próxima etapa para autenticar o cliente durante o processo de logon.<br/>                                                                                                                                                                                                                                   |
| **Pacote 3: \_ configuração da \_ sessão com SMB \_ \_ ANDX**<br/> **Direção:** Cliente para servidor<br/> **Descrição:** Esse pacote inclui informações sobre os recursos do cliente, portanto, esse pacote deve ser enviado mesmo que o servidor tenha implementado apenas a segurança em nível de compartilhamento.<br/> **Pacote 3: \_ configuração da \_ sessão com SMB \_ \_ ANDX**<br/> **Direção:** Servidor para cliente<br/> **Descrição:** Se o desafio/resposta for aceito pelo servidor, um UID válido será incluído no pacote que é retornado ao cliente. Se não for aceito, o servidor retornará um código de erro neste pacote e negará acesso.<br/> |
| **Pacote 4: \_ ANDX de \_ conexão de árvore com \_ SMB \_**<br/> **Direção:** Cliente para servidor<br/> **Descrição:** O cliente solicita acesso ao compartilhamento. O pacote contém o caminho totalmente especificado do compartilhamento no formato UNC.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Pacote 5: \_ ANDX de \_ conexão de árvore com \_ SMB \_**<br/> **Direção:** Servidor para cliente<br/> **Descrição:** Se o acesso ao compartilhamento for concedido, o servidor retornará a ID de árvore de 16 bits (TID) que corresponde ao compartilhamento nesse pacote. Se o compartilhamento não existir ou se o usuário não tiver credenciais suficientes para acessar o compartilhamento, o servidor retornará um código de erro nesse pacote e negará acesso ao compartilhamento.<br/>                                                                                                                                                                                                 |
| **Pacote 6: \_ ANDX com \_ Open \_ SMB**<br/> **Direção:** Cliente para servidor<br/> **Descrição:** O cliente solicita que o servidor Abra um arquivo no compartilhamento acessado em nome do cliente. Esse pacote contém o nome do arquivo a ser aberto.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| **Pacote 7: SMB \_ com \_ Open \_ ANDX**<br/> **Direção:** Servidor para cliente<br/> **Descrição:** Se o acesso ao arquivo for concedido, o servidor retornará a ID de arquivo do arquivo solicitado. Se o arquivo não existir ou se o usuário não tiver credenciais suficientes para acessar o arquivo, o servidor retornará um código de erro nesse pacote e negará acesso ao arquivo.<br/>                                                                                                                                                                                                                                                  |
| **Pacote 8: \_ ANDX de \_ leitura de com SMB \_**<br/> **Direção:** Cliente para servidor<br/> **Descrição:** O cliente solicita que o servidor leia dados do arquivo aberto em nome do cliente e retorne esses dados para o cliente. A ID de arquivo obtida pelo cliente quando o arquivo foi aberto está incluída neste pacote para identificar em qual arquivo aberto o servidor deve ler dados.<br/>                                                                                                                                                                                                                   |
| **Pacote 9: \_ ANDX de \_ leitura de com SMB \_**<br/> **Direção:** Servidor para cliente<br/> **Descrição:** O servidor retorna os dados de arquivo solicitados neste pacote. Um erro aqui é improvável, uma vez que o acesso ao servidor, ao compartilhamento e ao arquivo foi concedido. No entanto, isso pode acontecer em algumas situações: por exemplo, se o acesso a um compartilhamento for alterado entre a hora em que o arquivo é aberto e a hora em que ele é lido.<br/>                                                                                                                                                                                                      |



 

> [!Note]  
> se você implementar um CIFS que não dá suporte a notificações de alteração, Windows não poderá manter um identificador pendente para o sistema de arquivos e a conexão SMB poderá desaparecer sem aviso prévio.

 

 

 




