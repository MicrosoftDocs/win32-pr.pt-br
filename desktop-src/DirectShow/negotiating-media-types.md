---
description: Negociando tipos de mídia
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Negociando tipos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105792647"
---
# <a name="negotiating-media-types"></a>Negociando tipos de mídia

Quando o Gerenciador de gráfico de filtro chama o método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , ele tem várias opções para especificar um tipo de mídia:

-   **Tipo completo:** Se o tipo de mídia for totalmente especificado, os Pins tentarão se conectar com esse tipo. Se não puderem, a tentativa de conexão falhará.
-   **Tipo de mídia parcial:** Um tipo de mídia será *parcial* se o tipo de tipo principal, subtipo ou formato for GUID \_ NULL. O valor GUID \_ NULL age como um "curinga", indicando que qualquer valor é aceitável. Os Pins negociam um tipo que é consistente com o tipo parcial.
-   **Nenhum tipo de mídia:** Se o Gerenciador de gráfico de filtro passar um ponteiro **nulo** , os Pins poderão concordar com qualquer tipo de mídia aceitável para ambos os Pins.

Se os PINs se conectarem, a conexão sempre terá um tipo de mídia completo. A finalidade do tipo de mídia fornecido pelo Gerenciador de gráficos de filtro é limitar os possíveis tipos de conexão.

Durante o processo de negociação, o PIN de saída propõe um tipo de mídia chamando o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) do pino de entrada. O PIN de entrada pode aceitar ou rejeitar o tipo proposto. Esse processo se repete até que o PIN de entrada aceite um tipo, ou que o pino de saída fique sem tipos e a conexão falhe.

Como um pino de saída seleciona os tipos de mídia a serem propordos depende da implementação. Nas classes base do DirectShow, o pino de saída chama [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) no pino de entrada. Esse método retorna um enumerador que enumera os tipos de mídia preferenciais do pino de entrada. Falhando, o PIN de saída enumera seus próprios tipos preferenciais.

**Trabalhando com tipos de mídia**

Em qualquer função que recebe um parâmetro de **\_ \_ tipo de mídia am** , sempre valide os valores de **cbFormat** e **formatType** antes de desreferenciar o membro **pbFormat** . O código a seguir está incorreto:


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



O código a seguir está correto:


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



