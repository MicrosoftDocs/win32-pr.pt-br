---
description: Você pode armazenar qualquer tipo de dados específicos do aplicativo com uma superfície. Por exemplo, uma superfície que representa um mapa em um jogo pode conter informações sobre o terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Dados de superfície privada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105761706"
---
# <a name="private-surface-data-direct3d-9"></a>Dados de superfície privada (Direct3D 9)

Você pode armazenar qualquer tipo de dados específicos do aplicativo com uma superfície. Por exemplo, uma superfície que representa um mapa em um jogo pode conter informações sobre o terreno.

Uma superfície pode ter mais de um buffer de dados privado. Cada buffer é identificado por um GUID que você fornece ao anexar os dados à superfície.

Para armazenar dados de superfície privada, use SetPrivateData, passando um ponteiro para o buffer de origem, o tamanho dos dados e um GUID definido pelo aplicativo para os dados. Opcionalmente, os dados de origem podem existir na forma de um objeto COM; Nesse caso, você passa um ponteiro para o ponteiro de interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do objeto e define o sinalizador D3DSPD \_ IUNKNOWNPOINTER.

SetPrivateData aloca um buffer interno para os dados e copia-o. Em seguida, você pode liberar com segurança o objeto ou o buffer de origem. O buffer interno ou a referência de interface é liberada quando FreePrivateData é chamado. Isso ocorre automaticamente quando a superfície é liberada.

Para recuperar dados privados para uma superfície, você deve alocar um buffer do tamanho correto e, em seguida, chamar o método GetPrivateData, passando o GUID que foi atribuído aos dados. Você é responsável por liberar qualquer memória dinâmica usada para esse buffer. Se os dados forem um objeto COM, esse método recuperará o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

Se você não souber o tamanho de um buffer a ser alocado, primeiro chame GetPrivateData com zero em pSizeOfData. Se o método falhar com D3DERR \_ MOREDATA, ele retornará o número necessário de bytes para o buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
