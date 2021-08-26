---
description: 'Há dois tipos distintos de aplicativos de rede de soquete: servidor e cliente.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Sobre servidores e clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d8016d1fc9c23b901a03a924cd0e3ade3982dc2e1bf0db277eac47170d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898636"
---
# <a name="about-servers-and-clients"></a>Sobre servidores e clientes

Há dois tipos distintos de aplicativos de rede de soquete: servidor e cliente.

Servidores e clientes têm comportamentos diferentes; Portanto, o processo de criá-los é diferente. O que vem a seguir é o modelo geral para criar um cliente e servidor TCP/IP de streaming.

## <a name="server"></a>Servidor

1.  Inicialize o Winsock.
2.  Crie um soquete.
3.  Associe o soquete.
4.  Ouça o soquete de um cliente.
5.  Aceitar uma conexão de um cliente.
6.  Receber e enviar dados.
7.  Desconectar.

## <a name="client"></a>Cliente

1.  Inicialize o Winsock.
2.  Crie um soquete.
3.  Conexão ao servidor.
4.  Enviar e receber dados.
5.  Desconectar.

> [!Note]  
> Algumas das etapas são as mesmas para um cliente e um servidor. Essas etapas são implementadas quase exatamente da mesma forma. Algumas das etapas neste guia serão específicas para o tipo de aplicativo que está sendo criado.

 

Primeira etapa: [criando um aplicativo Winsock básico](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



