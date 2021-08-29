---
description: Eventos de extensão MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventos de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a95999557e67ee8929fddc56dd7fd8eb43e6831af9f81f884303a2089bbe3fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806706"
---
# <a name="mtp-extension-events"></a>Eventos de extensão MTP

Os eventos notificam um aplicativo de que ocorreram alterações em ou com um dispositivo. Por exemplo, um aplicativo pode se registrar para receber notficações de que um dispositivo foi removido.

## <a name="vendor-extended-event-codes"></a>Códigos de evento estendidos pelo fornecedor

Quando um fabricante de dispositivo dá suporte a um evento estendido pelo fornecedor, o driver combina o código de evento do fornecedor (UINT16) com os 16 bits mais altos do GUID de EVENTOS ESTENDIDOs do FORNECEDOR de **\_ EVENTOS \_ WPD MTP. \_ \_ \_**

Por exemplo, se o código estendido pelo fornecedor for 0xC001, o GUID resultante será conforme mostrado no exemplo a seguir:


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Parâmetros de evento estendidos pelo fornecedor

Os parâmetros para um evento estendido pelo fornecedor são relatados pelo GUID da **\_ \_ \_ \_ ID** DE EVENTO DE PARÂMETRO DE EVENTO WPD e pela PROPRIEDADE **WPD \_ \_ MTP \_ EXT EVENT \_ \_ PARAMS**, que é uma coleção **de PROPVARIANTS**. Esses **PROPVARIANTS** correspondem aos parâmetros de evento. Se não houver parâmetros, essa coleção será vazia.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a extensões MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



