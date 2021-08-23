---
title: O arquivo de proxy da interface
description: O arquivo de proxy de interface (U \_ p. c) é um arquivo c que contém rotinas equivalentes aos dos arquivos stub de cliente e stub de servidor de uma interface de objeto (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL e MIDL COM, interfaces, arquivos de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedb9de50d00524b1e038f027448be5aaab369aa5d92243d2a3425bf603cd65a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013534"
---
# <a name="the-interface-proxy-file"></a>O arquivo de proxy da interface

O arquivo de proxy de interface (U \_ p. c) é um arquivo c que contém rotinas equivalentes aos dos arquivos stub de cliente e stub de servidor de uma interface de objeto (com). Esse arquivo contém implementações das rotinas substitutas para o cliente e o servidor no modo embutido do compilador ou dados equivalentes e conversões nos modos interpretados, bem como outros dados de cola COM apropriados, como o proxy e o stub vtables.

O arquivo de proxy de interface inclui as rotinas de suporte e os dados somente para métodos das interfaces definidas no arquivo IDL atual. Para esclarecer esse comportamento, um exemplo estendido é usado em toda esta seção. Ao compilar um arquivo IDL com uma interface como IFaceB que herda de IFaceA, IFaceB dados auxiliares relacionados e rotinas são gerados para o arquivo de proxy atual, enquanto a interface base IFaceA relacionadas a dados auxiliares e rotinas são encontradas no proxy gerado a partir do arquivo IDL que contém a definição de IFaceA. O compilador gera todos os dados necessários para identificar os substitutos da interface base e delegá-los quando necessário para dar suporte aos métodos IFaceA usados por meio da interface IFaceB.

Para cada método em uma interface no arquivo IDL atual, o arquivo de proxy contém os dois métodos substitutos a seguir quando compilados no modo misto ([/os](-os.md)) e dados de intérprete equivalentes quando compilados no modo de intérprete ([/Oi](-oi.md)).

-   O substituto do lado do cliente, como o \_ proxy do método IFaceB \_ neste exemplo.

    Esse substituto do lado do cliente é o ponto de entrada virtual para o qual o cliente, por exemplo, IFaceB:: Method, expedetions. Ele realiza marshaling dos argumentos de entrada em um formulário de transmissãotable, transmite os argumentos marshaled com informações que identificam a interface e a operação e, em seguida, desempacota o valor de retorno e quaisquer argumentos de saída quando a operação invocada retorna.

-   O substituto do lado do servidor, por exemplo, o \_ stub do método IFaceB \_ .

    Esse substituto do lado do servidor é o ponto de entrada virtual que o tempo de execução subjacente despacha para o servidor para emular o cliente. Ele desempacota os argumentos de entrada para replicar os dados do cliente, invoca a implementação do servidor da função de interface e, em seguida, realiza o marshaling e transmite o valor de retorno e todos os argumentos de saída para o lado do cliente.

O nome padrão de um arquivo de proxy gerado a partir de um arquivo. idl é \_ o arquivo p. c. Use a opção de compilador [**/proxy nomedearquivo**](-proxy.md) MIDL para substituir o nome padrão do arquivo de proxy da interface. As opções [**/env**](-env.md) e [**/out**](-out.md) afetam esse arquivo.

 

 




