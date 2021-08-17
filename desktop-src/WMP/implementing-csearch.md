---
title: Implementando CSearch
description: Implementando CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- plug-ins Windows Media Player, classe CSearch
- plug-ins, classe CSearch
- plug-ins de interface do usuário, classe CSearch
- Plug-ins de interface do usuário, classe CSearch
- Classe CSearch
- Guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f99f3e232d11075bde9905169099649a3b6e754454ac10af60b8a83493fcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748150"
---
# <a name="implementing-csearch"></a>Implementando CSearch

a interface **IWMPPluginUI** tem vários métodos que são chamados por Windows Media Player em momentos diferentes durante o ciclo de vida de uma instância de plug-in. O assistente fornece implementações básicas desses métodos, bem como o construtor de classes e o destruidor e outros métodos de classe. o arquivo Search. h deve ser modificado para que Windows Media Player possa se comunicar com a interface do usuário, que é descrita na próxima seção.

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

 

 




