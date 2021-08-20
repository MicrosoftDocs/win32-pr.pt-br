---
description: Você pode armazenar qualquer tipo de dados específicos do aplicativo com uma superfície. Por exemplo, uma superfície que representa um mapa em um jogo pode conter informações sobre o terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Dados de superfície privada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c010e24f691dc64c75e4dcea428af21d46ebfcb95b31775b9c8db81b2263e6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520188"
---
# <a name="private-surface-data-direct3d-9"></a>Dados de superfície privada (Direct3D 9)

Você pode armazenar qualquer tipo de dados específicos do aplicativo com uma superfície. Por exemplo, uma superfície que representa um mapa em um jogo pode conter informações sobre o terreno.

Uma superfície pode ter mais de um buffer de dados privado. Cada buffer é identificado por um GUID que você fornece ao anexar os dados à superfície.

Para armazenar dados de superfície privada, use SetPrivateData, passando um ponteiro para o buffer de origem, o tamanho dos dados e um GUID definido pelo aplicativo para os dados. Opcionalmente, os dados de origem podem existir na forma de um objeto COM; nesse caso, você passa um ponteiro para o ponteiro da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do objeto e definiu o sinalizador \_ IUNKNOWNPOINTER do D3DSPD.

SetPrivateData aloca um buffer interno para os dados e o copia. Em seguida, você pode liberar com segurança o buffer ou o objeto de origem. A referência interna de buffer ou interface é liberada quando FreePrivateData é chamado. Isso ocorre automaticamente quando a superfície é liberada.

Para recuperar dados privados para uma superfície, você deve alocar um buffer do tamanho correto e, em seguida, chamar o método GetPrivateData, passando o GUID que foi atribuído aos dados. Você é responsável por liberar qualquer memória dinâmica usada para esse buffer. Se os dados são um objeto COM, esse método recupera o [**ponteiro IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Se você não sabe o tamanho de um buffer a ser alocado, primeiro chame GetPrivateData com zero em pSizeOfData. Se o método falhar com D3DERR \_ MOREDATA, ele retornará o número necessário de bytes para o buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
