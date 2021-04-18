---
description: Eventos de extensão MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventos de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105816021"
---
# <a name="mtp-extension-events"></a>Eventos de extensão MTP

Os eventos notificam um aplicativo de que as alterações ocorreram em, ou com, um dispositivo. Por exemplo, um aplicativo pode se registrar para receber notificações de que um dispositivo foi removido.

## <a name="vendor-extended-event-codes"></a>Fornecedor-códigos de eventos estendidos

Quando um fabricante de dispositivo dá suporte a um evento estendido pelo fornecedor, o driver combina o código de evento do fornecedor (UINT16) com os 16 bits mais altos do GUID de **\_ \_ \_ \_ \_ eventos estendidos do fornecedor do evento do WPD** .

Por exemplo, se o código estendido pelo fornecedor for 0xC001, o GUID resultante será como mostrado no exemplo a seguir:


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Fornecedor-parâmetros de evento estendido

Os parâmetros para um evento estendido de fornecedor são relatados pelo GUID de eventos de **\_ parâmetro de evento \_ \_ \_ WPD** e pelos **\_ \_ \_ parâmetros de \_ evento \_ MTP ext de propriedade WPD**, que é uma coleção de **PROPVARIANTS**. Esses **PROPVARIANTS** correspondem aos parâmetros do evento. Se não houver parâmetros, essa coleção estará vazia.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a extensões de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



