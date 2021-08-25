---
description: Visão geral do modelo em cascata para a classe RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: O modelo RealTimeStylus em cascata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf848f1382a8c6a54f58fb6db864ece165c7cff2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467993"
---
# <a name="the-cascaded-realtimestylus-model"></a>O modelo RealTimeStylus em cascata

O modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata permite que você use dois objetos **RealTimeStylus** , cada um executando em um thread diferente. Com esse modelo, você anexa um objeto **RealTimeStylus** secundário a um objeto **RealTimeStylus** primário. O objeto **RealTimeStylus** secundário é anexado como o único plug-in assíncrono na coleção de plug-ins assíncrono do objeto **RealTimeStylus** primário.

O modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata pode ser útil nos cenários a seguir.

-   Você pode adicionar determinadas tarefas que podem ser computacionalmente exigentes, ainda que ainda exijam acesso em tempo real ao fluxo de dados da caneta do Tablet, como reconhecimento de gestos com vários traços, à coleção de plug-ins síncrona do objeto [**RealTimeStylus**](realtimestylus-class.md) secundário.
-   Você pode distribuir a carga computacional de seus plug-ins síncronos em dois threads, reduzindo atrasos na coleta de tintas em alguns Tablet PCs.

O diagrama a seguir ilustra o fluxo de dados da caneta do Tablet por meio de dois objetos [**RealTimeStylus**](realtimestylus-class.md) em cascata e suas coleções de plug-ins.

![ilustração mostrando fluxo de dados RealTimeStylus em cascata](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

Neste diagrama, a letra do círculo "A" representa os dados da caneta do Tablet que já foram processados pelos objetos [**RealTimeStylus**](realtimestylus-class.md) primários e secundários e que foram colocados na fila de saída do objeto **RealTimeStylus** secundário. O círculo "B" representa os dados da caneta do Tablet que já foram processados pelo objeto **RealTimeStylus** primário e adicionados à fila de saída do objeto **RealTimeStylus** primário e ainda não foram enviados para o objeto **RealTimeStylus** secundário. O círculo "C" representa os dados da caneta eletrônica que o objeto **RealTimeStylus** primário está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e colocado na fila de saída. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

## <a name="constraints"></a>Restrições

Se você usar o construtor [**RealTimeStylus**](realtimestylus-class.md) padrão, criará um objeto **RealTimeStylus** que só pode aceitar a entrada de outro objeto **RealTimeStylus** .

A lista a seguir descreve as restrições associadas ao uso do modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata.

-   Somente dois objetos [**RealTimeStylus**](realtimestylus-class.md) podem ser usados, um objeto **RealTimeStylus** primário e um objeto **RealTimeStylus** secundário.
-   O objeto [**RealTimeStylus**](realtimestylus-class.md) primário deve ser criado com um construtor que usa o parâmetro **attachedControl** ou *Handle* . O objeto **RealTimeStylus** secundário deve ser criado com o Construtor no-Argument.
-   O objeto [**RealTimeStylus**](realtimestylus-class.md) secundário deve ser o único plug-in assíncrono na coleção de plug-ins assíncrono do objeto **RealTimeStylus** primário.
-   Um objeto [**RealTimeStylus**](realtimestylus-class.md) secundário só pode ser anexado a um objeto **RealTimeStylus** primário por vez. Se ele for adicionado a um segundo objeto **RealTimeStylus** primário, o método [Add](/previous-versions/ms824814(v=msdn.10)) lançará uma exceção e o objeto **RealTimeStylus** secundário não será anexado ao segundo objeto **RealTimeStylus** primário.
-   O comportamento de alguns dos membros do objeto [**RealTimeStylus**](realtimestylus-class.md) secundário é modificado. A tabela a seguir descreve o comportamento modificado desses membros.

    

    
| Membro | Comportamento | 
|--------|----------|
| <a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a> | Esse método retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.<br /> Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, esse método retornará o valor padrão.<br /> | 
| <a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a> | Esse método gera uma exceção <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .<br /> | 
| <a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a> | Esse método retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.<br /> Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, esse método retornará uma matriz vazia.<br /> | 
| <a href="/previous-versions/ms824832(v=msdn.10)">Habilitada</a> | Obter essa propriedade retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.<br /> Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, obter essa propriedade retornará o valor padrão.<br /><blockquote>    [!Note]<br />    A definição dessa propriedade gera uma exceção <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .    </blockquote><br /> | 
| <a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a> | Obter essa propriedade retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.<br /> Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, obter essa propriedade retornará o valor padrão.<br /><blockquote>    [!Note]<br />    A definição dessa propriedade gera uma exceção <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .    </blockquote><br /> | 


    

     

-   O objeto [**RealTimeStylus**](realtimestylus-class.md) pai deve parar de funcionar quando o **RealTimeStylus** filho é Descartado.

 

 
