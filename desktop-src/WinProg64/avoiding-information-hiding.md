---
title: Evitando a ocultação de informações
description: Ocasionalmente, os programas deliberadamente ou inadvertidamente ocultam informações do mecanismo de marshaling RPC.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- compatibilidade com versões anteriores programação de 64 bits do Windows
- problemas de compatibilidade de programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4b9e4ba7ed5165378beb93005243af03f9e469
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366276"
---
# <a name="avoiding-information-hiding"></a>Evitando a ocultação de informações

Ocasionalmente, os programas deliberadamente ou inadvertidamente ocultam informações do mecanismo de marshaling RPC. Alguns exemplos são os seguintes:

-   Enviando uma estrutura de dados como um bloco de bytes não diferenciado
-   Aproveitando o desempenho usando um efeito colateral de um método para canalizar dados adicionais pela conexão
-   Tentando disfarçar um identificador passando-o como um **DWORD** ou um **ULONG**

Essas técnicas são quase Garantidas de introduzir problemas de compatibilidade mesmo antes de você portar seu aplicativo para o Windows de 64 bits.

Em vez de enviar um contexto de servidor como um **DWORD** em uma chamada de procedimento remoto padrão, use um identificador de contexto para fornecer um identificador opaco para um contexto de servidor que é mantido em nome de um cliente. Os contextos são identificados por GUIDs definidos pelo tempo de execução de RPC quando um servidor cria um identificador de contexto para um cliente. Nenhum ponteiro é usado pela transmissão e a operação é completamente transparente entre os limites de 32 ou 64 bits. Para obter mais informações sobre como usar identificadores de contexto, consulte [identificadores de contexto](/windows/desktop/Rpc/context-handles).

As interfaces DCOM não podem usar identificadores de contexto porque o COM fornece seu próprio gerenciamento de contexto. Em vez de criar um identificador de contexto, você pode passar um ponteiro de interface para o objeto COM. Em seguida, você pode chamar os métodos diretamente por meio do ponteiro de interface ou posicionar o ponteiro dentro de outras chamadas. Para liberar o objeto Server, o cliente chama o método **Release** da interface por meio do ponteiro de interface.

Novamente, pode haver ocasiões em que você não pode alterar o design original do código que está sendo portado. Se não houver nenhuma maneira de evitar o envio de um ponteiro pela conexão como um **DWORD**, você precisará implementar alguma forma de mapeamento do lado do servidor entre os valores **DWORD** e os ponteiros. Uma maneira de fazer isso é alterar os ponteiros no aplicativo do lado do cliente para tipos de precisão de ponteiro, como **ULONG \_ PTR** ou **DWORD \_ PTR**. Em seguida, use a \[ [**chamada MIDL \_ como**](/windows/desktop/Midl/call-as) \] atributo para colocar os ponteiros na transmissão como valores **DWORD** . O wrapper do lado do cliente precisa passar apenas os argumentos. O wrapper do lado do servidor manipula o mapeamento entre os dois tipos. De forma semelhante, você pode usar o \[ atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] ou o \[ atributo [**representar \_ como**](/windows/desktop/Midl/represent-as) \] para converter seus dados em um formato compatível com versões anteriores para a representação de transmissão.

Se a compatibilidade de conexão reversa não for um problema ou se o identificador não for usado para chamadas remotas e você tiver certeza de que as chamadas remotas entre os processos de 32 e 64 bits nunca acontecerão, você poderá redefinir um argumento como um **ULONG64**. Se necessário, você pode modificar o aplicativo de 32 bits para passar um **DWORD** para o usuário. Como alternativa, você pode criar stubs separados de arquivos IDL separados para cada plataforma usando um **DWORD** em janelas de 32 bits e um **ULONG64** no Windows de 64 bits.

 

 