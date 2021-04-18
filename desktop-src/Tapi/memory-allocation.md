---
description: Os aplicativos devem alocar memória para esses dados; A TAPI e o provedor de serviços fornecem os dados. Se a operação for assíncrona, os dados não estarão disponíveis até que a mensagem de resposta assíncrona indique êxito.
ms.assetid: 61313fe3-74a1-4195-b5af-37463dad02c1
title: Alocação de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f192e34fdc652293c480277631c3839ecd2435fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813053"
---
# <a name="memory-allocation"></a>Alocação de memória

Os aplicativos devem alocar memória para esses dados; A TAPI e o provedor de serviços fornecem os dados. Se a operação for assíncrona, os dados não estarão disponíveis até que a mensagem de resposta assíncrona indique êxito.

Todas as estruturas de dados usadas para passar dados entre o aplicativo e a TAPI são *achatadas*. Ou seja, as estruturas de dados não contêm ponteiros para subestruturas que contêm componentes de dados de tamanho variados. Em vez disso, as estruturas de dados usadas para passar quantidades variáveis de dados de volta para o aplicativo devem ter a seguinte metaestrutura:

``` syntax
  DWORD  dwTotalSize;
  DWORD  dwNeededSize;
  DWORD  dwUsedSize; 
    <fixed size fields> 
  DWORD  dw<VarSizeField1>Size;
  DWORD  dw<VarSizeField1>Offset; 
    <fixed size fields> 
  DWORD  dw<VarSizeField2>Size;
  DWORD  dw<VarSizeField2>Offset; 
    <common extensions> 
    <var sized field1> 
    <var sized field2>
```

O membro **dwTotalSize** é o tamanho, em bytes, alocado para essa estrutura de dados. Ele marca o final da estrutura de dados e é definido pelo aplicativo antes de invocar a função que usa essa estrutura de dados. A função não lê ou grava além desse tamanho. Um aplicativo deve definir o membro **dwTotalSize** para indicar o número total de bytes alocados para a TAPI retornar o conteúdo da estrutura.

A TAPI preenche o membro **dwNeededSize** . Indica quantos bytes são necessários para retornar todos os dados solicitados. A existência de campos de tamanho variados geralmente torna impossível para o aplicativo estimar o tamanho da estrutura de dados necessário para alocar. Esse campo retorna o número de bytes realmente necessários para os dados. Esse número pode ser menor que, igual a, ou maior que **dwTotalSize**, e inclui espaço para o próprio membro **dwTotalSize** . Se for maior, a estrutura retornada só será parcialmente preenchida. Se os campos necessários para o aplicativo estiverem disponíveis na estrutura parcial, nada mais deverá ser feito. Caso contrário, o aplicativo deve alocar uma estrutura pelo menos o tamanho de **dwNeededSize** e invocar a função novamente. Normalmente, há espaço suficiente disponível desta vez para retornar todas as informações, embora seja possível que o tamanho tenha aumentado novamente.

A TAPI preenche o membro **dwUsedSize** se ele retornar dados ao aplicativo para indicar o tamanho real, em bytes, da parte da estrutura de dados que contém dados úteis. Se, por exemplo, uma estrutura que foi alocada for muito pequena e o campo truncado for um campo de tamanho de variavelmente, **dwNeededSize** será maior que **dwTotalSize** e o campo truncado será deixado vazio. Portanto, o membro **dwUsedSize** poderia ser menor do que **dwTotalSize**. Valores de campo parciais não são retornados.

Seguir esse cabeçalho é a parte fixa da estrutura de dados. Ele contém campos regulares e pares de tamanho/deslocamento que descrevem os campos de tamanho real de variavelmente. O campo de deslocamento contém o deslocamento em bytes do campo tamanho de variavelmente do início do registro. O campo tamanho contém o tamanho em bytes do campo tamanho de variavelmente. Se um campo de tamanho de variavelmente estiver vazio, o campo tamanho será zero e o deslocamento será definido como zero. Os campos de tamanho de variavelmente que seriam truncados se o tamanho total da estrutura for insuficiente e ficarão vazios. Ou seja, seu campo de tamanho é definido como zero e o deslocamento é definido como zero. Os campos de tamanho de variavelmente seguem os campos fixos.

Se o provedor de serviços precisar preencher um membro de variável, a TAPI inicializará o tamanho correspondente e os membros de deslocamento como zero. Se o provedor de serviços preencher o membro da variável, ele deverá definir os membros de tamanho e deslocamento correspondentes com os valores apropriados, incluindo **dwUsedSize** e **dwNeededSize** se ele definir membros variáveis. O provedor de serviços não deve truncar um membro variável para ajustá-lo ao espaço disponível.

O provedor de serviços deve iniciar os membros da variável imediatamente após os membros fixos da estrutura e deixar qualquer espaço extra no final da memória alocada para que a TAPI possa usá-la para os membros de comprimento variável. Ele pode posicionar os membros da variável em qualquer ordem, mas os membros devem ser contíguos.

 

 



