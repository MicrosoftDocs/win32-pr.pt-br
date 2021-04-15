---
title: Implementando CSearch
description: Implementando CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Plug-ins do Windows Media Player, classe CSearch
- plug-ins, classe CSearch
- plug-ins de interface do usuário, classe CSearch
- Plug-ins de interface do usuário, classe CSearch
- Classe CSearch
- Guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498652"
---
# <a name="implementing-csearch"></a>Implementando CSearch

A interface **IWMPPluginUI** tem vários métodos que são chamados pelo Windows Media Player em momentos diferentes durante o ciclo de vida de uma instância de plug-in. O assistente fornece implementações básicas desses métodos, bem como o construtor de classes e o destruidor e outros métodos de classe. O arquivo Search. h deve ser modificado para que o Windows Media Player possa se comunicar com a interface do usuário, que é descrita na próxima seção.

Para que a classe CPluginWindow tenha acesso à variável m de membro privado \_ , uma declaração de classe Friend deve ser feita dentro da definição de classe CSearch, conforme mostrado no seguinte trecho de código:


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação de plug-ins de interface do usuário**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




