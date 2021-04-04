---
title: Controlando um dispositivo
description: Depois de descobrir os dispositivos, você pode controlá-los.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822952"
---
# <a name="controlling-a-device"></a>Controlando um dispositivo

Depois de descobrir os dispositivos, você pode controlá-los.

**Para exibir as propriedades do dispositivo**

1.  Selecione um dispositivo na lista **dispositivos encontrados** .
2.  Clique em **Propriedades do dispositivo**. A janela **Propriedades do dispositivo** é exibida com as informações solicitadas.

> [!Note]  
> A funcionalidade **Exibir apresentação** não está disponível no código de exemplo C++.

 

**Para exibir a página de apresentação de um dispositivo**

1.  Selecione um dispositivo na lista **dispositivos encontrados** .
2.  Clique em **Exibir apresentação**. Uma janela do Internet Explorer é exibida com a página de apresentação solicitada.

> [!Note]  
> A funcionalidade do **serviço de exibição desc.** não está disponível no código de exemplo de C++.

 

**Para exibir uma descrição de serviço**

1.  Você pode inserir a URL para a descrição do serviço no **serviço desc.** Campo de URL.

    ![URL de descrição de serviço](images/ucp-url.png)

2.  Clique em **Exibir serviço desc.** A janela do **Visualizador de descrição de serviço** é exibida. Em seguida, você pode procurar a descrição do serviço usando o modo de exibição de árvore. Essa funcionalidade não está disponível no código de exemplo do C++.

    ![janela do Visualizador de descrição de serviço](images/ucp-serv.png)

    Há cinco comandos que podem ser usados na janela do Visualizador de descrição de serviço.



| Botão                 | Ação executada                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Carrega o arquivo mostrado no **serviço desc.** Campo de URL.                                                                                                                              |
| Definir ação             | Selecione um nome de ação na árvore de descrição de serviço e clique em **definir ação**. O nome da ação é inserido no campo **ação de invocação** da janela principal do **UCP genérico** .       |
| Definir variável           | Selecione um nome de variável na árvore de descrição de serviço e clique em **definir variável**. O nome da variável é inserido no campo **variável de consulta** da janela principal do **UCP genérico** . |
| Preencher lista de variáveis | Carrega todos os nomes de variáveis do serviço na lista de **variáveis de consulta** da janela principal do **UCP genérico** .                                                                           |
| Popular lista de ações   | Carrega todos os nomes de ação do serviço na lista de **ações de invocação** da janela principal do **UCP genérico** .                                                                              |



 

**Para controlar um dispositivo**

1.  Na lista **dispositivos encontrados** , selecione o dispositivo que você deseja controlar.
2.  Na lista **escolher serviço** , selecione o serviço que você deseja invocar ou a variável de estado que você deseja consultar.

    ![janela de dispositivos de controle](images/ucp-contr.png)

    > [!Note]  
    > O conteúdo da **lista de serviços** se baseia no dispositivo selecionado na lista **dispositivos encontrados** .

     

3.  Se você quiser descobrir o valor de uma variável de estado para o serviço selecionado, insira o nome da variável no campo **variável de consulta** para serviço. Clique em **Consulta**. Os resultados são mostrados no campo **valor do estado da consulta/argumentos fora da ação** .
4.  Se você quiser invocar uma ação para um serviço, insira o nome da ação no campo **ação de invocação** e todos os argumentos no campo **argumentos da ação** . Clique em **invocar**. Os resultados são mostrados no campo **valor do estado da consulta/argumentos fora da ação** , se houver.

    O valor de retorno, se houver, está contido no primeiro argumento out.

    > [!Note]  
    > Se houver vários argumentos para uma ação, separe-os com espaços.

     

5.  Exiba informações de eventos no campo **eventos** para o serviço selecionado.

 

 




